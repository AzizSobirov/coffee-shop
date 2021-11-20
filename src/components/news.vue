<template>
    <section id="news">
        <b>Testimonial</b>
        <h2>Our latest news</h2>
        <ul>
            <li v-for="letter in news" :key="letter">
                <img :src="require('../assets/feature-img'+letter.id+'.png')" :alt="letter.title">
                <span>
                    <p v-html="letter.who"></p>
                    <p>{{letter.time}}</p>
                </span>
                <h3>{{letter.title}}</h3>
                <b>See more <i class="far fa-arrow-right"></i></b>
            </li>
        </ul>
    </section>
</template>
<script>
export default {
    name:'News',
    data() {
        return {
            news:[
                {
                    id:1,
                    who:'<b>By:</b> rasaline',
                    time:'23.01.2021',
                    title:'Ideal cocktails from barmen....'
                },{
                    id:2,
                    who:'<b>By:</b> rasaline',
                    time:'23.01.2021',
                    title:'Ideal cocktails from barmen....'
                },{
                    id:3,
                    who:'<b>By:</b> rasaline',
                    time:'23.01.2021',
                    title:'Ideal cocktails from barmen....'
                }
            ]
        }
    },
}
</script>