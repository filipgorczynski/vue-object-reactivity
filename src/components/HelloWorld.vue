<template>
  <div>
    <button @click="changeObject1">change obj 1</button><br />
    <button @click="changeObject2">change obj 2</button><br />
    <button @click="changeObject3">change obj 3</button><br />
    <button @click="changeObject4">change obj 4</button>
    <pre>{{ my_obj_1 }}</pre>
    <pre>{{ my_obj_2 }}</pre>
    <pre>{{ my_obj_3 }}</pre>
    <pre>{{ my_obj_4 }}</pre>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      my_obj_1: {},
      my_obj_2: {'attribute_2': 'value_2'},
      my_obj_3: {},
      my_obj_4: {}
    }
  },
  methods: {
    changeObject1: function () {
      this.my_obj_1.attribue_1 = 'Value 1 - modified'
    },
    changeObject2: function () {
      this.my_obj_1.attribue_2 = 'Value 2 - modified'
    },
    changeObject3: function () {
      this.my_obj_3 = {attribute_3: 'Value 3 - modified'}
    },
    changeObject4: function () {
      this.my_obj_4 = Object.assign({}, this.my_obj_4, { attribute_4: 'Value 4 - modified' })
    }
  }
}
</script>
