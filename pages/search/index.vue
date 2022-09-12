<template>
  <div class="post-wrapper">
    <b-row>
      <b-col md="12" class="mb-5 text-center">
        <h3>
          Pencarian dengan kata kunci : <strong>{{ $route.query.q }}</strong>
        </h3>
      </b-col>

      <b-col md="4" class="mb-3" sm="12" v-for="post in posts" :key="post.id">
        <b-card
          :img-src="post.image"
          img-top
          tag="article"
          class="mb-2 h-100 rounded-lg"
        >
          <h3>
            <nuxt-link
              :to="{ name: 'post-slug', params: { slug: post.slug } }"
              >{{ post.title }}</nuxt-link
            >
          </h3>
          <b-card-text>
            <small class="text-muted mr-3"
              ><i class="fa fa-calendar"></i> {{ post.created_at }}</small
            >
            <small class="text-muted"
              ><i class="fa fa-comments"></i>
              {{ post.comments.length }} Komentar</small
            >
          </b-card-text>
          <b-card-text> {{ post.description.substr(0, 80) }}...</b-card-text>

          <nuxt-link
            :to="{ name: 'post-slug', params: { slug: post.slug } }"
            class="btn btn-more"
            >Baca Selengkapnya</nuxt-link
          >
        </b-card>
      </b-col>
    </b-row>
    <b-row class="mt-4 justify-content-center">
      <b-pagination
        v-model="pagination.current_page"
        :total-rows="pagination.total"
        :per-page="pagination.per_page"
        @input="changePage"
        aria-controls="my-table"
      >
      </b-pagination>
    </b-row>
  </div>
</template>

<script>
export default {
  //meta
  head() {
    return {
      title: "Search - S1 Sistem Informasi IT Telkom Purwokerto",
      meta: [
        {
          hid: "og:title",
          name: "og:title",
          content: "S1 Sistem Informasi IT Telkom Purwokerto",
        },
        {
          hid: "og:site_name",
          name: "og:site_name",
          content: "S1 Sistem Informasi IT Telkom Purwokerto",
        },
        {
          hid: "og:image",
          name: "og:image",
          content: "https://i.imgur.com/xKOCz0P.png",
        },
      ],
    };
  },

  //watch query URL
  watchQuery: ["q", "page"],

  async asyncData({ $axios, query }) {
    //fetching posts
    const posts = await $axios.$get(
      `/api/web/posts?q=${query.q}&page=${parseInt(query.page)}`
    );

    return {
      posts: posts.data.data,
      pagination: posts.data,
    };
  },

  methods: {
    //change page pagination
    changePage(page) {
      this.$router.push({
        path: this.$route.path,
        query: {
          q: this.$route.query.q,
          page: page,
        },
      });
    },
  },
};
</script>

<style></style>
