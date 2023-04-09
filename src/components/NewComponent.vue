<script>
import { ref } from "vue";
export default {
  setup() {
    const query = ref("");

    const reset = (evt) => {
      query.value = ""; //clears the query
    };

    return {
      reset,
      query,
    };
  },
};
</script>
<!--  -->

<template>
  <div>
    <h3 class="make-it-green">Here's the new component that I made</h3>
    <h2>Filter LearnVue Articles</h2>
    <input type="text" placeholder="Filter Search" v-model="query" />
    <button @click="reset">Reset</button>
    <p>{{ query }}</p>

  </div>
</template>

<!--  -->
<style scoped>
.make-it-green {
  color: greenyellow;
}
.root {
  width: 400px;
  margin: 0 auto;
}
.root p {
  text-align: right;
  font-size: 0.7em;
  margin: 0;
}
ul {
  list-style: none;
  width: 50px 0;
  padding: 0;
  background-color: #fafafa;
  border-radius: 5px;
  border: 1px solid #ddd;
}
li {
  text-align: left;
  padding: 20px;
  border-bottom: 1px solid #ddd;
}
li:nth-last-of-type(1) {
  border-bottom: none;
}
</style>
