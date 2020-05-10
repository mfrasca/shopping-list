<template>
  <li class="item-component">{{ msg }}</li>
</template>

<script>
export default {
  name: 'item-component',
  data () {
    return {
      msg: 'item: ' + (Math.random() * 200).toFixed(1)
    }
  }
}
</script>
