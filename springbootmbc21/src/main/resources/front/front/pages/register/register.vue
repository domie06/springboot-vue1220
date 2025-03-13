<template>
<view class="content">
	<view class="box" :style='{"minHeight":"100vh","width":"100%","padding":"520rpx 20rpx 80rpx","background":"url(http://codegen.caihongy.cn/20221223/fd8bb992964f4e2d84490fcbbdea7b14.gif) no-repeat center -200rpx / 100% auto,#fff","height":"100%"}'>
		<view :style='{"padding":"40rpx 40rpx","boxShadow":"0px 0px 0px #ddd","borderRadius":"24rpx","background":"#fff","display":"block","width":"100%","height":"auto"}'>
			<image :style='{"width":"160rpx","margin":"0 auto 24rpx auto","borderRadius":"8rpx","display":"none","height":"160rpx"}' src="http://codegen.caihongy.cn/20201114/7856ba26477849ea828f481fa2773a95.jpg" mode="aspectFill"></image>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='chujiezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.chujiezhanghao"  type="text"  class="uni-input" name="" placeholder="出借账号" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='chujiezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.mima" type="password"  class="uni-input" name="" placeholder="密码" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='chujiezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}' v-model="ruleForm.mima2" type="password" class="uni-input" name="" placeholder="确认密码" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='chujiezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.chujiexingming"  type="text"  class="uni-input" name="" placeholder="出借姓名" />
			</view>
            <view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='chujiezhe'" @tap="chujiezhetouxiangTap" class="">
                <view>请上传头像</view>
                <image :style='{"border":"0px solid #ccc","width":"200rpx","borderRadius":"16rpx","objectFit":"cover","display":"block","height":"160rpx"}' v-if="ruleForm.touxiang" class="avator" :src="baseUrl+ruleForm.touxiang" mode=""></image>
                <image :style='{"border":"0px solid #ccc","width":"200rpx","borderRadius":"16rpx","objectFit":"cover","display":"block","height":"160rpx"}' v-else class="avator" src="../../static/gen/upload.png" mode=""></image>
            </view>
			<picker :style='{"boxShadow":"0px 0px 0px #2c77cb","margin":"24rpx 0 24rpx 0","borderColor":"#1bccba","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='chujiezhe'"  @change="chujiezhexingbieChange" :value="chujiezhexingbieIndex" :range="chujiezhexingbieOptions">
				<view :style='{"width":"100%","padding":"0 24rpx","lineHeight":"80rpx","fontSize":"28rpx","color":"#767676"}' class="uni-input">{{ruleForm.xingbie?ruleForm.xingbie:"请选择性别"}}</view>
			</picker>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='chujiezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.shoujihaoma"  type="text"  class="uni-input" name="" placeholder="手机号码" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.jieyuezhanghao"  type="text"  class="uni-input" name="" placeholder="借阅账号" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.mima" type="password"  class="uni-input" name="" placeholder="密码" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}' v-model="ruleForm.mima2" type="password" class="uni-input" name="" placeholder="确认密码" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.jieyuexingming"  type="text"  class="uni-input" name="" placeholder="借阅姓名" />
			</view>
            <view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" @tap="jieyuezhetouxiangTap" class="">
                <view>请上传头像</view>
                <image :style='{"border":"0px solid #ccc","width":"200rpx","borderRadius":"16rpx","objectFit":"cover","display":"block","height":"160rpx"}' v-if="ruleForm.touxiang" class="avator" :src="baseUrl+ruleForm.touxiang" mode=""></image>
                <image :style='{"border":"0px solid #ccc","width":"200rpx","borderRadius":"16rpx","objectFit":"cover","display":"block","height":"160rpx"}' v-else class="avator" src="../../static/gen/upload.png" mode=""></image>
            </view>
			<picker :style='{"boxShadow":"0px 0px 0px #2c77cb","margin":"24rpx 0 24rpx 0","borderColor":"#1bccba","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","borderStyle":"solid","height":"auto"}' v-if="tableName=='jieyuezhe'"  @change="jieyuezhexingbieChange" :value="jieyuezhexingbieIndex" :range="jieyuezhexingbieOptions">
				<view :style='{"width":"100%","padding":"0 24rpx","lineHeight":"80rpx","fontSize":"28rpx","color":"#767676"}' class="uni-input">{{ruleForm.xingbie?ruleForm.xingbie:"请选择性别"}}</view>
			</picker>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.shoujihaoma"  type="text"  class="uni-input" name="" placeholder="手机号码" />
			</view>
			<view :style='{"width":"100%","margin":"0 0 40rpx 0","height":"auto"}' v-if="tableName=='jieyuezhe'" class="uni-form-item uni-column">
				<input :style='{"padding":"0px 24rpx","boxShadow":"0px 0px 0px #2c77cb","margin":"0px","borderColor":"#1bccba","color":"#333","borderRadius":"0px","background":"none","borderWidth":"0 0 2rpx","width":"100%","fontSize":"28rpx","borderStyle":"solid","height":"80rpx"}'  v-model="ruleForm.jine"  type="text"  class="uni-input" name="" placeholder="金额" />
			</view>
			<button :style='{"padding":"0px","boxShadow":"0px 4rpx 12rpx #82d1e8","margin":"60rpx auto 24rpx","borderColor":"#ef6d0d","color":"#fff","display":"block","borderRadius":"24rpx","background":"linear-gradient(90deg, rgba(27,192,241,1) 0%, rgba(27,206,179,1) 100%),#1bceb3","borderWidth":"0 0 0px","width":"60%","lineHeight":"80rpx","fontSize":"32rpx","borderStyle":"solid","height":"80rpx"}' class="btn-submit" @tap="register" type="primary">注册</button>
		</view>
	</view>
