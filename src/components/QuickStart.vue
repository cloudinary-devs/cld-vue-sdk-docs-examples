<script>
import { AdvancedImage } from '@cloudinary/vue';
import { Cloudinary } from '@cloudinary/url-gen';
import { fill } from '@cloudinary/url-gen/actions/resize';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate a CloudinaryImage object for the image with the public ID, 'docs/models'.
const myImg = cld.image('docs/models');

// Resize to 250 x 250 pixels using the 'fill' crop mode.
myImg.resize(fill().width(250).height(250));

export default {
  components: {
    AdvancedImage,
  },
  data() {
    return {
      myImg,
    };
  },
};
</script>

<template>
  <div class="App-body">
    <h3>Crop an image to a square, as shown in the<br><a class="App-link" href="https://cloudinary.com/documentation/vue_quick_start" target="_blank">Quick Start Guide</a></h3>
    <AdvancedImage :cldImg="myImg" />
  </div>
</template>
