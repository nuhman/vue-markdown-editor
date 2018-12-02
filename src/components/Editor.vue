<template>
  <div class="editor">
    <div class="left">
      <h2>Markdown Editor</h2>
      <p>
        <a
          href="https://learn.freecodecamp.org/front-end-libraries/front-end-libraries-projects/build-a-markdown-previewer"
          >Freecodeamp Project Link</a
        >
      </p>
      <textarea id="editor" v-model="text"></textarea>
    </div>
    <div class="container preview right">
      <h3>Preview</h3>
      <Preview :content="text" />
    </div>
  </div>
</template>

<script>
import Preview from "./Preview";

export default {
  name: "Editor",
  components: {
    Preview
  },
  data() {
    return {
      text: "# head"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2,
p {
  text-align: center;
}
textarea {
  background: #212121;
  color: #fff;
  width: 80%;
  height: 350px;
  padding: 20px;
  border-radius: 20px;
  font-family: monospace;
}
.left {
  text-align: center;
}
.container {
  background: #3b5f98;
  padding: 20px;
  margin: 20px;
  border-radius: 20px;
}
.container > * {
  background: #fff;
  padding: 10px;
}
.container > h3 {
  background: #3b5f98;
  text-align: center;
  color: #fff;
}
</style>
