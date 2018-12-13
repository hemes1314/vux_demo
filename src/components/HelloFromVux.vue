<template>
  <div>
    <div class="vux-demo">
      <img class="logo" src="../assets/vux_logo.png">
      <h1> </h1>
    </div>
    <group title="cell demo">
      <cell title="VUX" value="cool" is-link></cell>
    </group>
		<group title="登录">
			<x-input title="用户名" placeholder=""></x-input>
			<x-input title="密码" placeholder=""></x-input>
		</group>
		<div style="padding:15px;">
			<x-button @click.native="iconType = 'success'" type="primary">登录</x-button>
		</div>
		<div class="container">
			<ul>
				<li>信息内容一</li>
				<li>信息内容二</li>
			</ul>
		</div>
  </div>
</template>

<script>
import { Group, Cell, XInput, XButton } from 'vux'
import Limarquee from 'limarquee'
const limarquee = new Limarquee('.container')

export default {
  components: {
    Group,
    Cell,
		XInput,
		XButton
  },
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!'
    }
  },
	mounted() {
		console.log(111111);
		//this.scrollDiv();
		limarquee.render({
			direction: 'left',	// 滚动方向，可选 left / right / up / down
			loop:	-1,	      // 循环次数，-1 为无限循环
			scrolldelay:	0,	// 每次重复之前的延迟
			scrollamount:	50,	// 滚动速度，越大越快
			circular:	true,	// 无缝滚动，如果为 false， 则和 marquee 效果一样
			drag: true,	    // 鼠标可拖动
			runshort:	true,	// 内容不足是否滚动
			hoverstop: true, // 鼠标悬停暂停
			xml: false,	    // 加载 xml 文件
			inverthover: false	// 反向，即默认不滚动，鼠 标悬停滚动
		})
		console.log(2222222);
	},
	methods: {
		scrollDiv() {
			
		}
	},
}
</script>

<style>
.vux-demo {
  text-align: center;
}
.logo {
  width: 100px;
  height: 100px
}
</style>
