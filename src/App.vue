<script setup>
// import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <header>
    <div class="container">
      <div class="row">
        <div class="col text-center">
          <h1>header</h1>
        </div>
      </div>
    </div>
  </header>
  <main>
    <div class="container">
      <div class="row">
        <div class="col text-center">
          <h2>main</h2>
        </div>
      </div>
    </div>
  </main>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col text-center">
          <h2>footer</h2>
          <span class="text-body-tertiary py-3 m-2">
            <font-awesome-icon :icon="['fas', 'fa-user-secret']" />
            AP
          </span>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
h1 {
  color: red;
}
</style>
