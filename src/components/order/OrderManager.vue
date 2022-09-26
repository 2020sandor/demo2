<template>
  <div>
    <input  type="text" v-model:value="userName"></input>
    <el-button type="success" round icon="el-icon-check" v-on:click="onDeleteOrder"  circle></el-button>
  </div>

</template>

<script>
    export default {
        name: "OrderManager",
      data:function(){
          return{
            userName:""
          }
      },
      methods:{
          onDeleteOrder:function () {
            this.$message({
              message:'修改成功！',
              type:'success'
            });//query 相当于get 是明文传参
          this.$router.push({path:"/home",query:{"userName":this.userName}});
          }
      }
    }
</script>

<style scoped>

</style>
