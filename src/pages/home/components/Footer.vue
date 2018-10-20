<template>
  <div class="qn-footer">
    <div>
      <ul class="main-nav" ref="mainNav" style="height:25px">
        <li class="flight">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">机票</span>
          </a>
        </li>
        <li class="hotel">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">酒店</span>
          </a>
        </li>
        <li class="gongyu">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">公寓</span>
          </a>
        </li>
        <li class="tuan">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">团购</span>
          </a>
        </li>
        <li class="train">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">火车票</span>
          </a>
        </li>
        <li class="jingdian">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">景点</span>
          </a>
        </li>
        <li class="zuche">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">接送机</span>
          </a>
        </li>
        <li class="dujia">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">度假</span>
          </a>
        </li>
        <li class="gonglue">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">攻略</span>
          </a>
        </li>
        <li class="lvtu">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">旅途</span>
          </a>
        </li>
        <li class="cheche">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">车车</span>
          </a>
        </li>
        <li class="dangdiren">
          <a href="javascript:void(0)">
            <div class="icon"></div>
            <span class="title">当地人</span>
          </a>
        </li>
        <li class="tag" id="qnFooterToggle" @click="navShowClick" ref="tagClick"><span>更多</span></li>
      </ul>
      <ul class="footer-nav">
        <li><a href="javascript:void(0)">登录</a></li>
        <li><a href="javascript:void(0)">我的订单</a></li>
        <li><a href="javascript:void(0)">最近浏览</a></li>
        <li><a href="javascript:void(0)">关于我们</a></li>
        <div class="clear"></div>
      </ul>
      <ul class="mobile-pc">
        <li class="active"><a href="javascript:void(0)">触屏版</a></li>
        <li><a href="javascript:void(0)">电脑版</a></li>
      </ul>
      <div class="copyright"><span>Qunar 京ICP备05021087</span><a href="javascript:void(0)">意见反馈</a></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeFooter',
  methods: {
    navShowClick () {
      if (this.$refs.mainNav.style.height === '25px') {
        this.$refs.tagClick.style.top = '97px'
        this.$refs.mainNav.style.height = '110px'
        this.$refs.tagClick.classList.add('toggle')
        this.$refs.tagClick.children[0].innerText = '收起'
      } else {
        this.$refs.tagClick.style.top = '8px'
        this.$refs.mainNav.style.height = '25px'
        this.$refs.tagClick.classList.remove('toggle')
        this.$refs.tagClick.children[0].innerText = '更多'
      }
    }
  }
}
</script>

