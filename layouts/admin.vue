<template>

  <div class="hold-transition sidebar-mini">
    <div class="wrapper">
      <!-- Header -->
      <Header />
      <!-- /.Hader -->

      <aside class="main-sidebar sidebar-dark-primary elevation-4">
        <a to="/admin/dashboard" class="brand-link text-center">
          <div class="p-3"><img src="../assets/img/logo-si.png" width="100%" /></div>
        </a>

        <!-- Sidebar -->
        <div class="sidebar">
          <Sidebar />
        </div>
        <!-- /.sidebar -->
      </aside>

      <!-- content -->
      <Nuxt />
      <!-- / .content -->

      <footer class="main-footer">
        <div class="float-right d-none d-sm-block">
          <b>Made with</b> <i class="fa fa-heart" style="color: red;"/>
        </div>
        <strong>Copyright &copy; 2022 Hilman Singgih Wicaksana.</strong> All rights reserved.
      </footer>
      <aside class="control-sidebar control-sidebar-dark">
      </aside>
    </div>
  </div>
</template>

<script>
  import Header from '@/components/admin/header.vue'
  import Sidebar from '@/components/admin/sidebar.vue'

  export default {

    //middleware auth
    middleware: 'auth',

    components: {
      Header,
      Sidebar
    }

  }
</script>

<style>
  .wrapper, .content-wrapper {
    background-color: #ccdcec !important;
  }
</style>