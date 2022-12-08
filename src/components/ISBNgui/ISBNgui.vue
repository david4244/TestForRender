<script>
import { defineComponent } from "vue";
import Validator from "@/components/Validator/Validator.vue";


export default defineComponent( {

  components: {
    'validator': Validator

  },
  name: "ISBN",

  data () {

    return {
      isbn: "",
    }
  },
  methods: {
    someMethod() {
      console.log("some Method has been called")
    },
    anotherMethod(message) {
      console.log(`Message from child: ${message}`)
      console.log("another Method has been called (because")
    }
  }

});

</script>

<template>
  <header class="content columns is-centered">
  <div class="column is-one-quarter">
    <h1> ISBN Validator</h1>
  </div>
  </header>

  <main class="content columns is-centered">
    <div class="column is-one-quarter">
  <div class="field">
  <label for="ISBN" class="label">ISBN</label>
      <div class="control has-icons-left">
  <input title="Enter a valid ISBN 10" class="input is-primary" type="text" id="isbn">
        <span class="icon is-small is-left">
          <i class="fa fa-book"></i>
          </span>
        </div>
      </div>
    </div>
    <validator v-bind:isbn="isbn"></validator>
  </main>




</template>

<style scoped>

</style>