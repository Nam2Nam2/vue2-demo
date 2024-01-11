<template id="tp">
  <div>
    <div><input type="text" v-bind:value="name" /></div>
    <div><input type="date" v-bind:value="birthday" /></div>
    <div><input type="text" :value="age" /></div>
    <div><input type="button" value="点我执行m1" v-on:click="m1" /></div>
    <div><input type="button" value="点我执行m2" @click="m2" /></div>
    <div>{{ count }}</div>
    <el-button>按钮</el-button>
    <div>
            <label for="">请输入姓名</label>
            <input type="text" v-model="name">
        </div>
        <div>
            <label for="">请输入年龄</label>
            <input type="text" v-model="age">
        </div>
        <div>
            <label for="">请选择性别</label>
            男 <input type="radio" value="男" v-model="sex">
            女 <input type="radio" value="女" v-model="sex">
        </div>
        <div>
            <label for="">请选择爱好</label>
            游泳 <input type="checkbox" value="游泳" v-model="fav">
            打球 <input type="checkbox" value="打球" v-model="fav">
            健身 <input type="checkbox" value="健身" v-model="fav">
        </div>
        <h2>{{fullName}}</h2>
  </div>
</template>
<script>
const options = {
  data: function () {
    return { name: "王五", birthday: "1995-05-01", age: 20, count: 0, sex:'男' , fav:['打球'],firstName: '三', lastName: '张' };
  },
  methods: {
    m1() {
      this.count++;
      console.log("m1");
    },
    m2() {
      this.count--;
      console.log("m2");
    },
  },
  computed:{
    fullName(){
        console.log('进入了 fullName')
        return this.firstName + this.lastName;
    }
  }
};
export default options;
</script>