<template>
<view class="content">
	<view class="box" :style='{"minHeight":"100vh","padding":"160rpx 0 160rpx","borderColor":"#21d5ae","background":"url(http://codegen.caihongy.cn/20221223/869602be22f342bf8136d5a9f62af2f7.gif) no-repeat right top,url(http://codegen.caihongy.cn/20221223/a3dca8908c4c40b68f285ba0a3226a99.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/5100c3e4960949eeaacbc47dc102c484.png) no-repeat left bottom / 100% auto","borderWidth":"2rpx 0 0","width":"100%","position":"relative","borderStyle":"dashed","height":"auto"}'>
		<view :style='{"width":"100%","padding":"60rpx 40rpx","background":"none","display":"block","height":"auto"}'>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>出借账号</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}' disabled="true"  v-model="ruleForm.chujiezhanghao" placeholder="出借账号"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>密码</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'  type="password" v-model="ruleForm.mima" placeholder="密码"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>出借姓名</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'   v-model="ruleForm.chujiexingming" placeholder="出借姓名"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'" @tap="chujiezhetouxiangTap" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>头像</view>
				<image :style='{"width":"80rpx","borderRadius":"100%","objectFit":"cover","display":"block","height":"80rpx"}' v-if="ruleForm.touxiang" style="margin: 0;" class="avator" :src="baseUrl+ruleForm.touxiang" mode=""></image>
				<image :style='{"width":"80rpx","borderRadius":"100%","objectFit":"cover","display":"block","height":"80rpx"}' v-else class="avator" style="margin: 0;" src="../../static/gen/upload.png" mode=""></image>
			</view>
			<view v-if="tableName=='chujiezhe'" :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' class=" select">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">性别</view>
				<picker :style='{"width":"100%","flex":"1","height":"auto"}'  @change="chujiezhexingbieChange" :value="chujiezhexingbieIndex" :range="chujiezhexingbieOptions">
					<view :style='{"width":"100%","lineHeight":"80rpx","fontSize":"28rpx","color":"#666"}' class="uni-input picker-select-input">{{ruleForm.xingbie?ruleForm.xingbie:"请选择性别"}}</view>
				</picker>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>手机号码</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'   v-model="ruleForm.shoujihaoma" placeholder="手机号码"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>实得金额</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}' disabled="true"  v-model="ruleForm.shidejine" placeholder="实得金额"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>借阅账号</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}' disabled="true"  v-model="ruleForm.jieyuezhanghao" placeholder="借阅账号"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>密码</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'  type="password" v-model="ruleForm.mima" placeholder="密码"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>借阅姓名</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'   v-model="ruleForm.jieyuexingming" placeholder="借阅姓名"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'" @tap="jieyuezhetouxiangTap" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>头像</view>
				<image :style='{"width":"80rpx","borderRadius":"100%","objectFit":"cover","display":"block","height":"80rpx"}' v-if="ruleForm.touxiang" style="margin: 0;" class="avator" :src="baseUrl+ruleForm.touxiang" mode=""></image>
				<image :style='{"width":"80rpx","borderRadius":"100%","objectFit":"cover","display":"block","height":"80rpx"}' v-else class="avator" style="margin: 0;" src="../../static/gen/upload.png" mode=""></image>
			</view>
			<view v-if="tableName=='jieyuezhe'" :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' class=" select">
				<view :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}' class="title">性别</view>
				<picker :style='{"width":"100%","flex":"1","height":"auto"}'  @change="jieyuezhexingbieChange" :value="jieyuezhexingbieIndex" :range="jieyuezhexingbieOptions">
					<view :style='{"width":"100%","lineHeight":"80rpx","fontSize":"28rpx","color":"#666"}' class="uni-input picker-select-input">{{ruleForm.xingbie?ruleForm.xingbie:"请选择性别"}}</view>
				</picker>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>手机号码</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'   v-model="ruleForm.shoujihaoma" placeholder="手机号码"></input>
			</view>
			<view :style='{"padding":"0 20rpx 0px","boxShadow":"inset 0px 0px 0px 0px #f9edd9","margin":"0 0 32rpx","borderColor":"#e9be70","alignItems":"center","display":"flex","minHeight":"100rpx","borderRadius":"0px","borderWidth":"0px","background":"url(http://codegen.caihongy.cn/20221223/6b85fcf145f4443f8e0c6a1d35ff48d3.png) no-repeat left top / 100% auto,url(http://codegen.caihongy.cn/20221223/f37ce3301ae04b20b8b81e44b07f3934.png) no-repeat right bottom / 100% auto,url(http://codegen.caihongy.cn/20221223/1db3995025f1402b9bbef192396a51b4.png) repeat-y center center / 100% auto","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'" class="">
				<view class="title" :style='{"width":"160rpx","padding":"0 20rpx 0 0","lineHeight":"80rpx","fontSize":"28rpx","color":"#333","textAlign":"right"}'>金额</view>
				<input :style='{"border":"0","padding":"0px 24rpx","margin":"0px","color":"#666","borderRadius":"0px","flex":"1","background":"rgba(255, 255, 255, 0)","fontSize":"28rpx","height":"80rpx"}'   v-model="ruleForm.jine" placeholder="金额"></input>
			</view>
			<view :style='{"width":"100%","margin":"48rpx 0 0","justifyContent":"center","display":"flex","height":"auto"}' class="btn">
				<button @tap="update()" class="cu-btn lg" :style='{"padding":"0 40rpx","boxShadow":"2rpx 4rpx 8rpx #ccc","margin":"0 20rpx","borderColor":"#1bd0a9","color":"#111","minWidth":"200rpx","borderRadius":"0px","background":"linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(27,208,169,1) 100%)","borderWidth":"2rpx 8rpx 2rpx","width":"auto","lineHeight":"72rpx","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'>保存</button>
				<button @tap="logout()" class="cu-btn lg" :style='{"padding":"0 40rpx","boxShadow":"2rpx 4rpx 8rpx #ccc","margin":"0 20rpx","borderColor":"#aaa","color":"#333","minWidth":"200rpx","borderRadius":"0px","background":"linear-gradient(180deg, rgba(238,238,238,1) 0%, rgba(204,204,204,1) 100%),#bbb","borderWidth":"2rpx 8rpx 2rpx","width":"auto","lineHeight":"72rpx","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'>退出登录</button>
			</view>
		</view>
	</view>
