<template>
  <div id="preview" class="preview" v-html="getMarkdown"></div>
</template>

<script>
import marked from "marked";

export default {
  name: "Preview",
  props: ["content"],
  data() {
    return {};
  },
  computed: {
    getMarkdown: function() {
      return marked(this.content, { sanitize: true });
      //return this.text;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
  border: 1px solid black;
}
</style>
