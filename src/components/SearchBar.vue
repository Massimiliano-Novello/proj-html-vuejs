<script>
export default {
  name: "SearchBar",
  props: ['navigationBar']
};
</script>

<template>
  <ul class="header-list d-flex list">
    <li class="mx-2">
      <a class="text-decoration-none text-white" href="">{{ navigationBar }}</a>
    </li>
  </ul>
</template>

<style lang="scss" scoped>
.list {
    list-style-type: none;
}
</style>
