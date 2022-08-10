<template>
<h2>Category</h2>
<router-link to="/MyComp"><img src="./img/desktop.png" alt=""></router-link>
<img src="./img/laptop.png" alt="">
<img src="./img/smartphone.png" alt="">
<img src="./img/video-camera.png" alt="">
<img src="./img/joystick.png" alt="">
<img src="./img/vr-glasses.png" alt="">
<img src="./img/router.png" alt="">

</template>
<script>
export default {
  name: 'MyCate'
}
</script>
<style scoped>
img{
    width: 40px;
    margin: 6px;
}
img:hover{
    width: 30px;
    border: 4px solid rgb(33, 2, 145);
    border-radius: 20px;
}

</style>
