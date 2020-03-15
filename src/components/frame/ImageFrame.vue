<template>
  <figure class="imageframe">
    <slot>
      <img src="" />
    </slot>
    <figcaption>
      <slot name="caption">Please provide an image title</slot>
    </figcaption>
  </figure>
</template>

<style>
figure {
  box-shadow: 0 0 4px 0 black;
  padding: 0.75cm;
  background-color: whitesmoke;
}
figcaption {
  padding-top: 0.5cm;
}

figure > img {
  width: 100%;
  max-width: 100%;
  display: block;
  margin: 0 auto;
}

figure > img[src=""] {
  position: relative;
  border: 2px solid red;
  height: 100px;
  background-color: gold;
}
figure > img[src=""]::before {
  content: "No image";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: white;
}
</style>
