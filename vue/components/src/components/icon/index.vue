<!--
 * @Author: fwq
 * @Date: 2021-08-27 15:00:17
 * @LastEditTime: 2021-08-28 09:42:43
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \components\vue\components\src\components\icon\index.vue
-->
<template>
    <i 
        :class="'fw-icon-'+name"
        class="global" 
        :style="{color,fontSize:size+'px'}"
    ></i>
</template>
<script>

/**
 * @Description 基于字体的图标集，包含了大多数常见场景的图标
 * @property {String} name 图标名称，见示例图标集
 * @property {String} color 图标颜色
 * @property {String} size 图标字体大小
  */
export default {
    name:'Icon',
    props:['name','color','size']
}
</script>