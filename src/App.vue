<script lang="ts">
import ISBNgui from "@/components/ISBNgui/ISBNgui.vue";
import { defineComponent } from "vue";

export default defineComponent({
  components: {
    ISBNgui,
    "ISBN": ISBNgui,
  },
});

</script>

<template>


<ISBN></ISBN>

</template>

<style scoped>

</style>
