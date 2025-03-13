<template>
<div class="content">
	<div class="text" :style='{"margin":"20px auto 60px","color":"#9e8d83","textAlign":"center","background":"url(http://codegen.caihongy.cn/20221203/b5c67a11e9bc4e74b9564c42bb5b51ac.png) no-repeat left top,url(http://codegen.caihongy.cn/20221203/2f50007fbc5f49b4a2104e43b1a0ff7f.png) no-repeat right bottom","fontSize":"32px","lineHeight":"2","fontWeight":"bold","height":"auto","maxWidth":"760px"}'>欢迎使用 {{this.$project.projectName}}</div>
</div>
</template>
<script>
//0
import router from '@/router/router-static'
import * as echarts from 'echarts'
export default {
	data() {
		return {
		};
	},
  mounted(){
    this.init();
  },
  methods:{
    init(){
        if(this.$storage.get('Token')){
        this.$http({
            url: `${this.$storage.get('sessionTable')}/session`,
            method: "get"
        }).then(({ data }) => {
            if (data && data.code != 0) {
            router.push({ name: 'login' })
            }
        });
        }else{
            router.push({ name: 'login' })
        }
    },
  }
};
</script>
<style lang="scss" scoped>
    .cardView {
        display: flex;
        flex-wrap: wrap;
        width: 100%;

        .cards {
            display: flex;
            align-items: center;
            width: 100%;
            margin-bottom: 10px;
            justify-content: center;
            .card {
                width: calc(25% - 20px);
                margin: 0 10px;
                /deep/.el-card__body{
                    padding: 0;
                }
            }
        }
    }
</style>
