<template id="add-item-component">
  <!--
      properties: items,
      events: add
    -->
  <div class="input-group">
    <input @keyup.enter="addItem" v-model="newItem"
           placeholder="add shopping list item"
           type="text" class="form-control"/>
    <span class="input-group-btn">
      <button @click="addItem" class="btn btn-default" type="button">Add!</button>
    </span>
  </div>
</template>

<script>
export default {
  name: 'add-item-component',
  data () {
    return {
      newItem: '',
      msg: 'add-item-component'
    }
  },
  methods: {
    addItem: function () {
      var text = this.newItem.trim()
      if (text) {
        this.$emit('add', this.newItem)
        this.newItem = ''
      }
    }
  },
  props: ['items']
}
</script>
