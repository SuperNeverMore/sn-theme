<template>
  <div>
    <div class="day">
      <h1>test</h1>
      <p>A vue project.</p>
      <p><a href="https://www.timecamp.com/">https://www.timecamp.com/</a></p>
      <br/>
      <button type="button" @click="btnClick1" value="点击我">red</button>
      <button type="button" @click="btnClick" value="点击我" class="btn-warn " v-show="warn1">warn</button>
      <button type="button" @click="btnClick" value="点击我" class="btn-accessory " v-show="warn2">warn</button>
      <br/><br/>
      <button type="button" @click="btnClick2" value="点击我" class="btn-primary large">purple</button>
      <button type="button" @click="btnClick2" value="点击我" class="btn-primary">purple</button>
      <button type="button" @click="btnClick2" value="点击我" class="btn-primary small">purple</button>
      <br/><br/>
      <input type="text" class="large">
      <input type="text" class="">
      <input type="text" class="small">
    </div>
    <div class="night">
      <h1>test</h1>
      <p>A vue project.</p>
      <button type="button" @click="btnClick" value="点击我">sdsdsd</button>
      <button type="button" class="btn2" @click="btnClick" value="点击我">sdsdsd</button>
      <button type="button"  class="btn-primary" @click="btnClick" value="点击我">sdsdsd</button>
      <button type="button" @click="btnClick" value="点击我" class="btn-warn">warn</button>
      <input type="text" class="large">
      <p>一个快速、可靠、安全的依赖管理工具</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data: function() {
      return {
        warn1: true,
        warn2: true
      };
    },
    methods: {
      btnClick() {
        alert('click');
      },
      btnClick1() {
        this.warn1 = !this.warn1;
      },
      btnClick2() {
        this.warn2 = !this.warn2;
      }
    }
  };
</script>
<style lang="less" >
  @import '../../static/styles/common.less';
  @back: @base-color;
  .day{
    ::selection{
      background:#1c1c1c;
      color:#ffffff;
    }
    width:100%;
    display:inline-block;
    padding:40px;
  }
  .night{
    ::selection{
    }
    width:100%;
    display:inline-block;
    padding:40px;
    background-color: #1c1c1c;
    color: #ffffff;
    button{
      background-color: @dark-background-color;
      &.btn-warn{
        background: #EE3133;
        @back:#EE3133;
        &:hover{
          background-color: lighten(@back, 10%);
          /*background-color: #d62c2e;*/
        }
      }
      &:hover{
        background-color: lighten(#35b344, 10%);
        /*background-color: #35b344;*/
      }
      &.btn2{
        background-color: transparent;
        border: 1px solid #04AA51;
        color: #04AA51;
      }
      &.btn-primary{
        border: 1px solid #d8d8d8;
        color: #d8d8d8;
        background-color: transparent;
        &:hover{
          .btn2;
          transform: scale(1, 1);
        }
      }
    }
    p{
      color:@dark-p-color;
    }
    input{
      background-color: transparent;
      border: 1px solid #d8d8d8;
      color: #d8d8d8;
    }
  }

</style>