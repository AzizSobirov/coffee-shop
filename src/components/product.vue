<template>
    <section id="product">
        <b>Popular Product</b>
        <h2>Coffee popular Product</h2>
        <ul>
            <li v-for="(product,index) in products" :key="index">
                <img :src="require('../assets/product-img.png')" :alt="product.title">
                <span>
                    <b v-if="product.stars === 4">Coffee
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="far fa-star"></i>
                    </b>
                    <b v-if="product.stars === 4.5">Coffee
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </b>
                    <b v-if="product.stars === 5">Coffee
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </b>
                    <h3>{{product.title}}</h3>
                    <p v-html="product.price"></p>
                </span>
                <div class="as_btn">
                    <a href="#"><i class="far fa-shopping-cart"></i> Add to cart</a>
                </div>
            </li>
        </ul>
        <div class="as_btn">
            <a href="#">View Products</a>
        </div>
        <div class="bx">
            <img :src="require('../assets/coffee-machine.png')">
            <span>
                <h2>Coffee machine, buy for home</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum aut perferendis ratione fuga rem, nulla non repellendus obcaecati aspernatur expedita nobis doloribus inventore sint saepe quia in! Incidunt possimus eum numquam. Maiores illum aut doloremque.</p>
                <div class="as_btn">
                    <a href="#">Discover now</a>
                </div>
            </span>
        </div>
    </section>
</template>
<script>
export default {
    name:'Product',
    data(){
        return{
            products: [
                {
                    stars:4,
                    title:'Brazil coffee gred',
                    price:'Price - <b>$320.00/</b> $358'
                },
                {
                    stars:4.5,
                    title:'Brazil coffee gred',
                    price:'Price - <b>$310.00/</b> $328'
                },
                {
                    stars:5,
                    title:'Brazil coffee gred',
                    price:'Price - <b>$344.00/</b> $358'
                },
            ]
        }
    }
}
</script>