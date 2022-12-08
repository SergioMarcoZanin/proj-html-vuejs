<template>
    <div id="up" class="d-flex justify-content-between bg-container container-fluid">
        <div class="space">
            <h3 class="pb-3">New Challenges, New Skills</h3>
            <h1 class="pb-3">Build your own life coaching business</h1>
            <p class="pb-3">
                Whole-Life Business Coaching for committed entrepreneurs
            </p>
            <div class="d-flex button">
                <a class="text-white" href="#nogo">Get started today</a>
            </div>
        </div>
        <div class="img-backgorund"><img src="/img/home-business-hero-avatar.png" alt="Non Trovato">
        </div>
        <div class="menu-comparsa">
            <i class="py-2 fa-solid fa-ruler-combined"></i>
            <i class="py-2 fa-solid fa-life-ring"></i>
            <i class="py-2 fa-solid fa-book"></i>
            <i class="py-2 fa-solid fa-cart-shopping"></i>
        </div>
    </div>
</template>

<script>
export default {
    components: {
        name: 'JumboComponent',
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/mixins' as *;
@use '../assets/partials/variables' as *;

.menu-comparsa {
    z-index: 999;
    display: flex;
    position: fixed;
    flex-direction: column;
    padding: 10px;
    height: 150px;
    background-color: $col1;
    box-shadow: 10px 5px 5px black;
    width: 39px;
    align-items: center;
    margin-left: 1460px;
    margin-top: 120px;
    border-radius: 5px;
}

.bg-container {
    background-color: $col11;
}

.space {
    padding-top: 150px;
    padding-left: 50px;
}

.img-backgorund {
    background-image: url(./img/home-business-hero-global-image.png);
    width: 100%;
    height: 100%;
    margin-bottom: 0px;

    img {
        margin-top: 50px;
        width: 500px;
    }
}

h3 {
    color: $col4;
}

h1 {
    text-transform: uppercase;
    color: $col1-2;
    font-size: 4rem;
    font-weight: bold;
}

p {
    color: $col5;
    font-weight: 500;
    font-size: 20px;
}

.button {
    justify-content: center;
    font-weight: bold;
    padding: 18px 18px;
    background-color: $col4;
    border-radius: 4%;
    width: 25%;
    transition: .2s;

    &:hover {
        background-color: $col1-1;
    }

    a {
        text-decoration: none;
    }
}
</style>