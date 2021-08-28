<!--
 * @Author: your name
 * @Date: 2021-08-27 09:52:22
 * @LastEditTime: 2021-08-28 17:04:23
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \components\vue\components\src\App.vue
-->
<template>
   <div>
       <h3>组件：</h3>
       <Icon name="sousuo" color="red" size="28" />
       <Icon name="renyuan" />
       <Button>点击</Button>
   </div>
</template>

<script>
import Icon from '@/components/icon/index'
import Button from '@/components/button/index'
export default {
  name: 'App',
  components: {
    Icon,
    Button
  },
  methods:{
    handleclick(e){
      console.log(e,'handleclick')
    }
  }
}
</script>

<style>
@import url('./app.scss');
@import url('./assets/font/iconfont.css');
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
