<template lang="pug">
    .home
        v-app(dark)
            v-toolbar
                v-toolbar-title 化身度判定
            v-content
                p ここにアプリが入るぞ
                camera-window


</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import CameraWindow from "@/components/CameraWindow";

export default {
  name: "home",
  components: {
	  CameraWindow,
    HelloWorld
  }
};
</script>

<style lang="stylus">
    @import "../assets/stylus/base"
</style>
