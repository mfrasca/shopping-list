<template>
  <div class="items-component">
    <ul>
    <item-component v-for="item in items" :item="item" :key="item.text" />
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
