<template>
    <div class="container-fluid mt-5 mb-5 pt-5 pb-5 text-center bg-col2">
        <div>
            <h4>Let's Dream Big Together</h4>
        </div>
        <div class="d-flex justify-content-center">
            <h1>Explore How can I help you</h1>
        </div>
        
        <div class="d-flex justify-content-around my-5">
            <div class="card" v-for="(element, index) in store.elements2" :key="index">
                <img :src="element.img" alt="">
                <h5>{{ element.name }}</h5>
                <p> {{ element.info }} </p>
                <div class="bord"></div>
                <div class="disc-now-button">
                    <a @click.prevent :href="`${element.url}`">Discover now<i
                            class="fa-solid fa-arrow-right-long ms-2 mt-1"></i></a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from '../data/store';
export default {
    components: {
        name: 'Main2Component',
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
    background-color: $col11;
}

h4 {
    color: $col4;
    padding-bottom: 30px;
}

h1 {
    font-weight: bold;
}

.bord {
    border-bottom: 1px solid $col3;
}

.card {
    background-color: $col1;
    box-shadow: 10px 5px 5px $col5;
    width: 400px;
    transition: 0.8s;

    &:hover {
        transform: scale(1.1);
    }
}

img {
    border: 3%;
    width: 100%;
    margin-bottom: 20px;
}

h5 {
    color: $col1-2;
    font-weight: 700;
}

p {
    color: $col5;
    font-size: 15px;
    padding-top: 10px;
    padding-bottom: 10px;
}

.disc-now-button,
a {
    padding: 20px;
    margin: 0 auto;
    widows: 80%;
    transition-duration: .3s;
    text-decoration: none;
    color: $col4;
    font-weight: bolder;
    padding-top: 20px;

    &:hover {
        background-color: $col4;
        width: 100%;
        height: 100%;
        border-radius: 1%;
        color: $col1;
    }
}
</style>