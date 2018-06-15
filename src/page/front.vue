<template>
    <div class="main" >
        <div class="hello" id="hello">
            <hello></hello>
        </div>

    </div>
</template>
<script>
import hello from "../components/Hello.vue";
import headerFront from "../components/header/headerFront.vue";
import { eventHub } from "../config/eventHub.js";
export default {
  components: {
    hello
  },
  data() {
    return {};
  },
  methods: {
    changeMenu() {
      let full = false;
      let menu_front = document.getElementById("menu-front");
      let single_page_con = document.getElementById("single-page-con");
      let header_front = document.getElementById("header-front");
      if (menu_front.style.display == "none") {
        menu_front.style.display = "block";
        menu_front.style.width = "240px";
        single_page_con.style.paddingLeft = "240px";
        header_front.style.display = "block";
        header_front.style.height = "64px";
        single_page_con.style.paddingTop = "64px";
      } else {
        full = true;
        menu_front.style.display = "none";
        menu_front.style.width = "2px";
        single_page_con.style.paddingLeft = "2px";
        header_front.style.display = "none";
        header_front.style.height = "2px";
        single_page_con.style.paddingTop = "2px";
      }
      if (full) {
        document.onmousemove = function(e) {
          if (e.pageY < 40) {
            header_front.style.display = "block";
            header_front.style.height = "64px";
            single_page_con.style.paddingTop = "64px";
          } else {
            header_front.style.display = "none";
            header_front.style.height = "2px";
            single_page_con.style.paddingTop = "2px";
          }
        };
      } else {
        document.onmousemove = function(e) {
          header_front.style.display = "block";
          header_front.style.height = "64px";
          single_page_con.style.paddingTop = "64px";
        };
      }
    },
    hideMenu(){
        eventHub.$emit("hide-menu");
    }
  }
};
</script>
<<style lang="less">
    .main{
        position: relative;
        width: 100%;
        height: 100%;
        .sidebar-menu-front{
            position: fixed;
            height: 100%;
            width: 240px;
            top: 64px;
            left: 0;
            z-index: 1010;
            background-color: #fff;
            z-index:99;
            box-shadow: 4px 0 8px 0 #e5e5e5;
            .menu-show,.menu-hide{
                position: absolute;
                top: 40%;
                right: -13px;
                background: #fff;
                width: 13px;
                height: 45px;
                .ivu-icon{
                    line-height: 45px;
                    color: #7b7b7b;
                    width:15px;
                    text-align:center;
                }

            }
            .menu-show{display:none;}
        }
        &-header-con{
            box-sizing: border-box;
            position: fixed;
            display: block;
            width: 100%;
            height: 60px;
            z-index: 1000;
            box-shadow: 0 2px 1px 1px rgba(100,100,100,.1);

        }
        &-menu-left{
            background: #464c5b;
            height: 100%;
        }
        .single-page-con{
            box-sizing: border-box;
            padding-top: 64px;
            padding-left: 240px;
            background-color: #F5F6FA;
            z-index: -1;
            .single-page{
                margin: 10px;
            }

        }

    }
    .logo-con{
        padding: 8px;
        img{
            width: 100%;
        }
    }
.modalInput{
  margin-bottom:10px;
  text-align:left;
  position: relative;
  .icon-search {
      width: 32px;
      height: 32px;
      line-height: 32px;
      font-size: 16px;
      text-align: center;
      color: #80848f;
      position: absolute;
      left: 16px;
      z-index: 3;
      margin-top: 1px;
      -webkit-transform: scale(0.5);
      -ms-transform: scale(0.5);
      transform: scale(0.55);
  }
  .ivu-input{
    border: 1px solid #fff;
    color: #222;
    background-color: #f5f6fa;
    padding-left: 50px;
    height: 36px;
    font-size: 14px;
  }
}

</style>
