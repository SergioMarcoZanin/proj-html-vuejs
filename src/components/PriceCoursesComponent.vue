<template>
    <div class="container-fluid bg-col2 mt-5 mb-5 pt-5 pb-5">
        <div class="text-center">
            <h4>Let's Dream Big Together</h4>
        </div>
        <div class="text-center">
            <h1>Explore How can I help you</h1>
        </div>
        <div class="d-flex justify-content-around py-5 gap-1">
            <div class="carddd container" v-for="(card, index) in store.cards" :key="index">
                <img :src="card.img" alt="">
                <div class="cost"> {{ card.price }} </div>
                <h5>{{ card.info1 }}</h5>
                <div class="rest">
                    <span><i class="fa-solid fa-file-lines me-2"></i></span>
                    <span class="">{{ card.lessons }} Lessons</span>
                    &nbsp;
                    <span><i class="fa-solid fa-user me-2"></i></span>
                    <span>{{ card.Students }} Students</span>
                </div>
            </div>
        </div>
        <div class="text-center pt-5">
            <p>Take the control of their life back and start doing things to make their dream come true.<br><a
                    class="hover-underline-animation" @click.prevent href="#nogo">View all courses<i
                        class="fa-solid fa-arrow-right-long ps-2"></i></a>
            </p>
        </div>
    </div>
</template>

<script>
import { store } from '../data/store';
export default {
    components: {
        name: 'PriceCoursesComponent',
    },
    data: function () {
        return {
            store,
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/mixins' as *;
@use '../assets/partials/variables' as *;

.bg-col2 {
    background-color: $col1;
}

h4 {
    color: $col4;
    padding-bottom: 30px;
}

h1 {
    font-weight: bold;
}


h5 {
    text-align: center;
    color: $col1;
}

img {
    border-radius: 7px;
    width: 340px;
}

.cost {
    padding: 20px;
    color: $col16;
    font-size: 25px;
    font-weight: bold;
    margin-top: -180px;
}

.rest {
    text-align: center;
    color: $col1;
}

p {
    font-size: 20px;
    color: $col5;

    a {
        text-decoration: none;
        color: $col1-2;
    }
}

.hover-underline-animation {
    display: inline-block;
    position: relative;
    cursor: pointer;
}

.hover-underline-animation:after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color: $col1-2;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover:after {
    transform: scaleX(1);
    transform-origin: bottom left;
}
</style>