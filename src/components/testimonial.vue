<template>
    <section id="testimonial">
        <b>Testimonial</b>
        <h2>Says our customers</h2>
        <ul>
            <li v-for="user in customers" :key="user">
                <div class="content">
                    <img :src="require(`../assets/${user.img}.png`)" alt="">
                    <p>{{user.feedback}}</p>
                </div>
                <div class="info">
                    <span>
                        <h3>{{user.name}}</h3>
                        <p>{{user.hobby}}</p>
                    </span>
                    <b v-if="user.stars === 4">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="far fa-star"></i>
                    </b>
                    <b v-if="user.stars === 4.5">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </b>
                    <b v-if="user.stars === 5">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </b>
                </div>
            </li>
        </ul>
        <div class="footer">
            <span>
                <b>2/{{this.customers.length}} People</b><hr>
            </span>
            <div class="btn">
                <button @click="prev()">
                    <i class="far fa-arrow-left"></i>
                </button>
                <button @click="next()">
                    <i class="far fa-arrow-right"></i>
                </button>
            </div>
        </div>
    </section>
</template>
<script>
export default {
    name:'Testimonial',
    data() {
        return {
            translate:0,
            customers:[
                {
                    img:'user-img1',
                    name:'John Smith',
                    hobby:'Product Designer',
                    stars:5,
                    feedback:'Education WP is a special build for effective education & Learning Management System site. Education WP is the next generation & one of the best education WordPress themes which all the strength of eLearning WP..'
                },{
                    img:'user-img2',
                    name:'Brett Lee',
                    hobby:'User Experience Designer',
                    stars:4.5,
                    feedback:'Education WP is a special build for effective education & Learning Management System site. Education WP is the next generation & one of the best education WordPress themes which all the strength of eLearning WP..'
                },{
                    img:'user-img1',
                    name:'John Smith',
                    hobby:'Product Designer',
                    stars:5,
                    feedback:'Education WP is a special build for effective education & Learning Management System site. Education WP is the next generation & one of the best education WordPress themes which all the strength of eLearning WP..'
                },{
                    img:'user-img2',
                    name:'Brett Lee',
                    hobby:'User Experience Designer',
                    stars:4.5,
                    feedback:'Education WP is a special build for effective education & Learning Management System site. Education WP is the next generation & one of the best education WordPress themes which all the strength of eLearning WP..'
                },{
                    img:'user-img1',
                    name:'John Smith',
                    hobby:'Product Designer',
                    stars:5,
                    feedback:'Education WP is a special build for effective education & Learning Management System site. Education WP is the next generation & one of the best education WordPress themes which all the strength of eLearning WP..'
                },{
                    img:'user-img2',
                    name:'Brett Lee',
                    hobby:'User Experience Designer',
                    stars:4.5,
                    feedback:'Education WP is a special build for effective education & Learning Management System site. Education WP is the next generation & one of the best education WordPress themes which all the strength of eLearning WP..'
                }
            ]
        }
    },
    methods:{
        prev(){
            this.translate-=100
            console.log(this.translate);
            let ul = document.querySelector("#testimonial ul")
            ul.style.transform=`translate(-${this.translate}%)`
            if(this.translate === this.customers.length*100/2){
                this.translate = 0
                ul.style.transform=`translate(0%)`
            }else if(this.translate < 0){
                this.translate = 0
            }
        },
        next(){
            this.translate+=100
            console.log(this.translate);
            let ul = document.querySelector("#testimonial ul")
            ul.style.transform=`translate(-${this.translate}%)`
            if(this.translate === this.customers.length*100/2){
                this.translate = 0
                ul.style.transform=`translate(0%)`
            }
        }
    },
}
</script>