<template>
  <div class="form-group mt-4">
    <label>Enter some text:</label>
    <input class="form-control" @input="onInput" />
  </div>
</template>

<script>
export default {
  name: 'TextInput',

  methods: {
    onInput(event) {
      this.$emit('textInput', event.target.value);
    }
  }
};
</script>
