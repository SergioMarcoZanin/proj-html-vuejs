<template>
    <div class="bg3 container-fluid justify-content-between mt-5 pt-5 mb-5 pb-5">
        <div class="d-flex col-12">
            <div class="bg-video">
                <img src="src\assets\img\home-business-video-poster-670x450.jpg" alt="">
                <div class="yt">
                    <a href=""><img src="src\assets\img\icon-youtube-play.png"
                            alt=""></a>
                </div>
            </div>
            <div class="container question">
                <h1>To Thive In Business Today, You'll Need a Good Plan</h1>
                <div v-for="(element, index) in store.elements3" :key="index">
                    <div class="small-container">
                        <div class="question-box">
                            <div class="question-text">
                                <h4>{{ element.name }}</h4>
                            </div>
                            <div class="question-hr"><i class="fa-regular fa-circle-down"></i></div>
                            <div class="hidden">
                                {{ element.info }}
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from '../data/store';
export default {
    components: {
        name: 'VideoYoutubeComponent',
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

.bg3 {
    background-image: url(../assets/img/background-map-dots-top-right-transparent.png);
    background-size: cover;
    background-color: $col1-1;
}

.bg-video {
    position: relative;
    padding-top: 100px;
    width: 100%;
    border-radius: 50px;
}

img {
    border-radius: 10px;
}

.yt {
    margin-top: -250px;
    margin-left: 280px;
}

h1 {
    padding-top: 90px;
    padding-bottom: 40px;
    color: $col1;
    font-weight: bold;
    font-size: 55px;
}

.question {
    margin-bottom: 60px;
}

.question .small-container {
    border-bottom: 1px solid rgb(162, 162, 162);
}

.question-hr i {
    padding-top: 30px;
    font-size: 25px;
    color: $col1;
}

.question-text {
    font-weight: bold;
}

.question-box {
    border-top: 1px solid rgb(162, 162, 162);
    position: relative;
    min-height: 30px;
    align-items: center;
    padding: 20px 0;
}

.question-text h4 {
    margin: 10px;
    margin-left: 50px;
    color: $col1;

    &:hover {
        transition: 0.5s;
        color: $col4;
    }
}

.question-box i {
    position: absolute;
    top: 2px;
    right: 10px;
    transition: 0.8s;
}

.question-box:hover i {
    rotate: 180deg;
    padding-left: 30px;
    padding-bottom: 30px;
    color: $col4;
}

.question-box .hidden {
    display: none;
}

.question-box:hover .hidden {
    display: block;
    font-size: 15px;
    margin-left: 50px;
    margin-top: 20px;
    width: 80%;
    transition: 0.8s;
    color: $col1;
    line-height: 1.5rem;
}
</style>