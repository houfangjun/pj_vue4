<template>
    <!-- <div class="common-layout"> -->
      <el-container class="all_content">
        <el-header>
            <div class="top_statement">
                <el-text class="m-1">{{ statement1 }}</el-text>
                <el-button :size="large" style="background-color: rgb(38, 166, 154);">
                <div @click="get_extra_time" style="color: white;">购买/续费</div>
                <!-- <el-icon><Edit />123</el-icon> -->
                    <el-icon :size="27"><Edit /></el-icon>

                </el-button>
            </div>
            <el-text>{{ statement2 }}</el-text>
        </el-header>

        <el-container>
          <el-aside width="50%" style="background-color: green;">
            <el-card>
                <el-divider />
                    <el-text > 有效期至 </el-text>    
                    <el-text> {{ expiration_date }}  </el-text>
                    <el-text>({{ extra_time }})</el-text>
                <el-divider />
                <el-divider />
            </el-card>
          </el-aside>

          <el-main style="background-color: yellow;">
            
        </el-main>
        </el-container>
      </el-container>
    <!-- </div> -->
  </template>

<script setup>
import { User } from '@element-plus/icons-vue'
const statement1 = '每个人的FAST的模式使用时间是有限的, 如果FAST模式用完, 可以单独购买额度'
const statement2 = "晚上12点后可能会升级维护, 持续半小时左右. 遇到任何错误或BUG请向客服反馈，9点到24点保证可以用fast模式，0点到9点fast模式不保证，使用人员比较少，relax模式出图也很快"
const expiration_date = "2024-10-23"
const extra_time = ""

const get_extra_time = () =>{
    console.log('带飞汝者德华');
}
</script>

<style scoped>
.el-icon{
    color: white;
    /* background-color: white; */
}
.el-aside{
    height: auto;
}
.all_content{
    height: 800px; 
    width: 100%;
    background-color: black;
}

.el-header{
    background-color: yellowgreen;
    /* background-color: white; */
    height: 80px;
    color: white;
    color: gray;
}
</style>