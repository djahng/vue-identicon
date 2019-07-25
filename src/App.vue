<template>
  <div>
    <Header />
    <div class="container my-width">
      <TextInput @textInput="onTextInput" />

      <Identicon :text="text" />
    </div>
  </div>
</template>

<script>
import Header from './components/Header';
import TextInput from './components/TextInput';
import Identicon from './components/Identicon';

export default {
  name: 'App',

  data() {
    return { text: '' }
  },

  components: {
    Header,
    TextInput,
    Identicon
  },

  methods: {
    onTextInput(text) {
      this.text = text;
    }
  }
};
</script>

<style scoped>
  .my-width {
    width: 75%;
  }
</style>
