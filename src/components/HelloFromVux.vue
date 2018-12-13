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
		<div style="padding:15px;">
			<a id="ibangkf" href="http://www.ibangkf.com">网站客服</a>
			<script type="text/javascript" src="http://c.ibangkf.com/i/c-hemes1314.js"></script>
		</div>
  </div>
</template>

<script>
import { Group, Cell, XInput, XButton } from 'vux'

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