</view>
</template>

<script>
	export default {
		data() {
			return {
				ruleForm: {
				},
				tableName:"",
				chujiezhexingbieOptions: [],
				chujiezhexingbieIndex: 0,
				jieyuezhexingbieOptions: [],
				jieyuezhexingbieIndex: 0,
			}
		},
		computed: {
			baseUrl() {
				return this.$base.url;
			}
		},
		async onLoad() {
			let table = uni.getStorageSync("nowTable");
			let res = await this.$api.session(table);
			this.ruleForm = res.data;
			this.tableName = table;
			// 自定义下拉框值
			if(this.tableName=='chujiezhe'){
				this.chujiezhexingbieOptions = "男,女".split(',');
				this.chujiezhexingbieOptions.forEach((item, index) => {
					if(item==this.ruleForm.xingbie) {
						this.chujiezhexingbieIndex = index;
					}
				});
			}
			// 自定义下拉框值
			if(this.tableName=='jieyuezhe'){
				this.jieyuezhexingbieOptions = "男,女".split(',');
				this.jieyuezhexingbieOptions.forEach((item, index) => {
					if(item==this.ruleForm.xingbie) {
						this.jieyuezhexingbieIndex = index;
					}
				});
			}
			this.styleChange()
		},
		methods: {
			chujiezhetouxiangTap() {
				let _this = this;
				this.$api.upload(function(res) {
					_this.ruleForm.touxiang = 'upload/' + res.file;
					_this.$forceUpdate();
				});
			},
            // 下拉变化
            chujiezhexingbieChange(e) {
                    this.chujiezhexingbieIndex = e.target.value
                    this.ruleForm.xingbie = this.chujiezhexingbieOptions[this.chujiezhexingbieIndex]
            },
			jieyuezhetouxiangTap() {
				let _this = this;
				this.$api.upload(function(res) {
					_this.ruleForm.touxiang = 'upload/' + res.file;
					_this.$forceUpdate();
				});
			},
            // 下拉变化
            jieyuezhexingbieChange(e) {
                    this.jieyuezhexingbieIndex = e.target.value
                    this.ruleForm.xingbie = this.jieyuezhexingbieOptions[this.jieyuezhexingbieIndex]
            },

            toggleTab(str) {
                this.$refs[str].show();
            },

			styleChange() {
				this.$nextTick(()=>{
					// document.querySelectorAll('. .uni-input-input').forEach(el=>{
					//   el.style.backgroundColor = this.userInfoForm.list.input.backgroundColor
					// })
				})
			},
			// 获取uuid
			getUUID () {
				return new Date().getTime();
			},
			logout() {
				uni.setStorageSync('token', '');
				this.$utils.jump('../login/login');
			},
			// 注册
			async update() {
				if(`chujiezhe` == this.tableName && this.ruleForm.shoujihaoma&&(!this.$validate.isMobile(this.ruleForm.shoujihaoma))){
					this.$utils.msg(`手机号码应输入手机格式`);
					return
				}
				if(`chujiezhe` == this.tableName && this.ruleForm.shidejine&&(!this.$validate.isIntNumer(this.ruleForm.shidejine))){
					this.$utils.msg(`实得金额应输入整数`);
					return
				}
				if(`jieyuezhe` == this.tableName && this.ruleForm.shoujihaoma&&(!this.$validate.isMobile(this.ruleForm.shoujihaoma))){
					this.$utils.msg(`手机号码应输入手机格式`);
					return
				}
				if(`jieyuezhe` == this.tableName && this.ruleForm.jine&&(!this.$validate.isIntNumer(this.ruleForm.jine))){
					this.$utils.msg(`金额应输入整数`);
					return
				}
				let table = uni.getStorageSync("nowTable");
				await this.$api.update(table, this.ruleForm);
				this.$utils.msgBack('修改成功');;
			},

		}
	}
</script>

<style lang="scss" scoped>
	.content {
		min-height: calc(100vh - 44px);
		box-sizing: border-box;
	}
</style>
