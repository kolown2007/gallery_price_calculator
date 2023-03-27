
  <script>
  let widthInch = 0;
  let heightInch = 0;
  let unit = 1;
  let areaCm = 0;
  let dimensionCm = 0;
  let widthCm = 0;
  let heightCm = 0;
  let GalleryPrice = 0;

  function convert() {
  widthCm = widthInch * 2.54;
   heightCm = heightInch * 2.54;
    areaCm = widthCm * heightCm;
    GalleryPrice = areaCm * unit
  }
  </script>
  

<main class ="py-10 px-28 bg-rose-400 text-slate-50"> 
    <h1 class = "text-2xl text-gray-100 ">Gallery Price Calculator</h1>
    <label for="widthInput">Width (inches):</label>
    <input class ="text-gray-900" type="number" id="widthInput" bind:value={widthInch} on:input={convert}>
    <br>
    <br>
    <label for="heightInput">Height (inches):</label>
    <input class ="text-gray-900" type="number" id="heightInput" bind:value={heightInch} on:input={convert}>
    <br>
    <br>

    <p>Dimensions in inches:
     <br>
     {widthInch} in x {heightInch} in
    </p>

  <br>
  <p>
  Dimensions in cm:
  <br>
  {widthCm} cm x {heightCm} cm
    <br>
  </p>
 

  <br>
<p>
  Unit per square centimeter.
  <br>
  <label for="unitInput"></label>
  <input class ="text-gray-900" type="number" id="unitInput" bind:value={unit} on:input={convert}>

</p>

<br>
    
    <p>Gallery Price:  {GalleryPrice.toFixed(0)} </p>


    </main>