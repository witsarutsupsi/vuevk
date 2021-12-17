<template>
<div>
    Hi Hi Hi
  <unity src="static/Build/VK Build.json" width="1000" height="600" unityLoader="static/Build/UnityLoader.js"></unity>  
  

</div>
</template>

<script>
import Unity from 'vue-unity-webgl'

export default {
  name: "component-name",
  components: {
      Unity,
    },
};
</script>

<style scoped></style>
