<template>
  <div class="wrap">
    <article class="article">
      <div class="articleHead">
        <h1>小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了</h1>
        <div class="articleAuthor">
          <a href="javascript: void(0)" class="author">
            <div class="image">
              <img src="https://p3.pstatp.com/thumb/1a6e000bdec4dd8b32c5">
              <span></span>
            </div>
          </a>
          <div class="authorInfo">
            <p>
              <span>大爱猫咪控</span>
              <img src="https://s3b.pstatp.com/growth/mobile_detail/image/toutiaohao_tag_bc28ef080879ea46945f90a280f66c28.svg">  
            </p>
            <a class="sp">
              <span>06-20 11:54</span>
            </a>          
          </div>
          <a  class="a" href="javascript: void(0)">关注</a>
        </div>
      </div>
      <div class="articleContent">
        <div>
          <p v-for="item in list" :key="item">{{item.title}}
            <img v-lazy="item.img" v-if="item.img">
          </p>
        <div class="readMore">
          <a class='bt' @click="readMore" v-show="rm">展开全文</a>
        </div>
        <div v-show='cs'>
          <p v-for="itemMore in listMore" :key="itemMore">{{itemMore.title}}
            <img v-lazy="itemMore.img" v-if="itemMore.img">
          </p>
        </div>
        <!--
          <p>小奶喵卡住出不来</p>
          <p class="pimg"><img src="https://p3.pstatp.com/large/289100046793e88f5e5a" img_width="300" img_height="299" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了" ></p>
          <p>委屈到变形哈哈</p>
          <p>喵：出不来了，怎么办，好气哦</p>
          <p><img src="https://p3.pstatp.com/large/28900004face553ab585" img_width="300" img_height="299" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <div class="readMore">
            <a class='bt' @click="readMore" v-show="rm">展开全文</a>
          </div>
          <div v-show='cs'>
          <p>萌出血了</p>
          <p><img src="https://p3.pstatp.com/large/28920000dd2b2bc4dc8b" img_width="290" img_height="289" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <p>看到主人在拍摄，于是...</p>
          <p>喵：好尴尬哦，卖个萌好了</p>
          <p><img src="https://p3.pstatp.com/large/2897000259bf34c632da" img_width="300" img_height="299" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <p>翻了下po主的INS</p>
          <p>感受下这枚新萌猫</p>
          <p><img src="https://p3.pstatp.com/large/2893000461dab23851c4" img_width="440" img_height="440" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <p><img src="https://p3.pstatp.com/large/28920000dd2a075e8905" img_width="440" img_height="440" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <p>这是一斤？</p>
          <p><img src="https://p3.pstatp.com/large/28910004679447309eba" img_width="440" img_height="440" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <p><img src="https://p3.pstatp.com/large/289400045c67364af8d5" img_width="440" img_height="440" inline="0" alt="小奶喵卡住出不来，看到主人在拍摄，于是，喵：好尴尬哦，卖个萌好了"></p>
          <p>图自/微博/@设计系奶子</p>
          
          </div>
          -->
        </div>
      </div>
    </article>
    <!--
    <div class="bottom">
      <textarea ></textarea>

    </div>
    -->
  </div>
</template>

