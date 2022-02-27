<template>
  <div class="the-wrapper">
    <MyHeader></MyHeader>
    <div class="page-wrapper">
      <Nuxt />
    </div>
    <MyFooter></MyFooter>
  </div>
</template>
<script>
export default {
  mounted() {
    if (!this.$nuxt.$colorMode.preference) {
      this.$nuxt.$colorMode.preference = "dark";
    }
  }
}
</script>
