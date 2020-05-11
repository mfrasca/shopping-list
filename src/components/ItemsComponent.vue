<template>
  <div class="items-component">
    <ul>
    <item-component v-for="(item, i) in items" :item="item" :key="i" />
    </ul>
  </div>
</template>

<script>
import ItemComponent from './ItemComponent'
export default {
  name: 'items-component',
  components: { ItemComponent },
  props: ['items']
}
</script>