<style scoped>
  .qn-footer{background: #f3f3f3;}
  .main-nav{position: relative;width: 300px;height: 25px;margin: 0 auto;padding: 10px 10px 0 10px;overflow: hidden;}
  .main-nav li{margin: 0px;padding-left: 10px;height: 31px;width: 65px;float: left;position: relative;background: none;}
  .main-nav li a{display: block;height: 22px;width: 100%;font-size: 12px;}
  .main-nav li .icon{float: left;width: 22px;height: 22px;background: url(http://source.qunarzz.com/site/images/wap/touch/images/v2/images2x/nav_7.png) 0 0 no-repeat;background-size: 175px 50px;}
  .main-nav li .title{display: inline-block;color: #9e9e9e;margin: 3px 0 0 5px;border-bottom: 1px solid #acacac;font-size: 12px;}
  .qn-footer .main-nav .flight .icon {background-position: 0 0;}
  .qn-footer .main-nav .hotel .icon {background-position: -25px 0;}
  .qn-footer .main-nav .gongyu .icon {background-position: -150px 0px;}
  .qn-footer .main-nav .tuan .icon {background-position: -50px 0;}
  .qn-footer .main-nav .train .icon {background-position: -50px -25px;}
  .qn-footer .main-nav .jingdian .icon {background-position: -75px 0;}
  .qn-footer .main-nav .zuche .icon {background-position: -100px 0;}
  .qn-footer .main-nav .dujia .icon {background-position: 0 -25px}
  .qn-footer .main-nav .gonglue .icon {background-position: -75px -25px;}
  .qn-footer .main-nav .lvtu .icon {background-position: -100px -25px;}
  .qn-footer .main-nav .cheche .icon {background-position: -125px 0;}
  .qn-footer .main-nav .dangdiren .icon {background-position: -125px -25px;}
  .qn-footer .main-nav li.tag {position: absolute;top: 8px;right: 6px;background: #f3f3f3;font-size: 14px;color: #9e9e9e;width: 70px;}
  .qn-footer .main-nav li.tag:after {content: " ";position: absolute;top: 7px;left: 25px;width: 12px;height: 12px;background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAYCAYAAADkgu3FAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAIfSURBVEhLvVbnysJAEMz7P4u9otgbKIogKvaCvbcH2I8JXLi77BlR+H4oanI7szOzG63X60X/8bJkkPF4TN1u9yfgx+NBjUaDDoeDUscBGg6H5Pf7yefzUbPZ/ArscrlQNpu1a8TjcTqdTk4dG6jf79sX5Ve1WiWw+1TW/X5PiURCqZFMJgngqGHdbjcbXQfC91wuR7juBbZcLikcDrM10IQNhDegZjIZ9sZUKqVIoIMOBgMKBAKus/htNBqp0uEwZKrVaixYLBaj3W7n6qzdbrP3R6NRWq/XfBgE006n44RCljMUChEkEqTgISd3Op1mFVDiLcCm0ykFg0FWDmhukrlcLtP9fmc9ZYEAuN1ujSHhOoGM70JjBPIKiQBD5xh0r2QqQPP5XEmKV0hg+mazUUCezyehO3lYnXjjA3wRMUUgdIZ6SGD6+XxW7sPMFQoF21t5WB0g5F2sHyEJ9hXYyYCz2YyQvkql4jIdHWDmZP9ARgy8db1eCRJwBpdKJbag3i3kM9UQS9r26Hg8utgIYEQZZExmm0YBCvV6PfdmQIvFYpHtDHqDjA4GtrrkIIi9t1gszJsBnrRaLeNaEQnDffV63UgKm1wnxc4Rnk3cosTMTCYTJ1m6r/l83iizcWBXqxVFIhGWNRccLqVyV283w7uQCDB4JJ45X68gHMSSRMy5LjjTTWBvOxKHuJAgifofkJ86kg+LkMD0Tx7x8tk/qrabQu3SN6AAAAAASUVORK5CYII=) 0 0 no-repeat;background-size: 12px 12px;}
  .qn-footer .main-nav li.toggle:after {background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAYCAYAAADkgu3FAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAIfSURBVEhLlZZnCgJBDIW9/1nsFcXeQFEEUbEX7L0dIPIWZpmZzeyuPwSZHfMlLy9ZA9/vl/x+ns8nlUolCofDNJlMfP8O8QN+IefzmTKZDAWDQfvT7Xbp8/n4AvoCrddrisViCkQAq9UqvV4vT5gnaDQaUSgUYiECls1m6XK5uMKMIEjSbrddAbKM8XicttutEcaCHo+H1XQ5kPheLpdpPp9TJBJxPHcziQN0Op0cTReQVqtlN3+/31MikWCT4UyigExNR48Gg4FDFvRFd6JIqlKpEMZBuNoGDYdDtumQaLFYGLWHzPl8nq1MNokFQrZcPyANJNJn7Xq9KmewN2xuioFkLBBKzOVyykVkwwWs1+sUjUZpuVwqMM6lkHw6nVr3bOnu97utN5wl64uLt9tNSQZB+v2+o1qcoTI4UJZcMQMq6PV6jrXi5rBms0nv91sBoorVaqWceW6G2WzGzozcD5gBirjtTVcQquMazJ2lUik6HA7/bQa4qFarsRBkj/2HHuhAt1FwVIQ+6Q4UARuNht2PzWZjuU+HmUyigHa7nXGtQEa9B8fjkZLJJFu5bhIbBKdwcuBsPB4btYcCmDmub7JJLBA05y7iZQeJvN7CmLliscjGgEnw3ALJwyqA6XSasMm9IOI5Zgk91BNGEcpmgASg42KhUPCcC1MCnU7HigFTyH9gFDPgDwjeqvqk+61K3MOSxqDLv/PcDP9CTPd/7sWbQk+SlPgAAAAASUVORK5CYII=) 0 0 no-repeat;background-size: 12px 12px;}
  .qn-footer .main-nav li.tag span {display: inline-block;border-left: 1px solid #acacac;padding-left: 30px;margin-top: 5px;}
  .footer-nav{width: 100%;height: 39px;border-bottom: 1px solid #cacaca;}
  .footer-nav li {float: left;padding-left: 20px;}
  .footer-nav li a {position: relative;color: #25a4bb;font-size: 14px;line-height: 39px;}.mobile-pc {padding: 10px 0 0 0;text-align: center;}
  .mobile-pc li {display: inline-block;margin: 0 15px;}
  .qn-footer .mobile-pc a{font-size: 14px;color: #25a4bb;}
  .qn-footer .mobile-pc .active a{color: black;}
  .copyright {color: #9e9e9e;text-align: center;font-size: 14px;padding: 10px;}
  .copyright a {color: #9e9e9e;height: 33px;}
</style>
