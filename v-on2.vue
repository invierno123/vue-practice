new Vue({
  directives:{
    on2:{
      inserted(el,info){
        el.addEventListener(info.arg,info.value)
      },
      unbind(el,info){
        el.addEventListener(info.arg,info.value)
      }
    }
  },
template:`<button v-on2:click='hi'>watch</button>`,
methods:{
  hi(){
    console.log("hey")
  }
}
}).$mount("#app");
