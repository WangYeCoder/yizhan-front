<template>
  <div class="home">
    这是主页面
  </div>
</template>

<script>

  import { formatTime } from "@/utils/index";
  import card from "@/components/card";

  export default {
    data() {
      return {
        motto: "Hello World",
        userInfo: {}
      };
    },

    components: {
      card
    },
    computed: {},
    methods: {}
  };
</script>

<style>

</style>
