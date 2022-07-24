<template>
  <header-container>
    <template #default>
      <h1 class="w-full text-4xl font-normal">Teams</h1>
    </template>
    <template #subtitle>
      <h2 class="w-full my-4 text-base font-light">
        It's awesome working here. why don't you hire me
      </h2>
    </template>
  </header-container>
</template>

<script>
import HeaderContainer from "../components/Shared/HeaderContainer.vue";
export default {
  components: { HeaderContainer },
};
</script>

<style></style>
