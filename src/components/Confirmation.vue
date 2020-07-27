<template>
  <div>
    <b-alert variant="success" :show="showDismissibleAlert" @dismissed="dism" dismissible>
      {{ message }}</b-alert>
  </div>
</template>

<script>
export default {
  props: ['message', 'showDismissibleAlert'],
  methods: {
    dism() {
      this.$emit('closed');
    },
  },
};
</script>
