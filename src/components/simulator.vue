<template>
<div>
    Hi Hi Hi
  <unity ref="gameInstance" src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>

  <button v-on:click="onClickF()">Forward</button>
  <button v-on:click="onClickB()">Backward</button>
  <button v-on:click="onClickL()">TurnLeft</button>
  <button v-on:click="onClickR()">TurnRight</button>
  <button v-on:click="onClickS()">Stop</button>
  
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
        onClickF() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0.1");
            this.$refs.gameInstance.message("CameraVK", "KanomchanAngularDirec", "0"); 
        },
        onClickB() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "-0.1");
            this.$refs.gameInstance.message("CameraVK", "KanomchanAngularDirec", "0"); 
        },
        onClickL() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanAngularDirec", "0.2");
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0");
        },
         onClickR() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanAngularDirec", "-0.2");
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0");
        },
        onClickS() {
            this.$refs.gameInstance.message("CameraVK", "KanomchanLinearDirec", "0"); 
            this.$refs.gameInstance.message("CameraVK", "KanomchanAngularDirec", "0"); 
        }

    }

};

</script>

<style scoped></style>
