<template>
  <header class="sticky-top position-sticky">
    <div
      class="container-fluid d-flex align-items-center align-content-center m-auto justify-content-between gap-3 py-2"
      id="nav">
      <div class=" d-flex justify-content-between align-items-center">
        <div> <img class="w-50 ms-5 pt-1" src="src\assets\img\dark-logo.png" alt=""> </div>
      </div>
      <div class="">
        <ul class="d-flex gap-5 list-unstyled pt-2 m-0 position-relative uldprdwn">
          <li v-for="i in store.NavList"><a class="dropdwn text-decoration-none hover-underline-animation" href="#"
              @click="i.hover = !i.hover">{{ i.text }} <i class="fa-solid fa-chevron-down"></i></a>
            <Transition name="move">
              <div class="dropdwn-menu position-absolute p-4 d-flex bg-white" v-if="i.hover">
                <ul class="list-unstyled row">
                  <li class="col-5  text-capitalize" v-for="(j, index) in i.link" :key="index"
                    :class="{ 'hot': j.hot, 'new': j.new }">
                    {{ j.title }}
                  </li>
                </ul>
              </div>
            </Transition>
          </li>
          <div class="ms-5">
            <select class="form-select text-uppercase border-0" aria-label="Language">
              <option v-for="(element, index) in store.LanguageList" :key="index">{{ element.item }}</option>
            </select>
          </div>
          <a href="#nogo"><i class="fa-regular fa-circle-user text-black fs-5 align-self-center"></i></a>
        </ul>
      </div>
      <div>
        <div class="input-group">
          <div class="search">
            <input type="text" name="" placeholder="Search...">
            <a href="#nogo"><i class="fa-solid fa-magnifying-glass text-secondary text-dark fs-5"></i></a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import { store } from '../data/store';
export default {
  components: {
    name: 'HeaderComonent',
  },
  data: function () {
    return {
      store,
    };
  },
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/mixins' as *;
@use '../assets/partials/variables' as *;

header {
  background-color: $col1;
  
}

a {
  color: $col1-2;
  font-weight: 400;
  font-size: 18px;
  color: $col1-2;
  transition: 0.5s;

  &:hover {
    color: $col1-1;
  }

  i {
    font-size: 10px;
  }
}

select {
  margin-top: -7px;
}

.search {
  padding: 20px 20px;
  background-color: $col1;
  border-left: 2px solid $col3;
}

input {
  border: 0;
  padding: 0;
  width: 8rem;
  outline: none;
}

// dropdown menu
.uldprdwn {
  height: 100%;
}

.dropdwn {
  height: 100%;
}

.dropdwn:hover {
  transition: 0.25s ease;

  .fa-chevron-down {
    transform: rotate(180deg);
  }
}

.move-enter-active,
.move-leave-active {
  transition: all 0.5s ease;
}

.move-enter-from,
.move-leave-to {
  opacity: 0;
  transform: translateY(30px);
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
  background-color: $col1-1;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover:after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>
