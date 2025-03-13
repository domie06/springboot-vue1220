<template>
<view class="content">
	<view :style='{"minHeight":"100vh","padding":"160rpx 0 160rpx","borderColor":"#21d5ae","background":"url(http://codegen.caihongy.cn/20221223/869602be22f342bf8136d5a9f62af2f7.gif) no-repeat right top,url(http://codegen.caihongy.cn/20221223/a3dca8908c4c40b68f285ba0a3226a99.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/5100c3e4960949eeaacbc47dc102c484.png) no-repeat left bottom / 100% auto","borderWidth":"2rpx 0 0","width":"100%","position":"relative","borderStyle":"dashed","height":"auto"}'>
		<form :style='{"width":"100%","padding":"60rpx 40rpx","background":"none","height":"auto"}' class="app-update-pv">
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">借阅编号</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.jieyuebianhao" v-model="ruleForm.jieyuebianhao" placeholder="借阅编号"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">图书编号</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.tushubianhao" v-model="ruleForm.tushubianhao" placeholder="图书编号"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">图书名称</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.tushumingcheng" v-model="ruleForm.tushumingcheng" placeholder="图书名称"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">数量</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.shuliang" v-model="ruleForm.shuliang" placeholder="数量"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">押金</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.yajin" v-model="ruleForm.yajin" placeholder="押金"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class=" select">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">归还时间</view>
				<picker :style='{"width":"100%","flex":"1","height":"auto"}' mode="date" :value="ruleForm.guihaishijian" @change="guihaishijianChange">
					<view :style='{"width":"100%","lineHeight":"80rpx","fontSize":"28rpx","color":"#666"}' class="uni-input">{{ruleForm.guihaishijian?ruleForm.guihaishijian:"请选择归还时间"}}</view>
				</picker>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">借阅账号</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.jieyuezhanghao" v-model="ruleForm.jieyuezhanghao" placeholder="借阅账号"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">出借账号</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.chujiezhanghao" v-model="ruleForm.chujiezhanghao" placeholder="出借账号"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","display":"flex","width":"100%","lineHeight":"100rpx","borderStyle":"solid","height":"auto"}' class="">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">归还备注</view>
				<input :style='{"border":"0","padding":"0px 20rpx","margin":"0px","color":"#666","borderRadius":"8rpx","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx"}' :disabled="ro.guihaibeizhu" v-model="ruleForm.guihaibeizhu" placeholder="归还备注"></input>
			</view>
			
			<!-- 否 -->
 

			
			
			<view :style='{"width":"100%","margin":"40rpx 0 0 0","justifyContent":"center","display":"flex","height":"auto"}' class="btn" >
				<button :style='{"padding":"0 40rpx","boxShadow":"2rpx 4rpx 8rpx #ccc","margin":"0 40rpx 0 0","borderColor":"#1bd0a9","color":"#111","display":"inline","minWidth":"200rpx","borderRadius":"0px","background":"linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(27,208,169,1) 100%)","borderWidth":"2rpx 8rpx 2rpx","width":"auto","lineHeight":"72rpx","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}' @tap="onSubmitTap" class="bg-red">提交</button>
			</view>
		</form>

	</view>
</view>
</template>

