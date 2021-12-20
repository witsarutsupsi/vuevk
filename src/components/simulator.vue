<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>
   <div id="app2">
	     <div v-text="ImageBase64">10</div>
     </div>
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
        onClick () {
            this.$refs.myInstance.message("CameraVK", "KanomchanLinearDirec", "0.1")
        }
        
        ImageStream(value){
            el: '#app2',
		    data: {
		        ImageBase64: value
		    }
        }
    },
};

</script>

<style scoped></style>
