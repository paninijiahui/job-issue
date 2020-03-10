<template>
  <div class="ent_form">

    <div class="form_banner">
      <img src="../assets/images/form_banner.jpg" alt="">
      <p class="form_title">【心职】企业注册申请</p>
    </div>

    <div class="form_field">
      <p class="form_field_label">企业注册码</p>
      <input type="text" class="form_value_input" placeholder="企业注册后获得的六位随机数字">
    </div>
    <div class="form_field">
      <p class="form_field_label">企业名称</p>
      <input type="text" class="form_value_input" placeholder="如：宁波智士网络技术有限公司">
    </div>
    <div class="form_field">
      <div class="form_field_label01">
        <p class="title_node">公司对外简称</p>
        <p class="field_note_fade">&nbsp 0/1~5</p>
      </div>
      <input type="text" class="form_value_input" placeholder="如：智士网络">
    </div>

    <hr class="line">
    <div class="form_field">
      <div class="form_field_label01">
        <p class="title_node">职位名称</p>
        <p class="field_note_fade">&nbsp 0/2~10</p>
      </div>
      <input type="text" class="form_value_input" >
    </div>

    <div class="form_field">
      <div class="form_field_label01">
        <p class="title_node">职能职业</p>
        <p class="field_note_fade">&nbsp 0/2~10</p>
      </div>
      <input type="text" class="form_value_input" >
    </div>
    <div class="form_field">
      <p class="form_field_label">工作类型</p>
      <input type="text" class="form_value_input" placeholder="全职">
    </div>
    <div class="form_field">
      <div class="form_field_label01">
        <p class="title_node">招聘人数</p>
        <p class="field_note_fade">&nbsp 请输入1~1000的数字</p>
      </div>
      <input type="text" class="form_value_input" placeholder="人" style="text-align: right">
    </div>
    <div class="form_field">
      <!-- <p class="form_field_label01">公司对外简称 <br />-->
      <div class="form_field_label01">
        <p class="title_node">职位描述</p>
        <p class="field_note_light">职位的详细内容和要求</p>
      </div>
      <input type="text" class="form_value_input02" placeholder="注意：要求中请勿填写涉及歧视的内容，例如：残疾，乙肝等">
    </div>

    <div class="form_field">
      <div class="upload_field">
          <p class="form_field_label">工作薪资最低</p>
          <p class="salary_note_light">注：请输入月薪范围，最大薪资不能<br />超过最小薪资的3倍。如：3-6千元 </p>
          <p class="field_note_fade">请输入3~100的数字</p>
      </div>
      <input class="kuang01" type="text">
      <p class="salary_label">— 最高</p> <br />
      <p class="salary_note_fade">请输入3~100的数字</p>
      <input class="kuang02" type="text">
   <!--   <p class="field_note_fade">支持 jpg,png,gif,bmp,psd,tiff等</p>-->
    </div>
    <div class="form_field">
      <p class="form_field_label">职位福利</p>
      <input type="text" class="form_value_input" placeholder="如：提供住宿，缴纳五险，缴纳五险一金">
    </div>
    <div class="form_field">
      <p class="form_field_label">工作经验</p>
      <input type="text" class="form_value_input" placeholder="不限">
    </div>
    <div class="form_field">
      <div class="form_field_label01">
        <p class="title_node">学历要求</p>
        <p class="field_note_light">最低学历要求</p>
      </div>
      <input type="text" class="form_value_input">
    </div>
    <div class="form_field">
      <p class="form_field_label">其他要求</p>
      <input type="text" class="form_value_input" placeholder="如：技能、证书、操作系统等">
    </div>
    <div class="form_field">
      <!-- <p class="form_field_label01">公司对外简称 <br />-->
      <div class="form_field_label01">
        <p class="title_node">工作地点</p>
      </div>
      <div>
        <input type="text" class="form_input" placeholder="中国">
        <input type="text" class="form_input">
        <br />
        <input type="text" class="form_value_input01" placeholder="如：智士网络（1~5个字）">
      </div>
    </div>
    <div class="form_field">
      <p class="form_field_label">面试地点</p>
      <input  type="radio" id="place01" name="place" value="同工作地点" v-model="place">
      <label for="place01">同工作地点</label>
      <input class="form_radio" type="radio" @click="isUser = !isUser" id="place02" name="place" value="其他" v-model="place">
      <label for="place02">其他</label>
    </div>
    <div class="form_field">
      <p class="form_field_label">面试安排</p>
       <input type="checkbox" value="周一" v-model="week">周一
       <input class="form_checkbox" type="checkbox" value="周二" v-model="week"><p>周二</p>
       <input class="form_checkbox" type="checkbox" value="周三" v-model="week"><p>周三</p>
       <input class="form_checkbox" type="checkbox" value="周四" v-model="week"><p>周四</p>
        <!--<input class="form_checkbox" type="checkbox" value="周五" v-model="week"><p>周五</p>
        <input class="form_checkbox" type="checkbox" value="周六" v-model="week"><p>周六</p>
        <input class="form_checkbox" type="checkbox" value="周日" v-model="week"><p>周日</p>
        <input class="form_checkbox" type="checkbox" value="周日" v-model="week"><p>节假日除外</p>-->
    </div>

    <div class="form_field">
      <p class="form_field_label">开始面试</p>
      <input class="time01" type="text">
      <p class="form_field_label">结束面试</p>
      <input class="time02" type="text">
    </div>
    <div class="form_field">
      <p class="form_field_label">面试联系人</p>
      <div class="insert_icon">
        <i class="input_icon name_icon"></i>
        <input type="text" class="form_value_input" placeholder="只支持一位联系人">
      </div>
    </div>

    <div class="form_field">
      <p class="form_field_label">联系人手机</p>
      <div class="insert_icon">
        <i class="input_icon phone_icon"></i>
        <input type="text" class="form_value_input" placeholder="只支持一个手机号码">
      </div>
    </div>
    <div class="form_field">
      <!-- <p class="form_field_label01">公司对外简称 <br />-->
      <div class="form_field_label01">
        <p class="title_node">面试备注</p>
        <p class="field_note_light">面试安排及特别说明事项</p>
      </div>
      <input type="text" class="form_value_input02" placeholder="如：周一到周五9点到12点可面试，须携带本人身份证">
    </div>

  </div>