<script>
	import wPicker from "@/components/w-picker/w-picker.vue";
    import xiaEditor from '@/components/xia-editor/xia-editor';
	export default {
		data() {
			return {
				cross:'',
				ruleForm: {
				jieyuebianhao: '',
				tushubianhao: '',
				tushumingcheng: '',
				shuliang: '',
				yajin: '',
				guihaishijian: '',
				jieyuezhanghao: '',
				chujiezhanghao: '',
			        guihaibeizhu: '完好无损',
				shhf: '',
				ispay: '',
				},
				// 登陆用户信息
				user: {},
                ro:{
                   jieyuebianhao : false,
                   tushubianhao : false,
                   tushumingcheng : false,
                   shuliang : false,
                   yajin : false,
                   guihaishijian : false,
                   jieyuezhanghao : false,
                   chujiezhanghao : false,
                   guihaibeizhu : false,
                   sfsh : false,
                   shhf : false,
                   ispay : false,
                },
			}
		},
		components: {
			wPicker,
            xiaEditor
		},
		computed: {
			baseUrl() {
				return this.$base.url;
			},



		},
		async onLoad(options) {
            this.ruleForm.guihaishijian = this.$utils.getCurDate();
			let table = uni.getStorageSync("nowTable");
			// 获取用户信息
			let res = await this.$api.session(table);
			this.user = res.data;
			
			// ss读取
			this.ruleForm.jieyuezhanghao = this.user.jieyuezhanghao
			this.ro.jieyuezhanghao = true;



			// 如果有登陆，获取登陆后保存的userid
			this.ruleForm.userid = uni.getStorageSync("userid")
			if (options.refid) {
				// 如果上一级页面传递了refid，获取改refid数据信息
				this.ruleForm.refid = options.refid;
				this.ruleForm.nickname = uni.getStorageSync("nickname");
			}
			// 如果是更新操作
			if (options.id) {
				this.ruleForm.id = options.id;
				// 获取信息
				res = await this.$api.info(`tushuguihai`, this.ruleForm.id);
				this.ruleForm = res.data;
			}
			// 跨表
			this.cross = options.cross;
			if(options.cross){
				var obj = uni.getStorageSync('crossObj');
				for (var o in obj){
					if(o=='jieyuebianhao'){
					this.ruleForm.jieyuebianhao = obj[o];
					this.ro.jieyuebianhao = true;
					continue;
					}
					if(o=='tushubianhao'){
					this.ruleForm.tushubianhao = obj[o];
					this.ro.tushubianhao = true;
					continue;
					}
					if(o=='tushumingcheng'){
					this.ruleForm.tushumingcheng = obj[o];
					this.ro.tushumingcheng = true;
					continue;
					}
					if(o=='shuliang'){
					this.ruleForm.shuliang = obj[o];
					this.ro.shuliang = true;
					continue;
					}
					if(o=='yajin'){
					this.ruleForm.yajin = obj[o];
					this.ro.yajin = true;
					continue;
					}
					if(o=='guihaishijian'){
					this.ruleForm.guihaishijian = obj[o];
					this.ro.guihaishijian = true;
					continue;
					}
					if(o=='jieyuezhanghao'){
					this.ruleForm.jieyuezhanghao = obj[o];
					this.ro.jieyuezhanghao = true;
					continue;
					}
					if(o=='chujiezhanghao'){
					this.ruleForm.chujiezhanghao = obj[o];
					this.ro.chujiezhanghao = true;
					continue;
					}
					if(o=='guihaibeizhu'){
					this.ruleForm.guihaibeizhu = obj[o];
					this.ro.guihaibeizhu = true;
					continue;
					}
				}
            this.ruleForm.shuliang = 0;
            this.ro.shuliang = false;
			}
			this.styleChange()
		},
		methods: {
			styleChange() {
				this.$nextTick(()=>{
					// document.querySelectorAll('.app-update-pv . .uni-input-input').forEach(el=>{
					//   el.style.backgroundColor = this.addUpdateForm.input.content.backgroundColor
					// })
				})
			},

			// 多级联动参数

			guihaishijianChange(e) {
				this.ruleForm.guihaishijian = e.target.value;
				this.$forceUpdate();
			},




			getUUID () {
				return new Date().getTime();
			},
			async onSubmitTap() {

























//跨表计算判断
				var obj;
				obj = uni.getStorageSync('crossObj');
				var table = uni.getStorageSync('crossTable');
				//obj.shuliang = obj.shuliang - this.ruleForm.shuliang
                if((parseFloat(obj.shuliang) - parseFloat(this.ruleForm.shuliang))<0){
					this.$utils.msg("数量不足");
					return
				}
				if(this.ruleForm.shuliang&&(!this.$validate.isIntNumer(this.ruleForm.shuliang))){
					this.$utils.msg(`数量应输入整数`);
					return
				}
				if(this.ruleForm.yajin&&(!this.$validate.isIntNumer(this.ruleForm.yajin))){
					this.$utils.msg(`押金应输入整数`);
					return
				}
				//更新跨表属性
			       var crossuserid;
			       var crossrefid;
			       var crossoptnum;
				if(this.cross){
					var statusColumnName = uni.getStorageSync('statusColumnName');
					var statusColumnValue = uni.getStorageSync('statusColumnValue');
					if(statusColumnName!='') {
                        if(!obj) {
						    obj = uni.getStorageSync('crossObj');
                        }
						if(!statusColumnName.startsWith("[")) {
							for (var o in obj){
								if(o==statusColumnName){
									obj[o] = statusColumnValue;
								}

							}
							var table = uni.getStorageSync('crossTable');
							await this.$api.update(`${table}`, obj);
						} else {
						       crossuserid=Number(uni.getStorageSync('userid'));
						       crossrefid=obj['id'];
						       crossoptnum=uni.getStorageSync('statusColumnName');
						       crossoptnum=crossoptnum.replace(/\[/,"").replace(/\]/,"");
						}
					}
				}
				if(crossrefid && crossuserid) {
					this.ruleForm.crossuserid=crossuserid;
					this.ruleForm.crossrefid=crossrefid;
					let params = {
						page: 1,
						limit:10,
						crossuserid:crossuserid,
						crossrefid:crossrefid,
					}
					let res = await this.$api.list(`tushuguihai`, params);
					if (res.data.total >= crossoptnum) {
						this.$utils.msg(uni.getStorageSync('tips'));
						return false;
					} else {
                //跨表计算
                        if(!obj) {
                            obj = uni.getStorageSync('crossObj');
                        }
                        var table = uni.getStorageSync('crossTable');
                        obj.shuliang = parseFloat(obj.shuliang) - parseFloat(this.ruleForm.shuliang)
                        await this.$api.update(`${table}`, obj);
						if(this.ruleForm.id){
							await this.$api.update(`tushuguihai`, this.ruleForm);
						}else{
							await this.$api.add(`tushuguihai`, this.ruleForm);
						}
						this.$utils.msgBack('提交成功');
					}
				} else {
                //跨表计算
                    if(!obj) {
                        obj = uni.getStorageSync('crossObj');
                    }
                    var table = uni.getStorageSync('crossTable');
                    obj.shuliang = obj.shuliang - this.ruleForm.shuliang
                    await this.$api.update(`${table}`, obj);
					if(this.ruleForm.id){
						await this.$api.update(`tushuguihai`, this.ruleForm);
					}else{
						await this.$api.add(`tushuguihai`, this.ruleForm);
					}
					this.$utils.msgBack('提交成功');
				}
			},
			optionsChange(e) {
				this.index = e.target.value
			},
			bindDateChange(e) {
				this.date = e.target.value
			},
			getDate(type) {
				const date = new Date();
				let year = date.getFullYear();
				let month = date.getMonth() + 1;
				let day = date.getDate();
				if (type === 'start') {
					year = year - 60;
				} else if (type === 'end') {
					year = year + 2;
				}
				month = month > 9 ? month : '0' + month;;
				day = day > 9 ? day : '0' + day;
				return `${year}-${month}-${day}`;
			},
			toggleTab(str) {
				this.$refs[str].show();
			}
		}
	}
</script>

<style lang="scss" scoped>
	.content {
		min-height: calc(100vh - 44px);
		box-sizing: border-box;
	}
</style>