</view>
</template>

<script>
	export default {
		data() {
			return {
                chujiezhexingbieOptions: [],
                chujiezhexingbieIndex: 0,
                jieyuezhexingbieOptions: [],
                jieyuezhexingbieIndex: 0,
				ruleForm: {
                chujiezhanghao: '',
                mima: '',
                chujiexingming: '',
                touxiang: '',
                xingbie: '',
                shoujihaoma: '',
                shidejine: '',
                jieyuezhanghao: '',
                mima: '',
                jieyuexingming: '',
                touxiang: '',
                xingbie: '',
                shoujihaoma: '',
                jine: '',
				},
				tableName:""
			}
		},
        computed: {
            baseUrl() {
                return this.$base.url;
            }
        },
		async onLoad() {
			let res = [];
			let table = uni.getStorageSync("loginTable");
            this.tableName = table;

                        // 自定义下拉框值
			if(this.tableName=='chujiezhe'){
                this.chujiezhexingbieOptions = "男,女".split(',');
				this.ruleForm.xingbie=this.chujiezhexingbieOptions[0]
			}
                        // 自定义下拉框值
			if(this.tableName=='jieyuezhe'){
                this.jieyuezhexingbieOptions = "男,女".split(',');
				this.ruleForm.xingbie=this.jieyuezhexingbieOptions[0]
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
					// document.querySelectorAll('.uni-input .uni-input-input').forEach(el=>{
					//   el.style.backgroundColor = this.registerFrom.content.input.backgroundColor
					// })
				})
			},
			// 获取uuid
			getUUID () {
				return new Date().getTime();
			},
			// 注册
			async register() {
                if(`chujiezhe` == this.tableName && (this.ruleForm.mima!=this.ruleForm.mima2)){
                    this.$utils.msg(`两次密码输入不一致`);
                    return
                }
				if(`chujiezhe` == this.tableName && this.ruleForm.shoujihaoma&&(!this.$validate.isMobile(this.ruleForm.shoujihaoma))){
					this.$utils.msg(`手机号码应输入手机格式`);
					return
				}
				if(`chujiezhe` == this.tableName && this.ruleForm.shidejine&&(!this.$validate.isIntNumer(this.ruleForm.shidejine))){
					this.$utils.msg(`实得金额应输入整数`);
					return
				}
                if(`jieyuezhe` == this.tableName && (this.ruleForm.mima!=this.ruleForm.mima2)){
                    this.$utils.msg(`两次密码输入不一致`);
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
				await this.$api.register(`${this.tableName}`, this.ruleForm);
				this.$utils.msgBack('注册成功');;
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
