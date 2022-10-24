<template>
  <div>
    <ul class="flex">
      <li v-for="item in navMenu" :key="'item_' + item.name" class="me-2">
        <router-link :to="item.to">
          <button>{{ item.name }}</button>
        </router-link>
      </li>
    </ul>
  </div>
</template>

<script>
import NavMenuItems from "./navMenu/NavMenuItems.js";

export default {
  name: "NavMenu",

  computed: {
    navMenu() {
      return NavMenuItems;
    },
  },
};
</script>

<style scoped>
ul {
  list-style-type: none;
}

.flex {
  display: flex;
}

.flex-wrap {
  flex-wrap: wrap;
}
</style>