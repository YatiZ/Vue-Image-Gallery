<template>

  <bar @changeColor="changeColor"></bar>    

  <image-gallery ></image-gallery>

</template>

<script>
import Bar from './components/Bar.vue'
import ImageGallery from './components/ImageGallery.vue';

export default{
  components:{Bar,ImageGallery},
}
</script>



