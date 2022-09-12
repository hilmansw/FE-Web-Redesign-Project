<template>
  <div id="navbar-wrapper">
    <b-navbar toggleable="lg" type="light" class="top-navbar">
      <router-link class="navbar-brand" to="/"
        ><img src="../../assets/img/logo-si.png"
      /></router-link>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="ml-auto align-middle">
          <b-nav-item v-for="menu in menus" :key="menu.id" :to="menu.url">{{
            menu.name
          }}</b-nav-item>
            <b-button
              class="btn-search-circular"
              round
              id="show-btn"
              @click="$bvModal.show('bv-modal-example')"
              ><i class="fa fa-search"
            /></b-button>
        </b-navbar-nav>

        <b-modal id="bv-modal-example" hide-footer>
          <template #modal-title> Cari Berita </template>
          <div class="d-block text-center">
            <b-form-input
              v-model="search"
              @keypress.enter="searchData"
              size="sm"
              class="mr-sm-2 border-1"
              placeholder="tulis kata kunci..."
            >
            </b-form-input>
          </div>
          <b-button class="mt-3" block @click="searchData">Search</b-button>
        </b-modal>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  //data function
  data() {
    return {
      //state menus
      menus: [],

      //state search
      search: "",
    };
  },

  async fetch() {
    //fething menus on Rest API
    await this.$axios.get("/api/web/menus").then((response) => {
      //assign response to state "menus"
      this.menus = response.data.data;
    });
  },

  methods: {
    searchData() {
      this.$router.push({
        name: "search",
        query: {
          q: this.search,
        },
      });
    },
  },
};
</script>

<style>
</style>
