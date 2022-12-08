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

  <div>
  <H1><b><center>Réka A Király</center></b></H1>
  </div>

<!--<ISBN></ISBN>-->



</template>

<style scoped>
div {
  font-size: 100pt;
  color: red;
}
</style>
