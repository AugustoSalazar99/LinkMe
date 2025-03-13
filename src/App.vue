<template>
  <div class="min-h-screen  flex items-center justify-center  bg-gradient-to-b from-gray-900 via-purple-700 to-purple-700">
    <div class="w-full max-w-4xl p-5">
      <linkme />
    </div>
  </div>
</template>


<script>
import linkme from "@/components/linkme.vue";
export default {
  name: "App",
  components: {
    linkme,
  },
};
</script>

<style></style>
