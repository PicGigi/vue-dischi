<template>
  <div>
    <header-page @changeGenre="searchGenre" />
    <main-page :arr-albums="arrSelectedGenre" />
  </div>
</template>

<script>
import axios from 'axios';
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';

export default {
  name: 'App',
  components: {
    HeaderPage,
    MainPage,
  },
  data() {
    return {
      urlApi: 'https://flynn.boolean.careers/exercises/api/array/music',
      Albums: [],
      genreTwo: 'All',
    };
  },
  computed: {
    arrSelectedGenre() {
      return this.Albums.filter((objAlbum) => objAlbum.genre === this.genreTwo);
    },
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.Albums = axiosResponse.data.response;
      });
  },
  methods: {
    searchGenre(genre) {
      this.genreTwo = genre;
    },
  },
};

</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
