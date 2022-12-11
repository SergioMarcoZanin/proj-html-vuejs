<template>
    <div class="bgg container-fluid mt-5 pt-5 pb-5">
        <div class="text-center">
            <h4>Let's Dream Big Together</h4>
        </div>
        <div class="text-center">
            <h1>Explore How can I help you</h1>
        </div>
        <div class="d-flex container-fluid justify-content-around mt-5 pt-5 row gap-3">
            <div class="card2" v-for="(element, index) in store.elements4" :key="index">
                <div class="card2-1">
                    <p>{{ element.cap }}</p>
                    <h5> {{ element.name }} </h5>
                </div>
                <div class="card3">
                    <span class="num"> {{ element.num }} </span>
                    <span class="data"> {{ element.data }} </span>
                    <span class="button"> {{ element.buttonn }} </span>
                </div>
            </div>
        </div>
        <div class="text-center pt-5 pb-5 mt-5">
            <p>Excited about our event? <a class="hover-underline-animation" @click.prevent href="#nogo">View all
                    events<i class="fa-solid fa-arrow-right-long ps-2"></i></a>
            </p>
        </div>
    </div>
</template>

<script>
import { store } from '../data/store';
export default {
    components: {
        name: 'CityCoursesComponent',
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

.bgg {
    background-color: $col1;
}

h4 {
    color: $col4;
    padding-bottom: 30px;
}

h1 {
    font-weight: bold;
}

.card2 {
    width: 600px;
    height: 200px;

    p {
        color: $col5;
    }

    h5 {
        font-size: 22px;
        font-weight: 800;
        color: $col1-2;
    }
}

.card2-1 {
    margin-top: 30px;
    margin-left: 20px;
}

.card3 {
    width: 300px;
    height: 200px;
    margin-left: 320px;
}

.num {
    margin-right: 10px;
    color: $col4;
    font-weight: bold;
    font-size: 40px;
}

.data {
    color: $col1-2;
    font-weight: 500;
    font-size: 30px;
}

.button {
    margin-left: 10px;
    justify-content: center;
    font-weight: bold;
    padding: 10px 18px;
    background-color: $col4;
    border-radius: 4%;
    transition: .2s;
    color: $col1;

    &:hover {
        background-color: $col1-1;
    }

    a {
        text-decoration: none;
    }
}

p {
    font-size: 20px;
    color: $col5;

    a {
        text-decoration: none;
        color: $col4;
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
    background-color: $col4;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover:after {
    transform: scaleX(1);
    transform-origin: bottom left;
}
</style>