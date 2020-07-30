<template>
  <main>
    <px-header :links="links"></px-header>
    <router-view class="container px-5 sm:px-20 py-2 flex justify-center"></router-view>
  </main>
</template>

<script>
import PxHeader from "@/components/PxHeader";

export default {
  name: "App",
  components: { PxHeader },
  data() {
    return {
      links: [
        {
          title: "BTC",
          to: { name: "coin", params: { id: "bitcoin" } }
        },
        {
          title: "ETH",
          to: { name: "coin", params: { id: "ethereum" } }
        },
        {
          title: "XRP",
          to: { name: "coin", params: { id: "ripple" } }
        }
      ]
    };
  }
};
</script>
