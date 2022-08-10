<template>
<router-link to="/cart"><img src="./views/img/foot.jpg" alt="" class="head"></router-link>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> |
    <router-link to="/MyProfile">Profile</router-link> |
    <router-link to="/order">Order</router-link> |
  </nav>
   <router-link to="/MyCont"><img class="icon" src="./views/img/icon.jpeg" alt=""></router-link>
  <router-view/>
  <footer>

  </footer>
</template>
<script>
export default {
  name: 'app'
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
footer{
  background: darksalmon;
  min-width: 100%;
  min-height: 10vh;
  bottom: 0;
  left: 0;
  position: fixed;
}
.head{
  top: 2;
  right: 0;
  position: fixed;
  width: 30px;
  border-radius: 10px;

}
.head:hover{
  width: 40px;
  border: 3px solid red;
}
.icon{
  bottom: 10%;
  right: 0;
  position: fixed;
  width: 50px;
  border-radius: 20px;

}
.icon:hover{
  width: 60px;
  border-radius: 40px;
  border: 3px solid red;
}
.nav {
  @apply fixed;
  top: 1rem;
  right: 1.25rem;
  z-index: 999;

  &__cart {
    span {
      @apply text-sm font-bold bg-orange text-white py-0 px-1 -ml-2 rounded-full align-top;
    }
  }

  &__cart-close {
    @apply bg-blue text-white py-0 px-1 -ml-2 -mt-3 -mr-3 rounded-full align-top h-8 w-8;
  }
}
</style>
