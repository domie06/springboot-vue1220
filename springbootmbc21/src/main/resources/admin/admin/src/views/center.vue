<template>
  <div>
    <el-form
	  :style='{"padding":"30px 15px","boxShadow":"0 0px 0px #999","borderRadius":"0px","flexWrap":"wrap","background":"none","display":"flex","justifyContent":"space-between"}'
      class="add-update-preview"
      ref="ruleForm"
      :model="ruleForm"
      label-width="120px"
    >  
     <el-row>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='chujiezhe'"  label="出借账号" prop="chujiezhanghao">
          <el-input v-model="ruleForm.chujiezhanghao" readonly              placeholder="出借账号" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='chujiezhe'"  label="出借姓名" prop="chujiexingming">
          <el-input v-model="ruleForm.chujiexingming"               placeholder="出借姓名" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}' v-if="flag=='chujiezhe'" label="头像" prop="touxiang">
          <file-upload
          tip="点击上传头像"
          action="file/upload"
          :limit="3"
          :multiple="true"
          :fileUrls="ruleForm.touxiang?ruleForm.touxiang:''"
          @change="chujiezhetouxiangUploadChange"
          ></file-upload>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}' v-if="flag=='chujiezhe'"  label="性别" prop="xingbie">
          <el-select v-model="ruleForm.xingbie"  placeholder="请选择性别">
            <el-option
                v-for="(item,index) in chujiezhexingbieOptions"
                v-bind:key="index"
                :label="item"
                :value="item">
            </el-option>
          </el-select>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='chujiezhe'"  label="手机号码" prop="shoujihaoma">
          <el-input v-model="ruleForm.shoujihaoma"               placeholder="手机号码" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='chujiezhe'"  label="实得金额" prop="shidejine">
          <el-input v-model="ruleForm.shidejine" readonly              placeholder="实得金额" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='jieyuezhe'"  label="借阅账号" prop="jieyuezhanghao">
          <el-input v-model="ruleForm.jieyuezhanghao" readonly              placeholder="借阅账号" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='jieyuezhe'"  label="借阅姓名" prop="jieyuexingming">
          <el-input v-model="ruleForm.jieyuexingming"               placeholder="借阅姓名" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}' v-if="flag=='jieyuezhe'" label="头像" prop="touxiang">
          <file-upload
          tip="点击上传头像"
          action="file/upload"
          :limit="3"
          :multiple="true"
          :fileUrls="ruleForm.touxiang?ruleForm.touxiang:''"
          @change="jieyuezhetouxiangUploadChange"
          ></file-upload>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}' v-if="flag=='jieyuezhe'"  label="性别" prop="xingbie">
          <el-select v-model="ruleForm.xingbie"  placeholder="请选择性别">
            <el-option
                v-for="(item,index) in jieyuezhexingbieOptions"
                v-bind:key="index"
                :label="item"
                :value="item">
            </el-option>
          </el-select>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='jieyuezhe'"  label="手机号码" prop="shoujihaoma">
          <el-input v-model="ruleForm.shoujihaoma"               placeholder="手机号码" clearable></el-input>
        </el-form-item>
        <el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}'   v-if="flag=='jieyuezhe'"  label="金额" prop="jine">
          <el-input v-model="ruleForm.jine"               placeholder="金额" clearable></el-input>
        </el-form-item>
		<el-form-item :style='{"margin":"0 0 20px 0","flexWrap":"wrap","textAlign":"left","background":"none","display":"block","width":"100%","justifyContent":"flex-start"}' v-if="flag=='users'" label="用户名" prop="username">
			<el-input v-model="ruleForm.username" placeholder="用户名"></el-input>
		</el-form-item>
		<el-form-item :style='{"padding":"0","margin":"20px 0 0"}'>
			<el-button :style='{"cursor":"pointer","padding":"0 30px","margin":"0 20px 0 0","borderColor":"#1fbfae","color":"#fff","minWidth":"100px","outline":"none","borderRadius":"0px","background":"#7ca065","borderWidth":"0px","width":"auto","lineHeight":"40px","fontSize":"14px","borderStyle":"solid double solid double","height":"44px"}' type="primary" @click="onUpdateHandler">修 改</el-button>
		</el-form-item>
      </el-row>
    </el-form>
  </div>
</template>
<script>
// 数字，邮件，手机，url，身份证校验
import { isNumber,isIntNumer,isEmail,isMobile,isPhone,isURL,checkIdCard } from "@/utils/validate";

