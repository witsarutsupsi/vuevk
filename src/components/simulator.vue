<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>  
  <p id="ImageBase64">0</p>
</div>
</template>

<script>
import Unity from 'vue-unity-webgl'

export default {
  name: "component-name",
  components: {
      Unity,
    },
    
    methods: {
    ImageStream(value) {
      document.getElementById("ImageBase64") = value;
    }
    document.getElementById("ImageBase64") = 10;
    //this.$refs.myInstance.message("CameraVK", "KanomchanLinearDirec", 0.1);
  }
};
</script>

<style scoped></style>
