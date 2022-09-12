<template>
  <div>
    <Slider />

    <div id="main-content">
      <Greetings />
      <Reasons />

      <section id="news" class="news">
        <b-row md="12" sm="12" class="content">
          <b-col md="4" sm="12"><h3>Berita Terbaru</h3></b-col>
          <b-col md="8" sm="12" class="text-right">
            <nuxt-link
              :to="{ name: 'post' }"
              class="btn btn-md btn-outline rounded shadow-sm"
              >Lihat Selengkapnya
            </nuxt-link>
          </b-col>
        </b-row>

        <b-row md="12" sm="12">
          <b-col md="4" sm="12" v-for="post in posts" :key="post.id">
            <b-card no-body class="border-0 rounded-lg shadow-md mb-3">
              <b-row class="g-0">
                <b-col md="12">
                  <nuxt-link
                    :to="{ name: 'post-slug', params: { slug: post.slug } }"
                    ><b-img
                      :src="post.image"
                      class="w-100 img-post h-100 object-fit-cover"
                      rounded="top"
                    ></b-img
                  ></nuxt-link>
                </b-col>
                <b-col md="12">
                  <b-card-body>
                    <h3>
                      <nuxt-link
                        :to="{ name: 'post-slug', params: { slug: post.slug } }"
                        >{{ post.title }}</nuxt-link
                      >
                    </h3>
                    <b-card-text>
                      <small class="text-muted mr-3"
                        ><i class="fa fa-calendar"></i>
                        {{ post.created_at }}</small
                      >
                      <small class="text-muted"
                        ><i class="fa fa-comments"></i>
                        {{ post.comments.length }} Komentar</small
                      >
                    </b-card-text>
                    <b-card-text>
                      {{ post.description.substr(0, 80) }}...</b-card-text
                    >

                    <nuxt-link
                      :to="{ name: 'post-slug', params: { slug: post.slug } }"
                      class="btn btn-more"
                      >Baca Selengkapnya</nuxt-link
                    >
                  </b-card-body>
                </b-col>
              </b-row>
            </b-card>
          </b-col>
        </b-row>
      </section>

      <Join />
    </div>
  </div>
</template>

<script>
import Slider from "@/components/web/slider.vue";
import Greetings from "@/components/web/greetings.vue";
import Reasons from "@/components/web/reasons.vue";
import Join from "@/components/web/join.vue";

export default {
  components: {
    Slider,
    Greetings,
    Reasons,
    Join,
  },

  //meta
  head() {
    return {
      title: "Sistem Informasi - IT Telkom Purwokerto",
      meta: [
        {
          hid: "og:title",
          name: "og:title",
          content: "Sistem Informasi - IT Telkom Purwokerto",
        },
        {
          hid: "og:site_name",
          name: "og:site_name",
          content: "Sistem Informasi - IT Telkom Purwokerto",
        },
        {
          hid: "og:image",
          name: "og:image",
          content: "../assets/img/logo-si.png",
        },
      ],
    };
  },

  async asyncData({ $axios }) {
    //fetching posts
    const posts = await $axios.$get("/api/web/postHomepage");

    //fetching categories
    const categories = await $axios.$get("/api/web/categorySidebar");

    //fetching tags
    const tags = await $axios.$get("/api/web/tags");

    return {
      posts: posts.data,
      categories: categories.data,
      tags: tags.data,
    };
  },
};
</script>

<style></style>
