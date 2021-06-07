<template>
  <div id="app">
    <div class="container">
      <header>
        <HeaderNavbar />
      </header>
      <section>
        <div class="row">
          <div class="col-3">
            <SearchForm />
          </div>
          <div class="col-9">
            <ArticlesDisplay />
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>

import HeaderNavbar from './components/HeaderNavbar.vue'
import SearchForm from './components/SearchForm.vue'
import ArticlesDisplay from './components/ArticlesDisplay.vue'

export default {
  name: 'App',
  components: {
    HeaderNavbar,
    SearchForm,
    ArticlesDisplay
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
