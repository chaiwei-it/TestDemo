<template>
  <div class="goods">
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页</div>
    <div>我是首页1</div>
    <div>我是首页2</div>
    <div>我是首页3</div>
    <div>我是首页4</div>
    <div>我是首页5</div>
    <div>我是首页6</div>
    <div>我是首页7</div>
    <div>我是首页8</div>
    <div>我是首页9</div>
    <div>我是首页10</div>
    <div>我是首页11</div>
    
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
      icon: {
        normal: '//img.yzcdn.cn/icon-normal.png',
        active: '//img.yzcdn.cn/icon-active.png'
      },
      goods: {}
    };
  },

  methods: {
    formatPrice() {
      return '¥' + (this.goods.price / 100).toFixed(2);
    },

    onClickCart() {
      this.$router.push('cart');
    },

    sorry() {
      Toast('暂无后续逻辑~');
    }
  }
};
</script>

<style lang="less">
.goods {
  padding-bottom: 50px;

  &-swipe {
    img {
      width: 7.5rem;
      height: 7.5rem;
      display: block;
    }
  }

  &-title {
    font-size: 16px;
  }

  &-price {
    color: #f44;
  }

  &-express {
    color: #999;
    font-size: 12px;
    padding: 5px 15px;
  }

  &-cell-group {
    margin: 15px 0;

    .van-cell__value {
      color: #999;
    }
  }

  &-tag {
    margin-left: 5px;
  }
}
</style>
