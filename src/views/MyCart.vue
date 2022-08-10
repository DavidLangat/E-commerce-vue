<template>
<div class="card">
  <img src="./img/onsale1.jpg" alt="" class="Myorder">
  <h3>Laptop</h3>
  <button>Order</button>
</div>
<div class="card">
  <img src="./img/onsale2.jpg" alt="" class="Myorder">
  <h3>Smartphone</h3>
  <button>Order</button>
</div>
<div class="card">
  <img src="./img/onsale3.jpg" alt="" class="Myorder">
  <h3>Headset</h3>
  <button>Order</button>
</div>
<div class="card">
  <img src="./img/onsale4.jpg" alt="" class="Myorder">
  <h3>Smartwatch</h3>
  <button>Order</button>
</div>
<div class="card">
  <img src="./img/onsale5.jpg" alt="" class="Myorder">
  <h3>HDD</h3>
  <button>Order</button>
</div>
</template>
<style scoped>
*{
  color: rgb(0, 240, 248);
}
h3{
  margin-left: 10px;
  float: left;
}
.card{
  border-radius: 10px;
  padding-top: 20px;
  min-width: 100%;
  min-height: 70px;
  background:  linear-gradient(to top right,rgb(241, 236, 236), #e4d2c5);
  margin-bottom: 20px;
}
.card:hover{
  background:  linear-gradient(to top right,rgb(58, 57, 57), #4b4037);
}
.Myorder{
  margin-left: 20px;
  width: 60px;
  float: left;
  border-radius: 10px;
}
button{
  margin-top: 15px;
  border-radius: 10px;
  border: none;
  min-width: 80px;
  min-height: 20px;
  float: right;
  margin-right: 10px;
  background:  linear-gradient(to top right,rgb(236, 59, 59), #161311);
}
button:hover{
  background:  linear-gradient(to top right,rgb(0, 26, 255), #c4bfbb);
}
</style>
