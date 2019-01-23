<template>
  <div>
    <el-button type="primary" class="btn">新建</el-button>
    <el-table :data="tableData" border style="width: 100%">
      <el-table-column fixed prop="id" label="编号" width="150" align="center">
      </el-table-column>
      <el-table-column prop="name" label="姓名" width="120" align="center">
      </el-table-column>
      <el-table-column prop="age" label="年龄" width="120" align="center">
      </el-table-column>
      <el-table-column prop="phone" label="电话" width="120" align="center">
      </el-table-column>
      <el-table-column prop="email" label="邮箱" width="120" align="center">
      </el-table-column>
      <el-table-column prop="address" label="地址" width="300" align="center">
      </el-table-column>
      <el-table-column prop="skill" label="技能" width="120" align="center">
      </el-table-column>
      <el-table-column prop="decs" label="简介" width="120" align="center">
      </el-table-column>
      <el-table-column fixed="right" label="操作" width="150" align="center">
        <template slot-scope="scope">
          <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
          <el-button type="text" size="small">编辑</el-button>
          <el-button type="text" size="small" @click="handleDelete(scope.$index, tableData)">删除</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        tableData: [{
          id: '01',
          name: '甄漂亮',
          age: '18',
          email: '888@qq.com',
          address: '上海市普陀区金沙江路 1518 弄',
          phone: '18888767867',
          skill: 'vue',
          decs: '我会vue'
        }, {
          id: '02',
          name: '甄大胆',
          age: '22',
          email: '666@qq.com',
          address: '北京市海淀区长安路28号',
          phone: '13386786878',
          skill: 'vue',
          decs: '我会vue'
        }, {
          id: '03',
          name: '甄可爱',
          age: '30',
          email: '111@qq.com',
          address: '山东省青岛市栈桥路3号',
          phone: '13479787987',
          skill: 'vue',
          decs: '我会vue'
        }, {
          id: '04',
          name: '甄有钱',
          age: '33',
          email: '899@qq.com',
          address: '深圳市福田区华富路2号',
          phone: '18898912343',
          skill: 'vue',
          decs: '我会vue'
        }]
      }
    },
    methods: {
      handleClick(row) {
        console.log(row);
      },
      handleDelete(index, rows) {
        rows.splice(index, 1);
      }
    }
  }

</script>
<style scoped>
  .btn{
    float: right;
    margin: 10px 50px 10px 0;
  }
</style>
