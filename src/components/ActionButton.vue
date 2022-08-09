<template>
  <button :class="buttonClass">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "ActionButton",
   props:["text","type"],
  data() {
    return {
      primary: this.type==="primary", //false
      sceondary:this.type==="secondary"   //true
    };
  },
  computed: {
    buttonClass() {
      return {
        primary: this.primary,
        sceondary: !this.primary,
      };
    },
  },
  methods: {},

 
};
</script>

<style scoped>
button {
  @apply px-5  py-3  font-medium rounded;
}
.primary {
  @apply text-white border-0  bg-blue-500  hover:shadow-blue;
}
.sceondary {
  @apply text-brand-blue-1 bg-transparent hover:bg-brand-blue-2 hover:text-white;
}
</style>
>
