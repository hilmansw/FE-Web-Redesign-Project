<template>
  <div>
    <!-- navbar -->
    <Navbar />

    <!-- content -->
    <Nuxt />

    <!-- footer -->
    <Footer />
  </div>
</template>
<script>
import Navbar from "@/components/web/navbar.vue";
import Footer from "@/components/web/footer.vue";
export default {
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
body {
  background-color: #fafafa !important;
}

#navbar-wrapper {
  border-bottom: 5px solid #31ac8c;
  background: #fafafa;
  position: sticky;
  top: 0;
  z-index: 999;
  padding: 8px 56px 8px 56px;
}

.top-navbar {
  transition: all 0.5s;
  font-family: "Poppins", sans-serif;
}
.top-navbar a {
  padding: 10px;
  font-weight: 600;
  color: #4b4b4b;
}
.top-navbar .navbar-brand img {
  max-height: 70px;
}
.top-navbar .navbar-text {
  color: #4b4b4b;
}
.top-navbar .navbar-text a {
  color: #31ac8c;
}
.top-navbar .navbar-text a:hover,
.top-navbar .navbar-text a:focus {
  color: #31ac8c;
  transition: 0.3s;
}
.top-navbar .navbar-nav .nav-link:last-child {
  margin-right: 0 0.25em;
}
.top-navbar .navbar-nav .nav-link:not(.disabled):hover,
.top-navbar .navbar-nav .nav-link:not(.disabled):focus {
  color: #31ac8c;
}
.top-navbar .navbar-nav .nav-item.active .nav-link,
.top-navbar .navbar-nav .nav-item.active .nav-link:hover,
.top-navbar .navbar-nav .nav-item.active .nav-link:focus,
.top-navbar .navbar-nav .nav-item.show .nav-link,
.top-navbar .navbar-nav .nav-item.show .nav-link:hover,
.top-navbar .navbar-nav .nav-item.show .nav-link:focus {
  color: #31ac8c;
  background-color: #31ac8c;
}
.top-navbar .navbar-toggler {
  color: #31ac8c;
  border-color: #31ac8c;
}
.top-navbar .navbar-toggler:hover,
.top-navbar .navbar-toggler:focus {
  background-color: #31ac8c;
  color: white;
}
.top-navbar .navbar-toggler .navbar-toggler-icon {
  color: #31ac8c;
}
.top-navbar .navbar-collapse,
.top-navbar .navbar-form {
  border-color: #31ac8c;
}
.top-navbar .navbar-link {
  color: #4b4b4b;
}
.top-navbar .navbar-link:hover {
  color: #31ac8c;
  transition: 0.3s;
}

/* Button configuration */
.btn-outline {
  border-color: #31ac8c;
  color: #31ac8c;
}

.btn-outline:hover {
  background-color: #31ac8c;
  color: white;
}

.btn-more {
  background-color: #31ac8c;
  color: #fff;
  border-radius: 16px;
  padding: 8px 16px 8px 16px;
  white-space: nowrap;
  transition: 0.3s;
  font-size: 14px;
  display: inline-block;
}

.btn-more:hover {
  background: #4b4b4b;
  color: white;
}

.card-category {
  background-color: #dadada;
}

.card-body h3 {
  font-size: 24px;
  font-weight: 600;
}

.card-body h3 a {
  color: #4b4b4b;
  transition: 0.3s;
}

.card-body h3 a:hover {
  color: #31ac8c;
}

.object-fit-cover {
  object-fit: cover;
}

/* Greetings */
#greetings {
  padding: 64px 0px 64px 0px;
}

.greetings .btn-more {
  font-family: "Raleway", sans-serif;
  font-weight: 500;
  font-size: 15px;
  letter-spacing: 1px;
  display: inline-block;
  padding: 10px 35px;
  border-radius: 50px;
  transition: 0.5s;
  margin-top: 30px;
  border: 2px solid #fff;
  color: #fff;
  background: #31ac8c;
}
.greetings .btn-more:hover {
  background: #187b75;
  border: 2px solid #187b75;
}
.greetings .content h3 {
  font-size: 32px;
  margin: 30px 0 15px 0;
  font-weight: 700;
  position: relative;
  padding-bottom: 10px;
}
.greetings .content h3:before {
  content: "";
  position: absolute;
  display: block;
  width: 100%;
  height: 3px;
  background: #eef0ef;
  bottom: 0;
  left: 0;
}
.greetings .content h3:after {
  content: "";
  position: absolute;
  display: block;
  width: 28%;
  height: 3px;
  background: #31ac8c;
  bottom: 0;
  left: 0;
}
.greetings .content p {
  line-height: 1.8em;
  color: #6c6c6c;
  font-size: 18px;
}
.greetings .content ul {
  list-style: none;
  padding: 0;
}
.greetings .content ul li {
  padding-bottom: 10px;
}
.greetings .content ul i {
  font-size: 20px;
  padding-right: 4px;
  color: #31ac8c;
}
.greetings .content .learn-more-btn {
  background: #31ac8c;
  color: #fff;
  border-radius: 50px;
  padding: 8px 25px 9px 25px;
  white-space: nowrap;
  transition: 0.3s;
  font-size: 14px;
  display: inline-block;
}
.greetings .content .learn-more-btn:hover {
  background: #187b75;
  color: #fff;
}

