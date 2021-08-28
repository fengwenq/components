<!--
 * @Author: your name
 * @Date: 2021-08-27 17:00:23
 * @LastEditTime: 2021-08-28 17:00:46
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \components\vue\components\src\components\button\index.vue
-->
<template>
    <div class="custom_button">
         <button :class="[
                   $style.fw_button,
                   circle ? $style.is_circle : null
                ]"
                :type="type"
                :autofocus="autofocus"
                :style="{background:bg,color,fontSize:fs,fontWeight:fw,width}"
         >
            <slot></slot>     
        </button> 
    </div>
</template>
<script>
/**
 * @Description 按钮组件
 * @property {String} bg 按钮背景颜色
 * @property {String} color 按钮颜色
 * @property {String} fs 按钮字体大小
 * @property {String} fw 按钮字体粗细
 * @property {String} width 图标宽度
 * @property {Boolean} circle 圆角按钮
 * @property {String} type 按钮类型
 * @property {Boolean} autofocus 进入页面获取按钮焦点
  */
export default {
    name:'Button',
    props:{
        type:String,
        autofocus:Boolean,
        circle:{
            type:Boolean,
            default:true
        },
        bg:{
           type:String,
           default:'#fff'
        },
        color:{
           type:String,
           default:'#606266'
        },
        fs:{
           type:String,
           default:'14px'
        },
        fw:{
           type:String,
           default:'500'
        },
        width:{
           type:String,
           default:'100%'
        }
    },
    mounted(){
        console.log(this.$style,'style')
    }
}
</script>
<style lang="scss" module>
  .fw_button{
      line-height: 1;
      padding: 12px 20px;
      margin: 0;
      border: 1px solid #dcdfe6;
      border-radius: 4px;
      outline: none;
  }
  .is_circle{
      border-radius: 100px;
  }
</style>