<template>
<li :class="{ 'removed': item.checked }">
  <div class="checkbox">
    <label>
      <input v-model="item.checked" type="checkbox">{{ item.text }}
    </label>
  </div>
</li>
</template>

<script>
export default {
  name: 'item-component',
  props: ['item']
}
</script>

<style scoped>
  .removed {
    color: gray;
  }
  .removed span {
    text-decoration: line-through;
  }
  li {
    list-style-type: none;
  }
  li span {
  margin-left: 5px;
  }
</style>
