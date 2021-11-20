<template>
  <main>
    <Nav/>
    <Home/>
    <Feature/>
    <Product/>
    <Menu/>
    <Testimonial/>
    <Reservation/>
    <News/>
    <Footer/>
  </main>
</template>

<script>
import Nav from './components/nav.vue'
import Home from './components/home.vue'
import Feature from './components/feature.vue'
import Product from './components/product.vue'
import Menu from './components/menu.vue'
import Testimonial from './components/testimonial.vue'
import Reservation from './components/reservation.vue'
import News from './components/news.vue'
import Footer from './components/footer.vue'
import './css/style.css'

export default {
  name: 'App',
  components: {
    Nav,Home,Feature,Product,Menu,Testimonial,Reservation,News,Footer
  }
}
</script>