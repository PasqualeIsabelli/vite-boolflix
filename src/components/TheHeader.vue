<script>
import { store, fetchMovie } from "../store";

export default {
  data() {
    return {
      store,
    }
  },
  methods: {
    fetchMovie,
  }
}
</script>


<template>
  <nav class="navbar navbar-expand-lg nav-bg">
    <div class="container-fluid">
      <a class="navbar-brand ms-3" href="#"><img src="../assets/img/504e88f1a30f968e13f4cdd854aab685.png"></a>
    </div>

    <div class="input-group me-3 size">
      <input type="text" class="form-control" placeholder="Cerca il nome di un film" v-model="store.searchTitle" @keyup.enter="fetchMovie">
      <button class="input-group-text btn btn-light border" @click="fetchMovie"><i class="fa-solid fa-magnifying-glass" style="color: #000000;"></i></button>
    </div>
  </nav>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.nav-bg {
  background-color: $black;

  .size {
    width: 500px;
  }
}
</style>