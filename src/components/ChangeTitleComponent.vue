<template id="change-title-component">
<div>
  <em>change the title of your shopping list here</em>
  <input :value="value" @input="onInput"/>
  </div>
</template>

<script>
export default {
  name: 'change-title-component',
  props: ['value'],
  methods: {
    onInput: function (event) {
      console.log(event.target.value)
      this.$emit('input', event.target.value)
    }
  }
}
</script>
