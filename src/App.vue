<template>
  <div id="app">
    <firstcomponent ></firstcomponent>
    <ul>
      <li class="listli" v-for="todo in todos"  @mouseover="over('鼠标从我上面滑过',$event)">
        <a><img src="./assets/logo.png"></a>
        <dl class="listdl">
          <dd>{{todo.tit}}</dd>
          <dd>{{todo.text}}<span class="money">{{todo.money}}</span></dd>
        </dl>
      </li>
    </ul>
    <windowbox></windowbox>
  </div>
</template>

<script>
  import firstcomponent from './component/firstcomponent.vue'
  import windowbox from './component/windowbox.vue'
export default {
  name: 'app',
  data () {
    return {
        txtbox: 'Hi',
        todos:[
            {
                tit:'第1--',
                text:'第一条消息',
                money:'$23'
            },
            {
                tit:'第2',
                text:'第2条消息',
                money:'$43'
            },
            {
                tit:'第3',
                text:'第3条消息',
                money:'$54'
            },
        ],
        methods:{
          over:function (message,event) {
              alert(message+event);
          }
        }
    }
  },
  components:{firstcomponent,windowbox}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.listli{
  width:200px;
  height:300px;
  background: #f0f0f0;
  border:1px solid #444;
}
.listli a{
  display: inline-block;
  width:100%;
  padding:40px;
  box-sizing:border-box;
}
.listli a img{
  display: inline-block;
  width:100%;
}
.listdl{
  padding:10px 30px;
  box-sizing:border-box;
}
  .money{
    display: inline-block;
    float: right;
    color: #912732;
    font-weight: 700;
  }
</style>
