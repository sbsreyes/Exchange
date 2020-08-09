<template>
  <div>
    <px-assets-table v-bind:assets="assets" />
  </div>
</template>

<script>
import PxAssetsTable from "@/components/PxAssetsTable";
import api from "@/api";
export default {
  name: "Home",
  data() {
    return {
      assets: [],
    };
  },
  created() {
    api.getAssets().then((assets) => (this.assets = assets));
  },
  components: {
    PxAssetsTable,
  },
};
</script>
