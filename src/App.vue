<template>
  <MyTable :header="header" :rows="rows"></MyTable>
</template>

<script>
import MyTable from './components/MyTable.vue'

export default {
  name: 'App',
  setup(){
    const header = ["1st Title", "2nd Title"]
    const rows = [
        [{data: '1st Content'}, {data: '2nd Content'}],
        [{data: '1st Content2', colspan: 2} ],
        [{data: '1st Content3', rowspan: 3}, {data: '2nd Content3'}],
        [{data: '2nd Content4'}],
        [{data: '2nd Content5'}]
      ]
      return {header, rows}
  },
  components: {
    MyTable
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
