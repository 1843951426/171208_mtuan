<template>
  <div class="msite">
    <!--首页头部-->
    <HeaderTop title="昌平区北七家宏福科技园(337 省道北)">
      <a class="header_search" slot="left">
        <i class="iconfont icon-xingtaiduICON_sousuo--"></i>
      </a>
      <a class="header_login" slot="right">
        <span class="header_login_text">登录|注册</span>
      </a>
    </HeaderTop>            
    <!--首页导航-->
    <nav class="msite_nav border-1px">
      <div class="swiper-container">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/1.jpg" />
              </div>
              <span>甜品饮品</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/2.jpg" />
              </div>
              <span>商超便利</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/3.jpg" />
              </div>
              <span>美食</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/4.jpg" />
              </div>
              <span>简餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/5.jpg" />
              </div>
              <span>新店特惠</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/6.jpg" />
              </div>
              <span>准时达</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/7.jpg" />
              </div>
              <span>预订早餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/8.jpg" />
              </div>
              <span>土豪推荐</span>
            </a>
          </div>
          <div class="swiper-slide">
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/9.jpg" />
              </div>
              <span>甜品饮品</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/10.jpg" />
              </div>
              <span>商超便利</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/11.jpg" />
              </div>
              <span>美食</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/12.jpg" />
              </div>
              <span>简餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/13.jpg" />
              </div>
              <span>新店特惠</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/14.jpg" />
              </div>
              <span>准时达</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/1.jpg" />
              </div>
              <span>预订早餐</span>
            </a>
            <a href="javascript:" class="link_to_food">
              <div class="food_container">
                <img src="./images/nav/2.jpg" />
              </div>
              <span>土豪推荐</span>
            </a>
          </div>
        </div>
        <!-- Add Pagination -->
        <div class="swiper-pagination"></div>
      </div>
    </nav>
    <!--首页附近商家-->
    <div class="msite_shop_list border-1px">
      <div class="shop_header">
        <ShopList/>
        <i class="iconfont icon-xuanxiang"></i>
        <span class="shop_header_title">附近商家</span>
      </div>
     
    </div>
  </div>
</template>

<script>
import HeaderTop from'../../components/HeaderTop/HeaderTop.vue'
import ShopList from'../../components/ShopList/ShopList.vue'
import Swiper from 'swiper'
import 'swiper/dist/css/swiper.min.css'
export default {
      components: {
        HeaderTop,
        ShopList
      },
      mounted () {
          new Swiper('.swiper-container', {
          pagination: {
              loop: true,
              el: '.swiper-pagination',
            },
      
        })
      }
}
</script>
<style lang="stylus" rel="stylesheet/stylus">
@import "../../common/stylus/mixins.styl"
        .msite  //首页
          width 100%
          .msite_nav
            bottom-border-1px(#e4e4e4)
            margin-top 45px
            height 200px
            background #fff
            .swiper-container
              width 100%
              height 100%
              .swiper-wrapper
                width 100%
                height 100%
                .swiper-slide
                  display flex
                  justify-content center
                  align-items flex-start
                  flex-wrap wrap
                  .link_to_food
                    width 25%
                    .food_container
                      display block
                      width 100%
                      text-align center
                      padding-bottom 10px
                      font-size 0
                      img
                        display inline-block
                        width 50px
                        height 50px
                    span
                      display block
                      width 100%
                      text-align center
                      font-size 13px
                      color #666
              .swiper-pagination
                >span.swiper-pagination-bullet-active
                  background #ffd930
          .msite_shop_list
            top-border-1px(#e4e4e4)
            margin-top 10px
            background #fff
            .shop_header
              padding 10px 10px 0
              .shop_icon
                margin-left 5px
                color #999
              .shop_header_title
                color #999
                font-size 14px
                line-height 20px
        .search  //搜索
          width 100%
          .search_form
            clearFix()
            margin-top 45px
            background-color #fff
            padding 12px 8px
            input
              height 35px
              padding 0 4px
              border-radius 2px
              font-weight bold
              outline none
              &.search_input
                float left
                width 79%
                border 4px solid #f2f2f2
                font-size 14px
                color #333
                background-color #f2f2f2
              &.search_submit
                float right
                width 18%
                border 4px solid #ffd930
                font-size 16px
                color #fff
                background-color #ffd930
        .order  //订单
          width 100%
          .order_no_login
            padding-top 140px
            width 60%
            margin 0 auto
            text-align center
            >img
              display block
              width 100%
              height 30%
            >h3
              padding 10px 0
              font-size 17px
              color #6a6a6a
            >button
              display inline-block
              background #ffd930
              font-size 14px
              color #fff
              border 0
              outline none
              border-radius 5px
              padding 10px 20px
        .profile //我的
          width 100%
          .profile-number
            margin-top 45.5px
            .profile-link
              clearFix()
              position relative
              display block
              background #ffd930
              padding 20px 10px
              .profile_image
                float left
                width 60px
                height 60px
                border-radius 50%
                overflow hidden
                vertical-align top
                .icon-person
                  background #e4e4e4
                  font-size 62px
              .user-info
                float left
                margin-top 8px
                margin-left 15px
                p
                  font-weight: 700
                  font-size 18px
                  color #fff
                  &.user-info-top
                    padding-bottom 8px
                  .user-icon
                    display inline-block
                    margin-left -15px
                    margin-right 5px
                    width 20px
                    height 20px
                    .icon-mobile
                      font-size 30px
                      vertical-align text-top
                  .icon-mobile-number
                    font-size 14px
                    color #fff
              .arrow
                width 12px
                height 12px
                position absolute
                right 15px
                top 40%
                .icon-jiantou1
                  color #fff
                  font-size 5px
          .profile_info_data
            bottom-border-1px(#e4e4e4)
            width 100%
            background #fff
            overflow hidden
            .info_data_list
              clearFix()
              .info_data_link
                float left
                width 33%
                text-align center
                border-right 1px solid #f1f1f1
                .info_data_top
                  display block
                  width 100%
                  font-size 14px
                  color #333
                  padding 15px 5px 10px
                  span
                    display inline-block
                    font-size 30px
                    color #f90
                    font-weight 700
                    line-height 30px
                .info_data_bottom
                  display inline-block
                  font-size 14px
                  color #666
                  font-weight 400
                  padding-bottom 10px
              .info_data_link:nth-of-type(2)
                .info_data_top
                  span
                    color #ff5f3e
              .info_data_link:nth-of-type(3)
                border 0
                .info_data_top
                  span
                    color #6ac20b
          .profile_my_order
            top-border-1px(#e4e4e4)
            margin-top 10px
            background #fff
            .my_order
              display flex
              align-items center
              padding-left 15px
              >span
                display flex
                align-items center
                width 20px
                height 20px
                >.iconfont
                  margin-left -10px
                  font-size 30px
                .icon-order-s
                  color #ffd930
                .icon-jifen
                  color #ff5f3e
                .icon-vip
                  color #f90
                .icon-fuwu
                  color #ffd930
              .my_order_div
                width 100%
                border-bottom 1px solid #f1f1f1
                padding 18px 10px 18px 0
                font-size 16px
                color #333
                display flex
                justify-content space-between
                span
                  display block
                .my_order_icon
                  width 10px
                  height 10px
                  .icon-jiantou1
                    color #bbb
                    font-size 10px
</style>