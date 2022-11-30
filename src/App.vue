<template>
  <div>
    <header-page />
    <main-page :arr-albums="Albums" />
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
      Albums: null,
    };
  },
  created() {
    axios.get(this.urlApi)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.Albums = axiosResponse.data.response;
      });
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
