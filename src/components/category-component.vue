<template>
  <div class="container">
    <label class="name">{{ $t("category") }} {{ name }}</label>
    <label>{{ content }}</label>
    <ul>
      <li v-for="tutorial in tutorials">
        <tutorial :title="tutorial.title" />
      </li>
    </ul>
  </div>
</template>

<script>
import Tutorial from "@/components/tutorial-component.vue";

export default {
  components: { Tutorial },
  props: {
    name: String,
    content: String,
    tutorials: Array,
  },
  name: "category",
};
</script>

<style scoped>
.container {
  border-color: cadetblue;
  border-width: 2px;
  border-style: solid;
  margin: 10px;
  padding: 8px;
}

.name {
  font-weight: bold;
  font-size: large;
}
</style>
