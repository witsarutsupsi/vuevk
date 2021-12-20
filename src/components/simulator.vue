<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>
  <p> id="ImageBase64">10</p>
</div>
</template>

<script>
import Unity from 'vue-unity-webgl'

export default {
  name: "component-name",
  components: {
      Unity,
    },
    data() {
        return {
            ImageBase64: "",
        };
    },
    methods: {
        onClick () {
            this.$refs.myInstance.message("CameraVK", "KanomchanLinearDirec", "0.1")
        },
        
        ImageStream : function(value){
            this.ImageBase64 = value;
        }
    },
};

</script>

<style scoped></style>
