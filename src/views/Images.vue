<script setup>
import QuickStart from '../components/QuickStart.vue';
import FullExample from '../components/FullExample.vue';
import QuickExample from '../components/QuickExample.vue';
import ImageTransformations from '../components/ImageTransformations.vue';
import AssetInstance from '../components/AssetInstance.vue';
import Plugins from '../components/Plugins.vue';
import LazyLoad from '../components/LazyLoad.vue';
import Responsive from '../components/Responsive.vue';
import Accessibility from '../components/Accessibility.vue';
import Placeholder from '../components/Placeholder.vue';
import LazyLoadPlaceholder from '../components/LazyLoadPlaceholder.vue';
import SyntaxOverview from '../components/SyntaxOverview.vue';
import DeliveryType from '../components/DeliveryType.vue';
import TransformingYourImage from '../components/TransformingYourImage.vue';
import ChainingTransformations from '../components/ChainingTransformations.vue';
import ResizingAndCropping from '../components/ResizingAndCropping.vue';
import AutoGravity from '../components/AutoGravity.vue';
import ConvertingFormatExtension from '../components/ConvertingFormatExtension.vue';
import ConvertingFormatDelivery from '../components/ConvertingFormatDelivery.vue';
import AutoFormat from '../components/AutoFormat.vue';
import Effects from '../components/Effects.vue';
import Overlays from '../components/Overlays.vue';
import ImageOptimizations from '../components/ImageOptimizations.vue';
</script>

<template>
  <div class="App-body">
  <h1>Image Transformations</h1>
  </div>
  <QuickStart />
  <QuickExample />
  <FullExample />
  <ImageTransformations />
  <AssetInstance />
  <Plugins />
  <LazyLoad />
  <Responsive />
  <Accessibility />
  <Placeholder />
  <LazyLoadPlaceholder />
  <SyntaxOverview />
  <DeliveryType />
  <TransformingYourImage />
  <ChainingTransformations />
  <ResizingAndCropping />
  <AutoGravity />
  <ConvertingFormatExtension />
  <ConvertingFormatDelivery />
  <AutoFormat />
  <Effects />
  <Overlays />
  <ImageOptimizations />
</template>

<style>
.App-body {
  text-align: center;
  font-size: calc(8px + 2vmin);
  color: black;
}

.App-link {
  color: #FF5050;
}

a:hover {
  color: #FF5050;
  text-decoration: underline;
}

img {
	max-width: 50%;
}

video {
	max-width: 50%;
}
</style>