<template>
  <div class="hello">
    <img :src="pictureHover" @mouseover="hover = true" @mouseleave="hover = false">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      pictureStatic: require("../assets/todo.png"),
      pictureGif: require("../assets/todo.gif"),
      hover: false
    }
  },
  computed: {
    pictureHover () {
      if (this.hover == true) {
        return this.pictureGif
      } else {
        return this.pictureStatic
      }
    }
  }
}
</script>

<style scoped> 
img {
  height: 500px;
}
</style>
