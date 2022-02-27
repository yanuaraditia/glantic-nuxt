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
  created() {
    if (this.$nuxt.$colorMode.preference === 'system') {
      this.$nuxt.$colorMode.preference = 'dark'
    }
  },
  mounted() {
    if (this.$nuxt.$colorMode.preference === 'system') {
      this.$nuxt.$colorMode.preference = 'dark'
    }
  },
}
</script>
