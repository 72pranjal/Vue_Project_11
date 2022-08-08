<template>
  <img :src="imagelink" alt="" class="w-8 h-8 object-contain rounded-3xl" />
</template>

<script>
export default {
  name: "ProfileImage",
  data() {
    return {
      imagelink: ".assets/logo.png",
    };
  },
};
</script>

<style>
</style>