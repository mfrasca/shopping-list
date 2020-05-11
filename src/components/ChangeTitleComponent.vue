<template id="change-title-component">
<div>
  <!--
      properties: value
    -->
  <em>change the title of your shopping list here</em>
  <input v-model="value[0]" />
  </div>
</template>

<script>
export default {
  name: 'change-title-component',
  props: ['value']
}
</script>
