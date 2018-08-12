<template>
    <div class="pd20 bg-gray">
    <div class="box">
         <el-row :gutter="24">
  <el-col :span="6">
    <el-card shadow="always">
      <div class="card-item">
        <div class="card-icon icon-money">
            <svg-icon icon-class="money" class-name="card-panel-icon" />
        </div>
        <div class="card-content">
            <div class="card-text">余额</div>
            1000.00
        </div>
      </div>
    </el-card>
  </el-col>
  <el-col :span="6">
    <el-card shadow="always">
      <div class="card-item">
        <div class="card-icon icon-coin">
            <svg-icon icon-class="slidercoin" class-name="card-panel-icon" />
        </div>
        <div class="card-content">
            <div class="card-text">余币</div>
            666
        </div>
      </div>
    </el-card>
  </el-col>
  <el-col :span="6">
    <el-card shadow="always">
      <div class="card-item">
        <div class="card-icon icon-order">
            <svg-icon icon-class="order" class-name="card-panel-icon" />
        </div>
        <div class="card-content">
            <div class="card-text">交易次数</div>
            999
        </div>
      </div>
    </el-card>
  </el-col>
  <el-col :span="6">
    <el-card shadow="always">
      <div class="card-item">
        <div class="card-icon icon-income">
            <svg-icon icon-class="income" class-name="card-panel-icon" />
        </div>
        <div class="card-content">
            <div class="card-text">今日收益</div>
            ￥999
        </div>
      </div>
    </el-card>
  </el-col>
</el-row>
    </div>
    <div class="box">
<el-row>
        <el-col :span="12">
            <el-card class="box-card">
  <div slot="header" class="clearfix">
    <span>交易记录</span>
  </div>
  <el-table
    :data="tableData"
    stripe
    style="width: 100%">
    <el-table-column
      prop="date"
      label="时间"
      width="180">
    </el-table-column>
    <el-table-column
      prop="price"
      label="价格"
      width="180">
    </el-table-column>
    <el-table-column
      prop="number"
      label="数量">
    </el-table-column>
    <el-table-column
      prop="type"
      label="类型">
    </el-table-column>
  </el-table>
</el-card>
            
            

        </el-col>
        <el-col :span="10" :offset="1">
            <el-card class="box-card">
  <div slot="header" class="clearfix">
    <span>转账记录</span>
  </div>
  <div  class="text item">
    <p>转出：200</p>
    <p>xxxxxxx-xxxxx-xxxxxxxx</p>
    <p>2018-08-12</p>
  </div>
  <div  class="text item">
    <p>转出：200</p>
    <p>xxxxxxx-xxxxx-xxxxxxxx</p>
    <p>2018-08-12</p>
  </div>
</el-card>

        </el-col>

    </el-row>
    </div>
    
    </div>
</template>
<script>
export default {
    data() {
        return {
                tableData: [{
            date: '2016-05-02',
            price: 10.89,
            number: 5,
            type: "买入",
          },{
            date: '2016-05-02',
            price: 10.89,
            number: 5,
            type: "买入",
          },{
            date: '2016-05-02',
            price: 10.89,
            number: 5,
            type: "卖出",
          },{
            date: '2016-05-02',
            price: 10.89,
            number: 5,
            type: "买入",
          },{
            date: '2016-05-02',
            price: 10.89,
            number: 5,
            type: "买入",
          }]
        }
    },
}
</script>
<style>
.bg-gray {
    background: #f0f2f5;
}
.mg30 {
    margin: 30px;
}
.pd20 {
    padding: 20px;
}
.box {
    padding-left: 4px;
    padding-right: 8px;
    margin-bottom: 30px;
}
.card-item {
    
    position: relative;
    overflow: hidden;
    cursor: pointer;
}
.card-icon {
    float: left;
    padding: 16px;
    -webkit-transition: all 0.38s ease-out;
    transition: all 0.38s ease-out;
    border-radius: 6px;
}
.card-content {
    float: right;
    font-weight: bold;
    margin-top: 25px ;
    margin-right:10px;
}
.card-panel-icon {
    font-size: 48px;
    
}
.icon-money {
    color: #f4516c;
}
.icon-money:hover {
    background-color: #f4516c;
    color:#fff;
}
.icon-coin {
    color: #E6A23C;
}
.icon-coin:hover {
    background-color: #E6A23C;
    color:#fff;
}
.icon-order {
    color: #409EFF;
}
.icon-order:hover {
    background-color: #409EFF;
    color:#fff;
}
.icon-income {
    color: #F56C6C;
}
.icon-income:hover {
    background-color: #F56C6C;
    color:#fff;
}
.card-text {
    margin-bottom: 5px;
    color: #948a8a;
}
.item {
    margin-bottom: 18px;
    border-bottom: 1px solid #ddd;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }
</style>

