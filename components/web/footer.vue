<template>
  <footer id="footer">
    <div class="footer-top">
      <div class="row">
        <div class="col-lg-4 col-md-6 footer-contact">
          <h3><img src="../../assets/img/logo-si.png" width="200" /></h3>
          <p>Bridging Technology for Tourism</p>
          <p>
            Jl. D.I Panjaitan No. 128 Purwokerto 53147, Central Java - Indonesia
          </p>
        </div>

        <div class="col-lg-3 col-md-6 footer-links">
          <h3>Link Penting</h3>
          <ul>
            <li><i class="fas fa-angle-right fa-fw" /> <a href="http://ittelkom-pwt.ac.id">IT Telkom Purwokerto</a></li>
            <li><i class="fas fa-angle-right fa-fw" /> <a href="http://lms.ittelkom-pwt.ac.id">E-learning</a>
            </li>
            <li><i class="fas fa-angle-right fa-fw" /> <a href="https://dlibrary.ittelkom-pwt.ac.id/">Perpustakaan</a>
            </li>
          </ul>
        </div>

        <div class="col-lg-3 col-md-6 footer-links">
          <h3>Profil</h3>
          <ul>
            <li><i class="fas fa-angle-right fa-fw" /> <a href="#">Organization</a></li>
            <li><i class="fas fa-angle-right fa-fw" /> <a href="#">Faculty and Staff</a>
            </li>
            <li><i class="fas fa-angle-right fa-fw" /> <a href="#">Alumni</a>
            </li>
          </ul>
        </div>

        <div class="col-lg-2 col-md-6 footer-newsletter">
          <h3>Find Us</h3>
          <div class="social-links pt-3 pt-md-0">
            <a href="http://www.facebook.com/"><img src="../../assets/img/icon-fb.png" /></a>
            <a href="https://instagram.com/"><img src="../../assets/img/icon-ig.png" /></a>
            <a href="https://twitter.com/"><img src="../../assets/img/icon-twt.png" /></a>
          </div>
        </div>
      </div>
    </div>

    <div class="container py-4">
      <div class="me-md-auto text-center">
        <div class="copyright">
          &copy; Copyright <strong><span>Sistem Informasi ITTP</span></strong
          >. All Rights Reserved
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  //data function
  data() {
    return {
      //state tags
      tags: [],
    };
  },

  async fetch() {
    //fething tags on Rest API
    await this.$axios.get("/api/web/tags").then((response) => {
      //assign response to state "tags"
      this.tags = response.data.data;
    });
  },
};
</script>

<style></style>