/* Reasons */
#reasons {
  padding: 32px 0 32px 0;
}

.reasons .content .more-btn {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  padding: 6px 30px 8px 30px;
  color: #fff;
  border-radius: 50px;
  transition: all ease-in-out 0.4s;
}
.reasons .content .more-btn i {
  font-size: 14px;
}
.reasons .content .more-btn:hover {
  color: #187b75;
  background: #fff;
}

.reasons .content {
  padding: 32px;
  height: 394px;
  background: #31ac8c;
  display: table-cell;
  vertical-align: middle;
  border-radius: 16px;
  color: #fff;
}
.reasons .content h3 {
  font-weight: 700;
  font-size: 32px;
  margin-bottom: 16px;
}
.reasons .content p {
  margin-bottom: 30px;
  font-size: 18px;
}
.reasons .content .more-btn {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  padding: 6px 30px 8px 30px;
  color: #fff;
  border-radius: 50px;
  transition: all ease-in-out 0.4s;
}
.reasons .content .more-btn i {
  font-size: 14px;
}
.reasons .content .more-btn:hover {
  color: #187b75;
  background: #fff;
}

.reasons .content-2 {
  padding: 32px;
  background: #dedede;
  height: 394px;
  border-radius: 16px;
  color: #6d6d6d;
  text-align: center;
  display: table-cell;
  vertical-align: middle;
}
.reasons .content-2 h3 {
  font-weight: 500;
  font-size: 34px;
  margin-bottom: 30px;
}
.reasons .content-2 p {
  margin-top: 20px;
}
.reasons .content-2 .more-btn {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  padding: 6px 30px 8px 30px;
  color: #fff;
  border-radius: 50px;
  transition: all ease-in-out 0.4s;
  border: 0;
}
.reasons .content-2 .more-btn i {
  font-size: 14px;
}
.reasons .content-2 .more-btn:hover {
  color: #187b75;
  background: #fff;
}

.reasons .content-2 .icon-circle {
  margin: auto;
  width: 60px;
  padding-bottom: 16px;
}

/* Careers */
/* padding: top right bottom left */
#careers {
  padding: 0px 0px 64px 0px;
}
.careers .content h3 {
  font-weight: 600;
  line-height: 1.5em;
  font-size: 26px;
}
.careers .icon-box {
  display: flex;
  align-items: center;
  padding: 20px;
  transition: 0.3s;
  border: 1px solid #C6C6C6;
}
.careers .icon-box i {
  font-size: 32px;
  padding-right: 10px;
  line-height: 1;
}
.careers .icon-box h3 {
  font-weight: 700;
  margin: 0;
  padding: 0;
  line-height: 1;
  font-size: 16px;
}
.careers .icon-box h3 a {
  color: #37423b;
  transition: 0.3s;
}
.careers .icon-box:hover {
  border-color: #31AC8C;
}
.careers .icon-box:hover h3 a {
  color: #187b75;
}

#news {
  padding: 0px 6px 64px 6px;
}

.news .content h3 {
  font-size: 32px;
  margin: 0px 0 36px 0;
  font-weight: 700;
  position: relative;
  padding-bottom: 10px;
}
.news .content h3:after {
  content: "";
  position: absolute;
  display: block;
  width: 28%;
  height: 3px;
  background: #31ac8c;
  bottom: 0;
  left: 0;
}

/* Join banner */
#join {
  background: #31ac8c;
  border-radius: 32px;
  margin: 32px 0 64px 0;
}

.join img {
  margin-top: -64px;
}
.join .content .more-btn {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  padding: 6px 30px 8px 30px;
  color: #fff;
  border-radius: 50px;
  transition: all ease-in-out 0.4s;
}
.join .content .more-btn i {
  font-size: 14px;
}
.join .content .more-btn:hover {
  color: #187b75;
  background: #fff;
}

.join .content {
  padding: 32px;
  display: table-cell;
  vertical-align: middle;
  border-radius: 4px;
  color: #fff;
}
.join .content h3 {
  font-weight: 700;
  font-size: 32px;
  margin-bottom: 16px;
}
.join .content p {
  margin-bottom: 30px;
  font-size: 18px;
}
.join .content .more-btn {
  display: inline-block;
  background: rgba(255, 255, 255, 0.2);
  padding: 6px 30px 8px 30px;
  color: #fff;
  border-radius: 50px;
  transition: all ease-in-out 0.4s;
}
.join .content .more-btn i {
  font-size: 14px;
}
.join .content .more-btn:hover {
  color: #187b75;
  background: #fff;
}

