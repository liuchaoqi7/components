<template>
  <div class="wraper">
    <my-table
      :tableDatas="{
        selectionShow:false,
        indexLabel:'编号',
        labelProp: [
          { label: '城市', prop: 'city' },
          { label: '县名', prop: 'xianming' },
          { label: '乡镇', prop: 'xiangzhen' },
        ],
        tableData: [{
          city:'商丘',
          xianming:'睢阳区',
          xiangzhen:'路河乡'
        }],
      }"
    ></my-table>
  </div>
</template>

<script>
import myTable from "@/components/myTable";
export default {
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
    };
  },
  components: {
    myTable,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
