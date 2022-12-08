<template>
  <div class="bg-foot container-fluid d-flex justify-content-around mt-5 pt-5">
    <!-- left -->
    <div>
      <p class="fw-bold fs-4">Adress</p>
      <ul>
        <li v-for="(element, index) in store.addresses" :key="index"> <a @click.prevent href="">{{ element.text }}</a>
        </li>
      </ul>
      <!--social icons -->
      <div>
        <a @click.prevent href=""> <i class="fs-4 pe-5 fa-brands fa-square-facebook"> </i> </a>
        <a @click.prevent href=""> <i class="fs-4 pe-5 fa-brands fa-instagram"> </i></a>
        <a @click.prevent href=""> <i class="fs-4 pe-5 fa-brands fa-twitter"> </i></a>
        <a @click.prevent href=""> <i class="fs-4 pe-5 fa-brands fa-linkedin"> </i></a>
      </div>
    </div>
    <!-- right -->
    <div class="d-flex">
      <div class="px-4">
        <p class="fw-bold fs-4">Explore</p>
        <ul>
          <li v-for="(element, index) in store.info" :key="index"><a @click.prevent href=""> {{ element.inf }} </a></li>
        </ul>
      </div>
      <div class="px-4 p-mio">
        <ul class="special-padding">
          <li v-for="(element, index) in store.NotDefined" :key="index"> <a @click.prevent href=""> {{ element.moreInfo
          }}</a>
          </li>
        </ul>
      </div>
      <div class="px-4">
        <p class="fw-bold fs-4">Information</p>
        <ul>
          <li v-for="(element, index) in store.Explore" :key="index"><a @click.prevent href=""> {{ element.Exp }} </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
  <div class="bg-foot pt-5">
    <p class="fw-bold rights">&copy; 2020 MaxCoach. All Rigts Reserved</p>
    <a href="#up"> <i class="fa-solid fa-arrow-up anchor"></i></a>
  </div>
</template>

<script>
import { store } from '../data/store';
export default {
  components: {
    name: 'FooterComponent',
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

.bg-foot {
  background-color: $col21;
}

ul {
  padding: 0;
}

ul li {
  list-style: none;
  padding: 8px 0px;
  font-weight: bold;
}

a {
  text-decoration: none;
  color: $col5;

  &:hover {
    color: $col4;
  }
}

p {
  color: $col1-2;
}

.rights {
  color: $col5;
  text-align: center;
  padding: 40px 0px;
}

.special-padding {
  padding-top: 50px;
}

.p-mio {
  padding-top: 2px;
}

.anchor {
  font-size: 2.1rem;
  padding: 18px;
  position: relative;
  left: 95%;
  bottom: 57px;
  background: $col4;
  color: $col1;
  border-radius: 50%;
  width: 60px;
  height: 65px;
}
</style>