</template>

<script>
  export default {
    name: "issue",
    data() {
      return {
        place: '',
        week: ''
      }
    }
  }
</script>

<style scoped>
  .upload_field { /**上传图片备注容器**/
    width: 25%;
  }
  .upload_field .form_field_label{ /**单独设置上传图片字段容器宽度**/
    width: 100%;
  }
  .kuang01{
    width: 100px;
    height: 30px;
    border:1px solid #ddd;
    font-size: 14;
    line-height: 30px;
    outline: none;
    box-shadow: none;
    box-sizing: border-box;
    padding: 0 10px;
    margin-left: 100px;
  }
  .kuang02{
    width: 100px;
    height: 30px;
    border:1px solid #ddd;
    font-size: 14;
    line-height: 30px;
    outline: none;
    box-shadow: none;
    box-sizing: border-box;
    padding: 0 10px;
    margin-left: -20px;
  }
  .salary_label{ /**表单字段名**/
    font-size: 16px;
    color: #333;
    /*width: 25%;*/
    height: 28px;
    margin-left: 50px;
  }
  .salary_label::after{ /**字段名必填标志**/
    content: "*";
    color:#da2824;
    margin-left:5px;
    font-size: 16px;
  }
  .salary_note_fade{ /**字段名备注样式(浅灰色)**/
    font-size: 12px;
    height: 22px;
    color: rgba(102, 102, 102, 0.7);
    margin-top: 30px;
    margin-left: -53px;
  }
  .salary_note_light{ /**字段名备注样式(深灰色)**/
    font-size: 14px;
    line-height: 22px;
    color: #666;
  }
  .form_radio {
    margin-right: 0px;
    margin-left: 150px;
  }
  .form_checkbox {
    margin-left: 50px;
    margin-right: 10px;

  }
  .time01 {
    margin-left: -180px;
    margin-right: 150px;
  }
  .time02 {
    margin-left: -180px;
  }

</style>
