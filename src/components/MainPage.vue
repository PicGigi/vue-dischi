<template>
  <main>
    <album-card
      v-for="objAlbum in arrAlbums"
      :key="objAlbum.title"
      :album-info="objAlbum"
    />
  </main>
</template>

<script>
import AlbumCard from '@/components/AlbumCard.vue';

export default {
  name: 'MainPage',
  components: {
    AlbumCard,
  },
  props: {
    // eslint-disable-next-line vue/require-default-prop
    arrAlbums: Array,
  },
};
</script>

<style lang="scss" scoped>
main{
  height: 90vh;
  width: 100%;
  background-color: darkgray;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  padding: 0 20%;
}
</style>
