<template>
  <header>
    <img
      src="../img/logo-small.svg"
      alt=""
    >
  </header>
</template>

<script>
export default {
  name: 'HeaderPage',
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
  }
}
</style>
