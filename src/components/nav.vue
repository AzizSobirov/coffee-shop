<template>
  <nav id="navbar" :class="{navSticky:active}">
    <ul>
        <li class="active"><a href="#home">Home</a></li>
        <li><a href="#feature">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#reservation">Reservation</a></li>
    </ul>
    <img :src="require('../assets/logo.svg')" alt="">
    <ul>
        <li><a href="#testimonial">Pages</a></li>
        <li><a href="#product">Shop</a></li>
        <li><a href="#footer">Contact</a></li>
        <li><a href="#" class="far fa-search"></a></li>
        <li><a href="#" class="far fa-shopping-cart"></a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name:'Navbar',
  data() {
    return {
      active:false
    }
  },
  mounted(){
    window.document.onscroll = () => {
      let navBar = document.getElementById('navbar');
      window.scrollY > navBar.offsetTop ? this.active = true : this.active = false; 
    }
  }
}
</script>
