<template>
  <ul class="album">
    <img
      :src="albumInfo.poster"
      alt=""
    >
    <li>{{ albumInfo.title }}</li>
    <li>{{ albumInfo.author }}</li>
  </ul>
</template>

<script>
export default {
  name: 'AlbumCard',
  props: {
    // eslint-disable-next-line vue/require-default-prop
    albumInfo: Object,
  },
};
</script>

<style lang="scss" scoped>
.album{
  width: 200px;
  height: 300px;
  border: 3px solid black;
  background-color: grey;
  list-style: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: .5rem;
  color: white;
  font-weight: bold;
  font-family:'Segoe UI', Roboto;

  img{
    width: 100%;
    margin-bottom: 1rem;
  }
}
</style>
