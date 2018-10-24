<template>
  <div id="app">
  	<div>
  		<van-row>
  			<router-view />
  		</van-row>
  		<van-row>
	  		<van-tabbar v-model="active">
		      <van-tabbar-item info="" to="/home">
		        <span>首页</span>
		        <img
		          slot="icon"
		          slot-scope="props"
		          :src="props.active ? index.active : index.normal"
		        >
		      </van-tabbar-item>
		      <van-tabbar-item info="3" to="/cart">
		        <span>购物车</span>
		        <img
		          slot="icon"
		          slot-scope="props"
		          :src="props.active ? cart.active : cart.normal"
		        >
		      </van-tabbar-item>
		      <van-tabbar-item info=""  to="/user">
		        <span>个人中心</span>
		        <img
		          slot="icon"
		          slot-scope="props"
		          :src="props.active ? person.active : person.normal"
		        >
		      </van-tabbar-item>
		    </van-tabbar>
		   </van-row>
  	</div>
  </div>
</template>

<script>
import {
  Toast,Tabbar, TabbarItem
} from 'vant';

export default {
  components: {
    [Tabbar.name]: Tabbar,
    [TabbarItem.name]: TabbarItem
  },

  data() {
    return {
      active: 0,
      index: {
        normal: 'src/assets/images/index/index-never.png',
        active: 'src/assets/images/index/index.png'
      },
      cart: {
        normal: './images/index/cart-never.png',
        active: './images/index/cart.png'
      },
      person: {
        normal: './images/index/person-never.png',
        active: './images/index/person.png'
      },
      goods: {}
    };
  }
};
</script>

<style>
body {
  font-size: 16px;
  background-color: #f8f8f8;
  -webkit-font-smoothing: antialiased;
}
</style>
