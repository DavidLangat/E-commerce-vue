<template>
<h4><img src="./img/offer.jpg" alt=""></h4>
<img class="onsale" src="./img/onsale7.jpg" alt="">
   <img class="onsale" src="./img/onsale8.jpg" alt="">
   <img class="onsale" src="./img/onsale9.jpg" alt="">
   <img class="onsale" src="./img/onsale10.jpg" alt="">
   <img class="onsale" src="./img/onsale11.jpg" alt="">
   <img class="onsale" src="./img/onsale12.jpg" alt="">

</template>
<script>
export default {
  name: 'MyOffer'
}
</script>
<style scoped>
img{
    border-radius: 20px;
    width: 40%;
    margin: 5px;
}
.onsale{
    margin-bottom: 3%;
    width: 29%;
    border-radius: 10px;
}
.onsale:hover{
    width: 25%;
        border-radius: 50px;
        border:5px solid rgb(13, 13, 88);
}

</style>
