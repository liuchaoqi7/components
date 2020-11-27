<template>
  <div class="wraper">
    <h1>自己封装的element组件</h1>
    <h3>table表格组件</h3>
    <el-table :data="tableDatas.tableData" style="width: 100%">
      <el-table-column type="selection" v-if="tableDatas.selectionShow">
      </el-table-column>
      <el-table-column
        type="index"
        :label="tableDatas.indexLabel"
        v-if="tableDatas.indexShow"
      >
      </el-table-column>
      <el-table-column
        v-for="(item, index) in tableDatas.labelProp"
        :key="index"
        :prop="item.prop"
        :label="item.label"
      >
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  props: {
    tableDatas: {
      type: Object,
      default: () => {
        return {
          selectionShow: true,
          indexShow: true,
          indexLabel: "序号",
          labelProp: [
            { label: "姓名", prop: "name" },
            { label: "地址", prop: "address" },
            { label: "日期", prop: "date" },
          ],
          tableData: [
            {
              date: "2016-05-02",
              name: "王小虎",
              address: "上海市普陀区金沙江路 1518 弄",
            },
            {
              date: "2016-05-04",
              name: "王小虎",
              address: "上海市普陀区金沙江路 1517 弄",
            },
            {
              date: "2016-05-01",
              name: "王小虎",
              address: "上海市普陀区金沙江路 1519 弄",
            },
            {
              date: "2016-05-03",
              name: "王小虎",
              address: "上海市普陀区金沙江路 1516 弄",
            },
          ],
        };
      },
    },
  },
  data() {
    return {
      // tableData: [
      //   {
      //     date: "2016-05-02",
      //     name: "王小虎",
      //     address: "上海市普陀区金沙江路 1518 弄",
      //   },
      //   {
      //     date: "2016-05-04",
      //     name: "王小虎",
      //     address: "上海市普陀区金沙江路 1517 弄",
      //   },
      //   {
      //     date: "2016-05-01",
      //     name: "王小虎",
      //     address: "上海市普陀区金沙江路 1519 弄",
      //   },
      //   {
      //     date: "2016-05-03",
      //     name: "王小虎",
      //     address: "上海市普陀区金沙江路 1516 弄",
      //   },
      // ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
