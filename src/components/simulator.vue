<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>
  <div id="ImageBase64" ref="ImageBase64">12</div>
  <button v-on:click="onClick()">Click Forward</button>
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
        //ImageStream (value){
            //this.$refs.ImageBase64.innerText = = value;    
        //},
        onClick () {
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0.1")
            
        },
        message(gameObject, method, param) {
            if (param === null) {
                param = ''
            }   
            if (this.gameInstance !== null){
                this.gameInstance.SendMessage(gameObject, method, param)
            } else {
                //console.warn('vue-unity-webgl: you\'ve sent a message to the Unity content, but it wasn\t instantiated yet.')
            }
        }
    }
};

</script>

<style scoped></style>
