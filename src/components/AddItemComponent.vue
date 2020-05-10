<template id="add-item-component">
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
    addItem (event) {
      this.items.push({
        text: event.target.value,
        checked: false
      })
    }
  },
  props: ['items']
}
</script>
