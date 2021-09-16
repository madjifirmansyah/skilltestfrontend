<template>
  <div>
    <input type="text" v-model="item" @keypress.enter="add">
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ item}}
        <button @click="remove(index)">-</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return{
      items: [],
      item:''
    }
  },
methods: {
  add(item){
    this.items.push(this.item)
  },
  remove(index){
    this.items.splice(index, 1)
    }
  },
}
</script>

