<script>
import { defineComponent } from "vue";

export default defineComponent({
    name: "Validator",
  props: {
      isbn: {
        type: String,
        required: true,
        validator: function (value) {
          const isbn = value.replaceAll('-', '')
          return !isNan(isbn) && isbn.length === 10;

        },
      },
  },
  watch: {
      isbn(newValue) {
        this.validate(newValue);
      },
  },
  methods: {
      clickHappend() {
        this.$emit("customClickOnButtonEvent")
      },
      validate(value) {
        const isbn = String(value);
        let sum = 0;
        let x = 10;

        for (const digit of isbn) {
          sum+= digit * x--;
        }
        if (sum %11 !==0) {
          console.warn(`The input ${isbn} is not a valid ISBN10.`)
        } else {
          console.log(`The input ${isbn} is a valid ISBN10`)
        }
      },
  }
});

</script>


<template>



</template>

<style scoped>

</style>