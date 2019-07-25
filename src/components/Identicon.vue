<template>
  <div>
    Output:
    <div v-html="identicon" id="identicon" />
  </div>
</template>

<script>
import jdenticon from 'jdenticon';

export default {
  name: 'Identicon',

  props: ['text'],

  computed: {
    identicon() {
      return jdenticon.toSvg(this.text, 200);
    }
  }
};
</script>
