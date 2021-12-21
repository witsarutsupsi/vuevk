<template>
<div>
    Hi Hi Hi
  <unity ref="gameInstance" src="static/Build/VK Build.json" width="1000" height="600" class="webgl-content" unityLoader="static/Build/UnityLoader.js"></unity>
  <div id="ImageBase64" ref="ImageBase64">12</div>
  <button v-on:click="onClickF()">Click Forward</button>
  <button v-on:click="onClickS()">Click Stop</button>
</div>
</template>

<script>
import Unity from 'vue-unity-webgl'

export default {
    name: "component-name",
    components: {
        Unity,
    },
    props: {},
    created() {},
    data() {
        return {
            vkrun: "0",
        };
    },
    methods: {
        Call_RunProgram(value){
            this.vkrun = value;
            this.$refs.ImageBase64.innerText = vkrun;  
        },
        //Call_RunProgram: function (value) {
            //this.$refs.ImageBase64.innerText = value;  
        //},
        //ImageStream (value){
            //this.$refs.ImageBase64.innerText = value;    
        //},
        onClickF() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0.1");
            //this.$refs.ImageBase64.innerText = 20;   
        },
        onClickS() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0"); 
        }
    }
};

</script>

<style scoped></style>
