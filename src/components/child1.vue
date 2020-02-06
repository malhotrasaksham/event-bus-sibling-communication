<template>
  <div>
    <h2>First Child</h2>
    <p>Age is {{age}}</p>
    <p>
      <!--<button @click="IncrementAge()">Increment Age</button>-->
    </p>
  </div>
</template>

<script>
import { eventBus } from "../main.js";
export default {
  props: {
    /*age: {
      type: Number,
      default: age => parseInt(age, 10)
    }*/
  },
  data() {
    return {
      age: 4
    };
  },
  methods: {
    IncrementAge() {
      eventBus.$emit("IncrementAge", ++this.age);
    }
  },
  created() {
    eventBus.$on("IncrementAge", function(age) {
      console.log(age);
      this.age = age;
    });
  }
};
</script>
