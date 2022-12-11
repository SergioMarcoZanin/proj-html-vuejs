<template>
  <div class="container-fluid mt-5 pt-5 pb-5 text-center bg-col">
    <div>
      <h4>Let's Dream Big Together</h4>
    </div>
    <div class="d-flex justify-content-center">
      <h1>We are pioneers of the digital approach, using leading-edge technology to simplify procedures and apply
        executive coaching in the new age of digitalization.</h1>
    </div>
    
    <div class="d-flex container-fluid justify-content-around mt-5 pt-5 pb-3 row gap-5">
      <div class="card-info pt-2" v-for="(element, index) in store.elements" :key="index">
        <img :src="element.img" alt="">
        <h5>{{ element.name }}</h5>
        <p> {{ element.info }} </p>
      </div>
    </div>
    <div class="d-flex justify-content-around align-items-center pt-5 mt-5"></div>
    <span class="button2">
      <a class="" href="#nogo">Get started today</a>
    </span>
    <span class="button">
      <a class="text-white" href="#nogo">Get started today</a>
    </span>
  </div>
</template>

<script>
import { store } from '../data/store';
export default {
  components: {
    name: 'FeaturesCoursesComponent',
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

.bg-col {
  background-color: $col1;
}

h4 {
  color: $col4;
  padding-bottom: 30px;
}

h1 {
  color: $col1-2;
  font-weight: bold;
}

h5 {
  color: $col1-2;
  font-weight: 500;
  font-size: 20px;
  padding-top: 5px;
}

.card-info {
  width: 400px;
  height: 230px;
  background-color: $col1;
  border-radius: 3%;
}

img {
  width: 100px;
}

.button {
  margin-right: 40px;
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

.button2 {
  margin-right: 40px;
  font-weight: bold;
  padding: 18px 18px;
  border: 1px solid $col3;
  background-color: $col1;
  border-radius: 4%;
  width: 25%;
  transition: .2s;

  &:hover {
    background-color: $col1-1;
  }

  a {
    color: $col4;
    text-decoration: none;
  }
}

p {
  color: $col5;
}
</style>