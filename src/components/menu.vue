<template>
    <section id="menu">
        <b>Menu</b>
        <h2>Coffee popular menu</h2>
        <ul>
            <li v-for="(product,index) in products" :key="index">
                <img :src="require('../assets/feature-img'+product.id+'.png')" :alt="product.title">
                <h3>{{product.title}}</h3>
                <b v-html="product.price"></b>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name:'Menu',
    data() {
        return {
            products:[
                {
                    id:1,
                    title:'Americano rosted gred',
                    price:'<b>$12:00</b>'
                },{
                    id:1,
                    title:'Americano rosted gred',
                    price:'<b>$10:00</b>'
                },{
                    id:2,
                    title:'Americano rosted gred',
                    price:'<b>$12:00</b>'
                },{
                    id:1,
                    title:'Americano rosted gred',
                    price:'<b>$15:00</b>'
                },{
                    id:2,
                    title:'Americano rosted gred',
                    price:'<b>$11:00</b>'
                },{
                    id:1,
                    title:'Americano rosted gred',
                    price:'<b>$8:00</b>'
                },{
                    id:2,
                    title:'Americano rosted gred',
                    price:'<b>$9:00</b>'
                },{
                    id:1,
                    title:'Americano rosted gred',
                    price:'<b>$12:50</b>'
                }
            ]
        }
    },
}
</script>