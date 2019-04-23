<template lang="pug">
    .camera-window
        video(ref="video")
</template>

<script>
export default {
  name: "CameraWindow",
  methods: {
    async setupVideo() {
      const stream = await navigator.mediaDevices.getUserMedia({
        audio: false,
        video: true
      });
      const video = this.$refs.video;
      video.srcObject = stream;
      video.onloadedmetadate = () => {
        video.play();
      };
    }
  },
  mounted() {
    this.setupVideo();
  }
};
</script>

<style scoped lang="stylus"></style>
