<template>
  <div class="about">
    <h1>About Us</h1>
    <div class="wrapper">
  <div class="blog_post">
    <div class="img_pod">
      <img src="./img/delivery.jpg" alt="random image">
    </div>
    <div class="container_copy">
      <h2>Our Service</h2>
    <h3>We are the largest online shop in the country, with the widest range of products from electronics to clothes and the fastest free delivery.</h3>
    </div>
  </div>
</div>
  </div>
</template>
<style scoped>
.about{
  min-width: 100vw;
  min-height: 50vh;
}
.del{
  width: 50%;
  float: left;
  border-radius: 10px;
}
h3{
  padding: 20px;
  margin-top: 10px;
  font-family: 'Courier New', Courier, monospace;
}
/* my style */
.wrapper {
  height: 100%;
  width: 100%;
  height: 100vh;
}

.blog_post {
  position: relative;
  padding: 6rem 3rem 6rem 6rem;
  background: #fff;
  max-width: 400px;
  border-radius: 10px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  box-shadow: 1px 1px 2rem rgba(0, 0, 0, 0.3);
}

.img_pod {
  height: 110px;
  width: 110px;
  background: linear-gradient(90deg, #ff9966, #ff5e62);
  z-index: -1;
  box-shadow: 1px 1px 2rem rgba(0, 0, 0, 0.3);
  border-radius: 100%;
  position: absolute;
  left: -50px;
  top: 10px;
  transform: translateY(-50%);
}

img {
  height: 100px;
  width: 100px;
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 100%;
  box-shadow: 1px 1px 2rem rgba(0, 0, 0, 0.3);
}

h3 {
  margin: 0 0 0.5rem 0;
  color: #999;
  font-size: 1.25rem;
}

h1 {
  margin: 0 0 1rem 0;
  font-size: 2.5rem;
  letter-spacing: 0.5px;
  color: #333;
}

p {
  margin: 0 0 4.5rem 0;
  font-size: 1.5rem;
  color: #333;
}

.btn_primary {
  border: none;
  outline: none;
  background: linear-gradient(90deg, #ff9966, #ff5e62);
  padding: 1.5rem 2rem;
  border-radius: 50px;
  color: white;
  font-size: 1.2rem;
  box-shadow: 1px 10px 2rem rgba(255, 94, 98, 0.5);
  transition: all .2s ease-in;
  text-decoration: none;
}

.btn_primary:hover {
  box-shadow: 0px 5px 1rem rgba(255, 94, 98, 0.5);
}
</style>
<script>
export default {

  data () {
    return {
      name: 'Vue.js'
    }
  },
  methods: {
    greet (event) {
      // `this` inside methods points to the current active instance
      alert(`Hello ${this.name}!`)
      // `event` is the native DOM event
      if (event) {
        alert(event.target.tagName)
      }
    }
  }
}
</script>
