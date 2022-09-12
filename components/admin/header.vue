<template>
  <nav class="main-header navbar navbar-expand navbar-white navbar-light">
    <!-- Left navbar links -->
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" data-widget="pushmenu" href="javascript:void(0)" role="button"><i class="fas fa-bars"></i></a>
      </li>
    </ul>

    <!-- Right navbar links -->
    <ul class="navbar-nav ml-auto">
      <li class="nav-item mt-1 mr-3">
        <nuxt-link class="nav-link btn btn-sm btn-primary text-white" to="/" target="_blank">Lihat Website <i class="fa fa-external-link-alt"></i></nuxt-link>
      </li>
      <li class="nav-item dropdown pb-2">
        <a id="dropdownSubMenu1" href="#" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"
          class="nav-link dropdown-toggle">
          <img
            :src="`https://ui-avatars.com/api/?name=${user.name}&amp;background=4e73df&amp;color=ffffff&amp;size=100`"
            class="img-circle" style="opacity: .8" width="35" height="35">
          {{ user.name }}
        </a>
        <ul aria-labelledby="dropdownSubMenu1" class="dropdown-menu" style="right: 0px; left: inherit;">
          <li><a @click="logout" class="dropdown-item">Logout</a></li>
        </ul>
      </li>
    </ul>
  </nav>
</template>

<script>
  export default {

    computed: {
      user() {
        return this.$auth.user
      }
    },

    methods: {

      async logout() {

        //logout auth
        await this.$auth.logout()

        //redirect route login
        this.$router.push({
          name: 'login'
        })

      }

    }
  }
</script>

<style>

</style>