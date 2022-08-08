<template>
  <header class="w-full text-center text-3xl">
    <div class="fixed top-0 left-0 w-full h-16 bg-white">
      <div
        class="flex flex-nowrap h-full px-8 mx-auto border-b border-solid blue"
      >
        <a :href="url" class="flex items-center h-full text-xl">{{
          company
        }}</a>
        <nav class="h-full ml-12">
          <ul class="flex h-full p-0 m-0 list-none">
            <!-- <li class="h-full">
              <a href="" class="flex items-center h-full py-2.5">Teams</a>
            </li> -->
            <li
              class="h-full ml-9 first:ml-0"
              v-for="menuitems in menuitems"
              v-bind:key="menuitems"
            >
              <a href="" class="flex items-center h-full py-2.5">{{
                menuitems
              }}</a>
            </li>
          </ul>
        </nav>
        <div class="flex items-center h-full ml-auto">
          <ProfileImage v-if="isloggedin" />
          <ActionButton v-else @click="actionuser" />
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import ActionButton from "./ActionButton.vue";
import ProfileImage from "./ProfileImage.vue";
export default {
  name: "MainNav",
  components: {
    ActionButton,
    ProfileImage,
  },
  data() {
    return {
      company: "Bobo Careers",
      url: "https//google.careers.com",
      menuitems: ["Teams", "Location", "Life at Bobo", "How we hire", "Jobs"],
      isloggedin: false,
    };
  },
  methods: {
    actionuser() {
      this.isloggedin = true;
    },
  },
};
</script>

<style></style>
