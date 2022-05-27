<template>
  <main class="home-page container">
    <h1>Forms Available</h1>
    <div class="card">
      <h5 class="card-header d-flex justify-content-between align-items-center">
        Form A <a href="#" class="btn btn-primary">OPEN</a>
      </h5>

      <div class="card-body">
        <h5 class="card-title">Special title treatment</h5>
        <p class="card-text">
          With supporting text below as a natural lead-in to additional content.
        </p>
      </div>
    </div>
    <div class="card">
      <h5 class="card-header d-flex justify-content-between align-items-center">
        <span class="me-auto">Form B</span>
        <router-link class="mx-2" :to="{ path: '/about' }"
          ><button class="btn btn-secondary" @click="openForm">
            VERSIONS
          </button></router-link
        >
        <button
          type="button"
          class="btn btn-danger mx-2"
          data-bs-toggle="tooltip"
          data-bs-placement="top"
          title="Checked out by 'JASON SANDERS' on April 24, 2022"
          ref="info"
        >
          CHECKED OUT
        </button>
        <button type="button" class="btn btn-success mx-2">CHECK OUT</button>
        <router-link class="ms-2" :to="{ path: '/settings' }"
          ><button class="btn btn-primary" @click="openForm">
            OPEN
          </button></router-link
        >
      </h5>

      <div class="card-body">
        <h5 class="card-title">Special title treatment</h5>
        <p class="card-text">
          With supporting text below as a natural lead-in to additional content.
        </p>
      </div>
    </div>
  </main>
</template>

<script>
import { Tooltip } from "bootstrap";

export default {
  setup() {
    function openForm() {
      console.log("clicked");
    }

    return { openForm };
  },
  mounted() {
    new Tooltip(this.$refs.info);
  },
};
</script>

<style>
</style>