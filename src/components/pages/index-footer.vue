<template>
  <div class="index-footer">
    <el-row>
      <el-col :span="21" :offset="1">
        <el-row style="margin-top: 5px;text-align: center;">
          <hr />
          <p style="color: #999;font-size: 12px;">
            © 2023 二手交易系统 版权所有
          </p>
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<script>
    export default {
      name: "index-footer",
      data(){
          return{
            indexFooterMyElRow1:true,
            indexFooterMyElRow2:false,
            indexFooterMyElRow3:false,
          }
      },
      methods:{
        indexFooterMyElRowChange1(){
          this.indexFooterMyElRow1 = true;
          this.indexFooterMyElRow2 = false;
          this.indexFooterMyElRow3 = false;
          this.indexFooterMyElRowChangeActive("index-footer-my-li-1");
        },
        indexFooterMyElRowChange2(){
          this.indexFooterMyElRow1 = false;
          this.indexFooterMyElRow2 = true;
          this.indexFooterMyElRow3 = false;
          this.indexFooterMyElRowChangeActive("index-footer-my-li-2");
        },
        indexFooterMyElRowChange3(){
          this.indexFooterMyElRow1 = false;
          this.indexFooterMyElRow2 = false;
          this.indexFooterMyElRow3 = true;
          this.indexFooterMyElRowChangeActive("index-footer-my-li-3");
        },
        indexFooterMyElRowChangeActive(id){
          $("#index-footer-my-li-1").removeClass("active");
          $("#index-footer-my-li-2").removeClass("active");
          $("#index-footer-my-li-3").removeClass("active");
          $("#"+id).addClass("active");
        }
      }
    }
</script>

<style scoped>
  .index-footer a{
    text-decoration: none;
    font-size: 14px;
    color: #999;
  }
  .index-footer ul>li>a{
    font-weight: bold;
  }
  .index-footer{
    margin-top: 30px;
  }
</style>