/* Footer */
#footer {
  color: #fff;
  font-size: 16px;
  background: #31AC8C;
}
#footer .footer-top {
  padding: 64px;
  background: #ECF9F0;
}
#footer .footer-top .footer-contact {
  margin-bottom: 30px;
}
#footer .footer-top .footer-contact h4 {
  font-size: 22px;
  margin: 0 0 30px 0;
  padding: 2px 0 2px 0;
  line-height: 1;
  font-weight: 700;
}
#footer .footer-top .footer-contact p {
  font-size: 14px;
  line-height: 24px;
  margin-bottom: 0;
  font-family: "Raleway", sans-serif;
  color: #777777;
}
#footer .footer-top h4 {
  font-size: 22px;
  font-weight: bold;
  color: #444444;
  position: relative;
  padding-bottom: 12px;
}
#footer .footer-top .footer-links {
  font-size: 16px;
  margin-bottom: 24px;
}
#footer .footer-top .footer-links h3 {
  color: #4B4B4B;
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 18px;
}
#footer .footer-top .footer-links ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
#footer .footer-top .footer-links ul i {
  padding-right: 2px;
  color: #31AC8C;
  font-size: 18px;
  line-height: 1;
}
#footer .footer-top .footer-links ul li {
  padding: 10px 0;
  display: flex;
  align-items: center;
}
#footer .footer-top .footer-links ul li:first-child {
  padding-top: 0;
}
#footer .footer-top .footer-links ul a {
  color: #777777;
  transition: 0.3s;
  display: inline-block;
  line-height: 1;
}
#footer .footer-top .footer-links ul a:hover {
  text-decoration: none;
  color: #31AC8C;
}
#footer .footer-newsletter {
  font-size: 15px;
}
#footer .footer-newsletter h3 {
  color: #4B4B4B;
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 18px;
}
#footer .credits {
  padding-top: 5px;
  font-size: 13px;
}
#footer .credits a {
  color: #3ac162;
  transition: 0.3s;
}
#footer .credits a:hover {
  color: #31AC8C;
}
#footer .social-links a {
  margin-right: 8px;
}
#footer .social-links img {
  width: 40px;
  height: 40px;
}
#footer .social-links a:hover {
  opacity: .8;
}

.card {
  background: #F5F5F5;
  transition: 0.5s;
}

.card:hover {
  box-shadow: 0 1px 20px 0 rgba(0, 0, 0, 0.1);
}

.card .card-block .card-title h4 {
  margin-top: 10px;
}

.btn-search-circular,
.btn-search-circular:focus {
  background: #31ac8c;
  border: 0px;
  width: 45px;
  height: 45px;
  display: table-cell;
  vertical-align: middle;
  border-radius: 25px;
  margin-left: 16px;
}

.btn-search-circular:hover {
  background: #187b75;
}

#main-content {
  padding: 0 64px 0 64px;
}

.post-wrapper {
  margin: 64px;
}

.post-wrapper h3 {
  font-size: 24px;
  font-weight: 600;
}

.post-wrapper .content {
  font-size: 18px;
}

.breadcrumbs {
  background: #F5F5F5;
  padding: 16px 64px 16px 64px;
}


/* X-Small devices (portrait phones, less than 576px) */
@media (max-width: 575.98px) {
  .top-navbar {
    width: 100%;
  }
  #main-content {
    padding: 0 20px 0 20px;
  }

  #join {
    margin-top: -32px;
  }

  .join img {
    margin-top: 16px;
  }

  #navbar-wrapper {
    padding: 10px !important;
  }

  .btn-search-circular,
  .btn-search-circular:focus {
    width: 100%;
    margin-top: 16px;
    margin-left: 0px !important;
  }

  .btn-outline {
    width: 100%;
    margin-bottom: 20px;
  }

  .reason1, .reason2 {
    margin-bottom: 16px;
  }
}

@media (max-width: 767.98px) {
  #main-content {
    padding: 0 20px 0 20px;
  }

  #join {
    margin-top: -32px;
  }

  .join img {
    margin-top: 16px;
  }

  #navbar-wrapper {
    padding: 10px !important;
  }

  .btn-search-circular,
  .btn-search-circular:focus {
    width: 100%;
    margin-top: 16px;
    margin-left: 0px !important;
  }

  .btn-outline {
    width: 100%;
    margin-bottom: 20px;
  }

  .reason1, .reason2 {
    margin-bottom: 16px;
  }
}

@media (max-width: 991.98px) {
  #main-content {
    padding: 0 20px 0 20px;
  }

  #join {
    margin-top: -32px;
  }

  .join img {
    margin-top: 16px;
  }

  #navbar-wrapper {
    padding: 10px !important;
  }

  .btn-search-circular,
  .btn-search-circular:focus {
    width: 100%;
    margin-top: 16px;
    margin-left: 0px !important;
  }

  .btn-outline {
    width: 100%;
    margin-bottom: 20px;
  }

  .reason1, .reason2 {
    margin-bottom: 16px;
  }
}
</style>
