<template>
  <div class="items-component">
    <h1>{{ msg }}</h1>
    <ul>
    <item-component/>
    <item-component/>
    <item-component/>
    <item-component/>
    <item-component/>
    </ul>
  </div>
</template>

<script>
import ItemComponent from './ItemComponent'
export default {
  name: 'items-component',
  data () {
    return {
      msg: 'items-component'
    }
  },
  components: { ItemComponent }
}
</script>
