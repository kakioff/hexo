# xian`s 博客网站

[xian的博客网站](https://www.byxian.top)



# 包含的插件和用法

> 来自 [「推荐」本站用到的 hexo 插件 | 若风 (loafing.cn)](https://loafing.cn/posts/hexo-tags.html#其它)

## [文字上方注释 Ruby](https://github.com/lostandfound/markdown-it-ruby)



> 实测中`hexo-tag-pinyin`不可用，会报错

![readme](https://cdn.jsdelivr.net/gh/kakioff/pictureBeds@main/20211001/readme.1jauy9y42kv4.png)

## [悬浮注释 hint](https://github.com/etigerstudio/hexo-tag-hint)

![readme](https://cdn.jsdelivr.net/gh/kakioff/pictureBeds@main/20211001/readme.4rtmfs4luvm0.png)

## [豆瓣电影/读书/音乐卡片](https://github.com/TankNee/hexo-douban-card)

```shell
{% douban movie 24745500 %}
{% douban book 30376420 %}
{% douban music 35099703 %}
```

![readme](https://cdn.jsdelivr.net/gh/kakioff/pictureBeds@main/20211001/readme.7il25s3fz8c0.png)



## [pdf](https://github.com/superalsrk/hexo-pdf)

```
{% pdf 文件地址 %}
{% pdf http://7xov2f.com1.z0.glb.clouddn.com/bash_freshman.pdf %}
```



## [文字遮盖效果 Spoiler](https://github.com/unnamed42/hexo-spoiler)



```yaml
# _config.yml
spoiler:
  style: blur # 或者box
  color: black # 仅当 style 为 box 时起效
  p: false # 没懂啥意思，不管它
```

![readme](https://cdn.jsdelivr.net/gh/kakioff/pictureBeds@main/20211001/readme.793ahq865bg0.png)



## [数据可视化工具 Chartjs](https://github.com/Shen-Yu/hexo-tag-chart)

[Chart.js 介绍](https://chartjs.bootcss.com/)

[插件预览效果](https://shen-yu.gitee.io/2020/chartjs/)

```markdown
{% chart 90% 300 %}
\\TODO option goes here
{% endchart %}
```

其中 `chart` 是标签名，`endchart` 是结束标签，不需要更改，`90%` 是图表容器的相对宽度，默认是`100%`，`300` 是图表容器的高度，默认是按正常比例缩放的，你可以通过设置 `options` 里面的 `aspectRatio` 属性来调整宽高比例，另外还有许多属性可以自定义，你可以查看 [官方文档](https://www.chartjs.org/) ([中文文档](https://chartjs.bootcss.com/))。在标签之间的部分，都是需要自己填充的图表数据和属性。

例子：

```json
{% chart 90% 300 %}
    {
    type: 'line',
    data: {
    labels: ['January', 'February', 'March', 'April', 'May', 'June', 'July'],
    datasets: [{
        label: 'My First dataset',
        backgroundColor: 'rgb(255, 99, 132)',
        borderColor: 'rgb(255, 99, 132)',
        data: [0, 10, 5, 2, 20, 30, 45]
        }]
    },
    options: {
        responsive: true,
        title: {
        display: true,
        text: 'Chart.js Line Chart'
        }
    }
}
{% endchart %}
```



## [Instagram分享](https://github.com/tea3/hexo-tag-instagram)

```markdown
{% instagram false https://www.instagram.com/p/B2vyQrxHuIN/ 100% %}
```



## [hexo-simple-mindmap](https://github.com/HunterXuan/hexo-simple-mindmap) [思维导图](https://hunterx.xyz/use-mindmap-in-hexo.html)

```markdown
{% pullquote mindmap mindmap-md %}
- [在 Hexo 中使用思维导图](https://hunterx.xyz/use-mindmap-in-hexo.html)
  - 前言
  - 操作指南
    - 准备需要的文件
    - 为主题添加 CSS/JS 文件
  - 使用方法
{% endpullquote %}
```



## [hexo-tag-wikipedia 嵌入维基百科摘要](https://github.com/tuanna-hsp/hexo-tag-wikipedia)

```
{% wikipedia title:GitHub wikiButton:true %}
```

| Parameter            | Description                                                  |
| -------------------- | ------------------------------------------------------------ |
| `title:<wiki_title>` | For example with the wiki URL https://en.wikipedia.org/wiki/Star_Wars, it is 'Star_Wars' |
| `wikiButton:<true>`  | Whether or not to show the Wikipedia page link. Default to `false` |
| `lang:<code>`        | The wiki page language code. `en`, `fr`, `ja`... Default to `en` |
| `sentences:<number>` | Limit the number of sentences to show if specified. Only accept value from 1 to 10. Omit to show the full extract |