export default {
  data() {
    return {
      ruleForm: {},
      flag: '',
      usersFlag: false,
      chujiezhexingbieOptions: [],
      jieyuezhexingbieOptions: [],
    };
  },
  mounted() {
    var table = this.$storage.get("sessionTable");
    this.flag = table;
    this.$http({
      url: `${this.$storage.get("sessionTable")}/session`,
      method: "get"
    }).then(({ data }) => {
      if (data && data.code === 0) {
        this.ruleForm = data.data;
      } else {
        this.$message.error(data.msg);
      }
    });
    this.chujiezhexingbieOptions = "男,女".split(',')
    this.jieyuezhexingbieOptions = "男,女".split(',')
  },
  methods: {
    chujiezhetouxiangUploadChange(fileUrls) {
        this.ruleForm.touxiang = fileUrls;
    },
    jieyuezhetouxiangUploadChange(fileUrls) {
        this.ruleForm.touxiang = fileUrls;
    },
    onUpdateHandler() {
        if(this.ruleForm.touxiang!=null) {
                this.ruleForm.touxiang = this.ruleForm.touxiang.replace(new RegExp(this.$base.url,"g"),"");
        }
      if( 'chujiezhe' ==this.flag && this.ruleForm.shoujihaoma&&(!isMobile(this.ruleForm.shoujihaoma))){
        this.$message.error(`手机号码应输入手机格式`);
        return
      }
      if( 'chujiezhe' ==this.flag && this.ruleForm.shidejine&&(!isIntNumer(this.ruleForm.shidejine))){
       this.$message.error(`实得金额应输入整数`);
        return
      }
        if(this.ruleForm.touxiang!=null) {
                this.ruleForm.touxiang = this.ruleForm.touxiang.replace(new RegExp(this.$base.url,"g"),"");
        }
      if( 'jieyuezhe' ==this.flag && this.ruleForm.shoujihaoma&&(!isMobile(this.ruleForm.shoujihaoma))){
        this.$message.error(`手机号码应输入手机格式`);
        return
      }
      if( 'jieyuezhe' ==this.flag && this.ruleForm.jine&&(!isIntNumer(this.ruleForm.jine))){
       this.$message.error(`金额应输入整数`);
        return
      }
      if('users'==this.flag && this.ruleForm.username.trim().length<1) {
	this.$message.error(`用户名不能为空`);
        return	
      }
      this.$http({
        url: `${this.$storage.get("sessionTable")}/update`,
        method: "post",
        data: this.ruleForm
      }).then(({ data }) => {
        if (data && data.code === 0) {
          this.$message({
            message: "修改信息成功",
            type: "success",
            duration: 1500,
            onClose: () => {
            }
          });
        } else {
          this.$message.error(data.msg);
        }
      });
    }
  }
};
</script>
<style lang="scss" scoped>
	.el-date-editor.el-input {
		width: auto;
	}
	
	.add-update-preview .el-form-item /deep/ .el-form-item__label {
	  	  padding: 0 10px 0 0;
	  	  text-shadow: 0 1px 10px #fff;
	  	  color: #666;
	  	  background: none;
	  	  font-weight: 500;
	  	  display: block;
	  	  width: 120px;
	  	  font-size: 14px;
	  	  line-height: 40px;
	  	  text-align: right;
	  	}
	
	.add-update-preview .el-form-item /deep/ .el-form-item__content {
	  margin-left: 120px;
	}
	
	.add-update-preview .el-input /deep/ .el-input__inner {
	  	  border-radius: 0px;
	  	  padding: 0 12px;
	  	  box-shadow: 0 0 0px #4b681d;
	  	  outline: none;
	  	  color: #666;
	  	  background: rgba(149,141,130,.1);
	  	  width: 400px;
	  	  font-size: 14px;
	  	  border-color: #958d82;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  height: 40px;
	  	}
	
	.add-update-preview .el-select /deep/ .el-input__inner {
	  	  border-radius: 0px;
	  	  padding: 0 10px;
	  	  box-shadow: 0 0 0px #4b681d;
	  	  outline: none;
	  	  color: #666;
	  	  background: rgba(149,141,130,.1);
	  	  width: 400px;
	  	  font-size: 14px;
	  	  border-color: #958d82;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  height: 40px;
	  	}
	
	.add-update-preview .el-date-editor /deep/ .el-input__inner {
	  	  border: 0px solid #333;
	  	  padding: 0 10px 0 30px;
	  	  color: #666;
	  	  font-size: 14px;
	  	  border-color: #958d82;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px #4b681d;
	  	  outline: none;
	  	  background: rgba(149,141,130,.1);
	  	  width: 400px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  height: 40px;
	  	}
	
	.add-update-preview /deep/ .el-upload--picture-card {
		background: transparent;
		border: 0;
		border-radius: 0;
		width: auto;
		height: auto;
		line-height: initial;
		vertical-align: middle;
	}
	
	.add-update-preview /deep/ .el-upload-list .el-upload-list__item {
	  	  border: 2px solid #ddd;
	  	  cursor: pointer;
	  	  color: #958d82;
	  	  font-size: 32px;
	  	  border-color: #958d82;
	  	  line-height: 90px;
	  	  border-radius: 0px;
	  	  background: rgba(149,141,130,.1);
	  	  width: 200px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  text-align: center;
	  	  height: 100px;
	  	}
	
	.add-update-preview /deep/ .el-upload .el-icon-plus {
	  	  border: 2px solid #ddd;
	  	  cursor: pointer;
	  	  color: #958d82;
	  	  font-size: 32px;
	  	  border-color: #958d82;
	  	  line-height: 90px;
	  	  border-radius: 0px;
	  	  background: rgba(149,141,130,.1);
	  	  width: 200px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  text-align: center;
	  	  height: 100px;
	  	}
	
	.add-update-preview .el-textarea /deep/ .el-textarea__inner {
	  	  padding: 12px;
	  	  color: #666;
	  	  font-size: 14px;
	  	  border-color: #958d82;
	  	  min-height: 120px;
	  	  border-radius: 0px;
	  	  box-shadow: 0 0 0px #4b681d;
	  	  outline: none;
	  	  background: rgba(149,141,130,.1);
	  	  width: 500px;
	  	  border-width: 1px;
	  	  border-style: solid;
	  	  height: auto;
	  	}
</style>
