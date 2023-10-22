## 说明

&emsp;&emsp;当前 npm 包，是对[hexo-filter-gitcalendar](https://www.npmjs.com/package/hexo-filter-gitcalendar)包的功能升级。

> 新增功能：git 提交日历 可以跟随主题模式进行变化。

## 安装

```sh
npm i hexo-butterfly-git-gitcalendar
```

## 使用

&emsp;&emsp;在博客根目录的`_config.yml`文件中添加如下配置信息：

```yml
# hexo-butterfly-git-gitcalendar
gitcalendar:
  enable: true # 开关
  priority: 5 #过滤器优先权
  enable_page: / # 应用页面
  # butterfly挂载容器
  layout: # 挂载容器类型
    type: id
    name: recent-posts
    index: 0
  user: Lencamo # 你的github用户名
  apiurl: 'https://gitcalendar.zfe.space' # 使用自己部署api，详见：https://github.com/Zfour/python_github_calendar_api
  minheight:
    pc: 280px #桌面端最小高度
    mibile: 0px #移动端最小高度
  color_light: # light 亮色主题配色，见后面
  color_dark: # dark 暗色主题配色，见后面
  container: .recent-post-item(style='width:100%;height:auto;padding:10px;') #父元素容器，需要使用pug语法
  gitcalendar_css: https://unpkg.zhimg.com/hexo-filter-gitcalendar/lib/gitcalendar.css
  gitcalendar_js: https://unpkg.zhimg.com/hexo-filter-gitcalendar/lib/gitcalendar.js
```

&emsp;&emsp;更多配置可以查看[hexo-filter-gitcalendar](https://www.npmjs.com/package/hexo-filter-gitcalendar)

## 配色推荐

&emsp;&emsp;以下配色抓取与 github：

- light 亮色主题

```sh
color_light: "['#f1f3f4','#ffdacf','#ffb9a5','#f79981','#ec775c','#de5b41','#c2442d','#a93524','#8d291b','#771d13','#5d1008']" # github 的 --color-scale-coral 系列
color_light: "['#f1f3f4','#ffd7eb','#ffb3d8','#fc8dc7','#e275ad','#c96198','#ae4c82','#983b6e','#7e325a','#69264a','#551639']" # github 的 --color-scale-pink 系列
color_light: "['#f1f3f4','#eedcff','#dcbdfb','#dcbdfb','#b083f0','#986ee2','#8256d0','#6b44bc','#5936a2','#472c82','#352160']" # github 的 --color-scale-purple 系列
color_light: "['#f1f3f4','#ffd8d3','#ffb8b0','#ff938a','#f47067','#e5534b','#c93c37','#ad2e2c','#922323','#78191b','#5d0f12']" # github 的 --color-scale-red 系列
color_light: "['#f1f3f4','#ffddb0','#ffbc6f','#f69d50','#e0823d','#cc6b2c','#ae5622','#94471b','#7f3913','#682d0f','#4d210c']" # github 的 --color-scale-orange 系列
color_light: "['#f1f3f4','#fbe090','#eac55f','#daaa3f','#c69026','#ae7c14','#966600','#805400','#6c4400','#593600','#452700']" # github 的 --color-scale-yellow 系列
color_light: "['#f1f3f4','#b4f1b4','#8ddb8c','#6bc46d','#57ab5a','#46954a','#347d39','#2b6a30','#245829','#1b4721','#113417']" # github 的 --color-scale-green 系列
color_light: "['#f1f3f4','#c6e6ff','#96d0ff','#6cb6ff','#539bf5','#4184e4','#316dca','#255ab2','#1b4b91','#143d79','#0f2d5c']" # github 的 --color-scale-blue 系列
color_light: "['#f1f3f4','#cdd9e5','#adbac7','#909dab','#768390','#636e7b','#545d68','#444c56','#373e47','#2d333b','#22272e']" # github 的 --color-scale-gray 系列
```

- dark 暗色主题

```sh
color_dark: "['#2d333b','#5d1008','#771d13','#8d291b','#a93524','#c2442d','#de5b41','#ec775c','#f79981','#ffb9a5','#ffdacf']" # github 的 --color-scale-coral 系列
color_dark: "['#2d333b','#551639','#69264a','#7e325a','#983b6e','#ae4c82','#c96198','#e275ad','#fc8dc7','#ffb3d8','#ffd7eb']" # github 的 --color-scale-pink 系列
color_dark: "['#2d333b','#352160','#472c82','#5936a2','#6b44bc','#8256d0','#986ee2','#b083f0','#dcbdfb','#dcbdfb','#eedcff']" # github 的 --color-scale-purple 系列
color_dark: "['#2d333b','#5d0f12','#78191b','#922323','#ad2e2c','#c93c37','#e5534b','#f47067','#ff938a','#ffb8b0','#ffd8d3']" # github 的 --color-scale-red 系列
color_dark: "['#2d333b','#4d210c','#682d0f','#7f3913','#94471b','#ae5622','#cc6b2c','#e0823d','#f69d50','#ffbc6f','#ffddb0']" # github 的 --color-scale-orange 系列
color_dark: "['#2d333b','#452700','#593600','#6c4400','#805400','#966600','#ae7c14','#c69026','#daaa3f','#eac55f','#fbe090']" # github 的 --color-scale-yellow 系列
color_dark: "['#2d333b','#113417','#1b4721','#245829','#2b6a30','#347d39','#46954a','#57ab5a','#6bc46d','#8ddb8c','#b4f1b4']" # github 的 --color-scale-green 系列
color_dark: "['#2d333b','#0f2d5c','#143d79','#1b4b91','#255ab2','#316dca','#4184e4','#539bf5','#6cb6ff','#96d0ff','#c6e6ff']" # github 的 --color-scale-blue 系列
color_dark: "['#2d333b','#22272e','#2d333b','#373e47','#444c56','#545d68','#636e7b','#768390','#909dab','#adbac7','#cdd9e5']" # github 的 --color-scale-gray 系列
```
