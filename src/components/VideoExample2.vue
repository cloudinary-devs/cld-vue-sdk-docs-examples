<script>
import { AdvancedVideo } from '@cloudinary/vue';
import { Cloudinary } from '@cloudinary/url-gen';
import {Transformation} from "@cloudinary/url-gen";
import {reverse,accelerate} from "@cloudinary/url-gen/actions/effect";
import {brightness} from "@cloudinary/url-gen/actions/adjust";
import {max} from "@cloudinary/url-gen/actions/roundCorners";
import {concatenate} from "@cloudinary/url-gen/actions/videoEdit";
import {Concatenate} from "@cloudinary/url-gen/qualifiers/concatenate";


// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
  url: {
      analytics: false,
    }
});

// Use the video with public ID, 'ski_jump'.
const myVideo = cld.video('ski_jump');

// Apply the transformation.
myVideo
  .videoEdit(concatenate(Concatenate.videoSource('ski_jump').transformation(new Transformation().effect(reverse()))))
  .videoEdit(concatenate(Concatenate.videoSource('ski_jump').transformation(new Transformation().effect(accelerate(-50)))))
  .adjust(brightness(10))
  .roundCorners(max());


export default {
  components: {
    AdvancedVideo,
  },
  data() {
    return {
      myVideo,
    };
  },
};
</script>

<template>
  <div class="App-body">
    <h3>Apply several transformations to the elephant video, as shown in <br><a class="App-link" href="https://cloudinary.com/documentation/vue_video_transformations#example_2" target="_blank">Example 2</a></h3>
    <AdvancedVideo :cldVid="myVideo" controls autoPlay loop muted/>
  </div>
</template>