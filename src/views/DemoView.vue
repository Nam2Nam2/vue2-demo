<template id="tp">
    <div>
      <div><input type="text" v-bind:value="name" /></div>
    </div>
  </template>
  <script>
  const options = {
    data: function () {
      return { name: "王五"};
    },
    methods: {
      m1() {
        console.log("m1");
      },
      m2() {
        console.log("m2");
      },
    },
    computed:{
      fullName(){
          console.log('进入了 fullName')
          return this.name + this.name;
      }
    }
  };
  export default options;
  </script>