<script>
import Vue from 'vue'
import { Lazyload } from 'mint-ui';
Vue.use(Lazyload);
export default {
  name: 'detail',
  data () {
    return {
      list: [
        {
          title: '小奶喵卡住出不来'
        },
        {
          img: 'https://p3.pstatp.com/large/289100046793e88f5e5a'
        },
        {
          title: '喵：出不来了，怎么办，好气哦'
        },
        {
          img: 'https://p3.pstatp.com/large/28900004face553ab585'
        }],
      listMore: [
        {
          title: '萌出血了'
        },
        {
          img: 'https://p3.pstatp.com/large/28920000dd2b2bc4dc8b'
        },
        {
          title: '看到主人在拍摄，于是...'
        },
        {
          title: '喵：好尴尬哦，卖个萌好了'
        },
        {
          img: 'https://p3.pstatp.com/large/2897000259bf34c632da'
        },
        {
          title: '翻了下po主的INS'
        },
        {
          title: '感受下这枚新萌猫'
        },
        {
          img: 'https://p3.pstatp.com/large/2893000461dab23851c4'
        },
        {
          img: 'https://p3.pstatp.com/large/28920000dd2a075e8905'
        },
        {
          title: '这是一斤？'
        },
        {
          img: 'https://p3.pstatp.com/large/28910004679447309eba'
        },
        {
          img: 'https://p3.pstatp.com/large/289400045c67364af8d5'
        },
        {
          title: '图自/微博/@设计系奶子'
        }
      ],

      cs: false,
      rm: true
    }
  },
  methods: {
    readMore: function() {
      this.cs = true
      this.rm = false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.article {
  padding: 10px 14px 0  14px;
  margin-top: 12px;
  line-height: 34px;
  position: relative;
  overflow: hidden;
  background-color: #fff;
  .articleHead {
    position: relative;
    h1 {
      font-size: 24px;
      line-height: 34px;
      text-align: left;
    }
    .articleAuthor {
      margin-top: 12px;
      display: flex;
      flex-direction: row;
      align-items: center;
      a {
        color: #131313;
        .image {
          height: 36px;
          width: 36px;
          border: none;
          position: relative;
          img {
            width: 100%;
            height: 100%;
            border-radius: 32px;
            position: absolute;
            top: 0;
            left: 0;
          }
          span {
            background-color: rgba(34,34,34,.05);       
          }
        }
      }
        .authorInfo {
          padding-left: 8px;
          -webkit-box-flex: 1;
          -ms-flex-positive: 1;
          flex-grow: 1;
          p {
            
            line-height: 16px;
            font-size: 12px;
            margin-bottom: 2px;
            span {
              font-family: PingFangSC-Medium;
              font-size: 14px;
              line-height: 16px;
              color: #222121;
            }
            img {
              padding-left: 5px;
              height: 16px;
              margin-bottom: 0px;
            }
          }
          .sp {
            height: 30px;
            span {
              font-size: 12px;
              line-height: 12px;
              vertical-align: middle;
              display: inline-block;
              color: #999;
            }
          }
        }
        .a {
          background-color: #2a90d7;
          display: block;
          text-align: center;
          color: hsla(0,0%,100%,.96);
          -webkit-box-sizing: border-box;
          box-sizing: border-box;
          width: 72px;
          height: 29px;
          line-height: 29px;
          font-size: 14px;
          margin-top: 16px;
          border-radius: 6px;
        }
      }   
  }
  .articleContent {

    position: relative;
    overflow: hidden;
    clear: both;
    padding-bottom: 24px;
    p {
      word-wrap: break-word;
      color: #333;
      margin-top: 24px;
      font-size: 18px;
      line-height: 30px;
      img {
        width: 100%;
        display: block;
        margin: 4px auto;
      }
    }
  .readMore {
     text-align: center;
     position: relative;
     padding: 10px 0;
     height: 50px;
    .bt {
      display: inline-block;
      cursor: pointer;
      font-size: 16px;
      line-height: 30px;
      border-radius: 29px;
      color: #406599;
    }
    .bt:after {
      content: '';
      background-image: url(./../assets/readMore.png);
      background-size: contain;
      background-repeat: no-repeat;
      width: 18px;
      height: 12px;
      display: inline-block;
      margin-left: 16px;
    }
  }
  }
  image[lazy=loading] {
  width: 300px;
  height: 300px;
  margin: auto;
}
}
.bottom {
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 40px;
  background-color: #fff;
  border-top: 1px solid #999;
  textarea {
    font-size: 16px;
    line-height:20px;
    height: 30px;
    width: 60%;
    color: #404040;
    background-color: #f2f2f2;
    margin: 6px 0 6px 12px;
    border-radius: 24px;
    text-align: center;
  }
}
</style>