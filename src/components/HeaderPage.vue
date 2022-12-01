<template>
  <header>
    <img
      src="../img/logo-small.svg"
      alt=""
    >
    <label for="select-genre">
      <select
        id="select-genre"
        v-model="selectValue"
        name="genre"
        @change="$emit('changeGenre', selectValue)"
      >
        <option value="All">All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </label>
  </header>
</template>

<script>
export default {
  name: 'HeaderPage',
  data() {
    return {
      selectValue: 'All',
    };
  },
};
</script>

<style lang="scss" scoped>
header{
  height: 10vh;
  background-color: grey;
  display: flex;
  align-items: center;
  padding: 1rem;
  img{
    height: 100%;
    margin-right: 2rem;
  }
  select{
    width: 100px;
  }
}
</style>
