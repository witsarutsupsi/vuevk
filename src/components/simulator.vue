<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>
  <p id="ImageBase64">10</p>
  <div id="ImageBase64" ref="ImageBase64">{{ message }}</div>
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
          message:"Welcome"
    },
    methods: {
        onClick () {
            this.$refs.myInstance.message("CameraVK", "KanomchanLinearDirec", "0.1")
            
        },
        ImageStream : function(value){
            this.$refs.ImageBase64.innerText = value
        }
    },
};

</script>

<style scoped></style>
