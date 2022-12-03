<template>
  <nav class="nav bg-black px-2 sm:px-4 py-2.5">
    <div class="container flex flex-wrap items-center justify-between mx-auto">
      <div class="logo flex items-center">
        <p class="logo-style">ReminderBot</p>
      </div>
      <button
        data-collapse-toggle="navbar-default"
        type="button"
        class="inline-flex items-center p-2 ml-3 text-sm text-white-500 rounded-lg md:hidden hover:bg-white-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
        aria-controls="navbar-default"
        aria-expanded="false"
        @click="navMenu"
      >
        <svg
          class="w-6 h-6"
          aria-hidden="true"
          fill="white"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
      <div
        class="nav-link w-full md:block md:w-auto"
        :class="{ block: expand, hidden: hidden }"
      >
        <ul
          class="flex flex-col p-4 mt-4 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700"
        >
          <li>
            <RouterLink to="/" class="link-nav block py-3 pl-3 my-2"
              >Home</RouterLink
            >
          </li>
          <li>
            <RouterLink to="/" class="link-nav block py-3 pl-3 my-2"
              >Features</RouterLink
            >
          </li>
          <li>
            <RouterLink to="/" class="link-nav block py-3 pl-3 my-2"
              >Support</RouterLink
            >
          </li>
          <li>
            <RouterLink
              to="/"
              class="link-nav button-login rounded-lg block py-3 pl-3 pr-3 my-2"
              >Login</RouterLink
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
import { RouterLink } from "vue-router";

export default {
  name: "Navbar",
  data() {
    return {
      expand: false,
      hidden: true,
    };
  },
  methods: {
    navMenu() {
      if (this.expand == false && this.hidden == true) {
        this.expand = true;
        this.hidden = false;
      } else {
        this.expand = false;
        this.hidden = true;
      }
    },
  },
};
</script>

<style>
.logo-style {
  color: #fff;
  font-weight: 600;
  font-size: 21px;
}

.nav .link-nav {
  color: #fff;
  font-size: 18px;
}

.button-login {
  background-color: rgb(6 182 212);
}
</style>
