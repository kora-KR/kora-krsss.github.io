---
home: true
heroImage: /images/KR.png
# actionText: 博客开发 →
# actionLink: guide.html

footer: MIT Licensed | Copyright © 2019-present Kora Run
---

<home/>

<style lang="stylus">
.home .hero img
    width: 240px
    box-shadow: 0 0 15px #999
    border-radius: 50%
#container, #container>a
  display: flex
  justify-content: space-around
  align-items: center
  width: 100%
  height: 100px
  color: #222
#container>a
    position: relative
    top: 0
    left: 0
    width: 120px
    justify-content: center
    cursor: pointer
    img
        margin-right: 10px
        width: 30px
        height: auto
        border-radius: 50%
        background: #eee
    .scan
        position: absolute
        top: -20px
        left: 4px
        z-index: 9999
        width: 150px
        height: auto
        border-radius: 0
        opacity: 0
        transition: all 1.4s
        border: 1px solid #eee
        border-radius: 10px
    span
        font-size: .9em
#container>.resume
    animation: jump 1.3s linear infinite

@keyframes jump{
0%{
    transform:rotate(0deg);
}
20% {
    transform:rotate(3deg);
}
40% {
    transform:rotate(-3deg);
}
60% {
    transform:rotate(3deg);
}
80% {
    transform:rotate(-3deg);
}
100% {
    transform:rotate(0deg);
}
}
</style>
<div id="container">
<!-- #### Vue <Badge text="git"/> -->
    <a href='https://github.com/kora-KR' target='_blank'>
        <img src='https://github.githubassets.com/images/icons/emoji/octocat.png'/>
        <h5>GitHub</h5>
    </a>
    <a href='https://gitee.com/' target='_blank'>
        <img src='https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=1081188092,2818074614&fm=26&gp=0.jpg'/>
        <h5>码云中国</h5>
    </a>
    <a href='https://www.zhihu.com/people/keycode/activities' target='_blank'>
        <img src='https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559284656478&di=93d472c7922dda1a25c47e719980e694&imgtype=0&src=http%3A%2F%2Fi0.hdslb.com%2Fbfs%2Fface%2Fda9963b27ae87094c53eb0a2973b013a50857db3.jpg'/>
        <h5>知乎</h5>
    </a>
    <a class='resume'>
        <img src='./.vuepress/public/images/resume.png'/>
        <h5>简历</h5>
    </a>
      <a id='wx'>
        <img src='./.vuepress/public/images/wx.jpg' class='scan' id='scan'/>
        <img src='https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1559284880347&di=94fa6d2b0258329ca5dc55f2d35fe874&imgtype=0&src=http%3A%2F%2Fwww.sj520.cn%2Fsc%2Fima%2Fweixin_sj520_27.jpg'/>
        <h5>微信</h5>
    </a>
</div>

<script>
window.onload = function() {
    function $(id) { return document.getElementById(id) }

    $('wx').onmouseover = function() {
        $('scan').style = 'top: -90px; opacity: 1'
    }

    $('wx').onmouseout  = function() {
        $('scan').style = ''
    }
}
</script>