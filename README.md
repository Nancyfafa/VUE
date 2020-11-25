### 一、指令
1、v-cloak解决插值表达式(el:'#app',data:{num:0},)的闪动问题（原理：先隐藏，替换好值之后再显示）   
2、数据绑定指令：   
v-text没有闪动问题   
v-html填充HTML片段（存在安全隐患，本网站内部数据可以使用，来自第三方的数据不可以用）   
v-pre填充原始信息（跳过编译过程）   
3、数据响应式：   
v-once只编译一次   
4、双向数据绑定：   
v-model用户修改数据内容，input值发生变化；input值变化，进而插值表达式发生变化。<input type='text' v-model='uname'>   
MVVM设计思想   
5、事件绑定：   
v-on指令用法v-on:click='num++'，简写形式@click='num++'   
事件函数调用v-on:click='say'或者v-on:click='say()'。函数需要定义在methods中，say:function(){...}   
事件函数参数传递say("hi",$event)   
6、事件修饰符：   
.stop阻止冒泡（里层的触发事件传递到外层，触发外层事件）原来这么阻止event.stopPropagation()，VUE中v-on:click.stop='say';   
.prevent阻止默认行为v-on:click.prevent='say'   
7、按键修饰符：   
v-on:keyup.enter='say'    
自定义按键事件修饰符：全局config.keyCodes对象Vue.config.keyCodes.f1 = 112   
8、属性绑定：   
v-bind指令用法<a v-bind:href='url'></a>缩写<a :href='url'></a>   
可用于双向绑定<input v-bind:value='msg' v-on:input='msg=$event.target.value'>   
9、样式绑定：   
对象语法：<div v-bind:class="{active:isActive}"></div>   
数组语法：<div v-bind:class="[activeClass,errorClass]"></div>需要在data中声明activeClass:'active'   



### 二、细节
1、parseInt()将input中string转int   












