<template>
  <v-app class="white">
    <router-view/>
    <v-footer height="auto" color="deep-purple">
      <v-layout justify-center row wrap>
        <v-btn
          v-for="link in links"
          :key="link.link"
          color="white"
          flat
          round
          :href="link.href"
        >{{ link.link }}</v-btn>
        <v-flex deep-purple lighten-1 py-3 text-xs-center white--text xs12>
          &copy;2018 —
          <strong>Hart</strong>
        </v-flex>
      </v-layout>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    links: [
      {
        link: 'Document',
        href: '#/document'
      },
      {
        link: 'Hart Demo',
        href: '/'
      },
      {
        link: 'Blog',
        href: 'https://rumo.tistory.com/'
      },
      {
        link: 'Contact Me',
        href: 'https://rumo.netlify.com/'
      }
    ]
  })
}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Nanum+Myeongjo");
#app {
  font-family: "Avenir", "Nanum Myeongjo", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
