<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <nuxt-link  class="navbar-brand" to="/">NUXTY</nuxt-link>
      <button
        @click="navToggleAction()"
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" :class="[navToggle === true ? 'show' : '']" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/">Home</nuxt-link>
          </li>
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/about">About</nuxt-link>
          </li>
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/service">Service</nuxt-link>
          </li>
          <li class="nav-item active">
            <nuxt-link class="nav-link" to="/contact">Contact</nuxt-link>
          </li>
          
        </ul>
        <form class="form-inline my-2 my-lg-0">
          <input
            class="form-control mr-sm-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
          <button class="btn btn-outline-success my-2 my-sm-0" type="submit">
            Search
          </button>
        </form>
      </div>
    </nav>
</template>

<script>
export default {
  data(){
    return{
      navToggle: false
    }
  },
  methods: {
    navToggleAction(){
      this.navToggle == true ? this.navToggle = false : this.navToggle = true
    }
  }
}
</script>

<style lang="scss" scoped></style>
