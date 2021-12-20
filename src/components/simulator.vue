<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>  
   <div v-text="ImageBase64">5</div>
</div>
</template>

<script>
import Unity from 'vue-unity-webgl'

export default {
  name: "component-name",
  components: {
      Unity,
    },
    data: {
          ImageBase64: 'Hello this is GeeksforGeeks.'
    },
    methods: {
    ImageStream(value) {
      //document.getElementById("ImageBase64") = value;

    }
    this.$refs.myInstance.message("CameraVK", "KanomchanLinearDirec", 0.1);
  }
};
</script>

<style scoped></style>
