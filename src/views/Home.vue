<template>
  <div class="container mx-auto flex pt-10 lg:pt-20 px-3 flex-col lg:flex-row">
    <div class="content basis-full lg:basis-1/2 mb-10 lg:mb-0">
      <p class="title-section pb-5">About</p>
      <h1 class="title-content mb-10">Dont Forget About Your Journey</h1>
      <p class="description leading-8">
        Remember yourself or your friend about tasks, event, birthday and much
        more in your discord server. Easy to use for everyone
      </p>
      <div class="button-group mt-16">
        <RouterLink
          to="/login"
          class="link-nav button-login rounded-lg py-3 px-2 mr-5"
          >Get Started</RouterLink
        >
        <RouterLink
          to="/login"
          class="link-nav btn-features rounded-lg border-solid border-2 py-3 px-2 mr-5"
          >See Features</RouterLink
        >
      </div>
    </div>
    <div class="image-hero basis-full lg:basis-1/2">
      <img :src="image" class="block mx-auto" alt="" />
    </div>
  </div>
</template>

<script>
import { RouterLink } from "vue-router";
import Hero from "../assets/images/hero.png";

export default {
  data() {
    return {
      image: Hero,
    };
  },
};
</script>

<style>
.title-section {
  color: rgb(6 182 212);
}

.title-content {
  color: #fff;
  font-size: 30px;
  font-weight: 600;
}

.description {
  color: #fff;
}

.image-hero img {
  width: 400px;
  justify-content: center;
}

.button-login {
  background-color: rgb(6 182 212);
  color: #fff;
}

.btn-features {
  color: #fff;
  border-color: rgb(6 182 212);
}

@media (min-width: 1024px) {
  .image-hero img {
    width: 500px;
    justify-content: center;
  }
}
</style>
