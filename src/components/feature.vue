<template>
    <section id="feature">
        <ul>
            <li v-for="(card,index) in cards" :key="index">
                <span>
                    <b>0{{card.id}}</b>
                    <p>{{card.title}}</p>
                </span>
                <img :src="require('../assets/feature-img'+card.id+'.png')" :alt="card.title">
            </li>
        </ul>
        <div class="history">
            <div class="img-bx">
                <img :src="require('../assets/feature-img1.png')" alt="">
                <img :src="require('../assets/feature-img2.png')" alt="">
                <img :src="require('../assets/feature-img4.png')" alt="">
            </div>
            <span>
                <b>Our history</b>
                <h2>Create a new story with us</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. <br> Soluta exercitationem ratione nemo, adipisci autem nobis dolorem ea quod quam deserunt. Laboriosam quo ducimus consequatur aut reiciendis sequi, fugit, quos, at repellendus possimus similique saepe enim!</p>
            </span>
        </div>
    </section>
</template>

<script>
export default {
    name:'Feature',
    data(){
        return{
            cards: [
                {id:1,title:'Best Coffee Flavour'},
                {id:2,title:'Place to get lost'},
                {id:3,title:'Proper roesting'},
            ]
        }
    }
}
</script>