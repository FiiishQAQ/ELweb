## **网站导航栏部分**
> `ul.nav:`导航列表样式，左外边距80，宽度100%-80，子对象左对齐，高60
> 
> `li a.item:`导航单元，由于都要加超链接，就只针对`a`写了样式，左漂浮，100*60（靠line-height决定高）。字体16px，居中，悬浮变绿
> 
> `#active:`指示当前页面，字体绿色
> 
> `span.logo:`内边距5px，外边距10px，fixed
> 
> `div.nav:`容纳导航的块，超出部分不显示
---
## **带有背景的一块显示文字的地方**
目前有标题、正文、日期时间三种文字样式，目前设置点击块页面滑到这一节，悬停有背景放大效果
> `textField_head:`内边距200 155 100 155
> 
> >`~ p.heading:`白色，5px模糊阴影，50px，其余默认
> >
> >`~ p:`正文，白色，5px模糊阴影，其余默认
> >
> >`~ p.date:`白色，5px阴影，其余默认
> >
> ><span style="text-shadow: 0 0 5px rgba(0, 0, 0, 0.76);color: white;">5px模糊示例</sapn>
> >默认样式见最后
---
## **页面标题部分**
保留了文字块的点击效果，删除背景放大
> `page_title:`基本同上
> 
> >`~ p.heading:`同上
> >
> >`~ p:`同上
> >
> >`~ p.date:`同上
---
## **空白背景的文字块**
有标题、正文、日期时间三种文字样式
> `textField_body:`内边距100 155 100 155
> 
> > `heading:`默认
> >
> > `p:`默认
> >
> > `date:`默认
---
## **多个短篇（一小段文字构成的介绍性段落）构成的页面布局**
目前设计为：最上方为页面标题，有背景，正文部分左侧为内容，右侧为页面导航
### **内容部分** 
> `div.content_box:`内边距30 50 100 155，宽50%，左float
> 
> `div.content:`下方有<span style="border-bottom: 1px solid rgb(209, 209, 209);">1px，颜色rgb(209, 209, 209)的下边界</span>，上下内边距30
>
> > `~ p.heading:`默认
> >
> > `~ p:`默认
> >
> > `date:`默认
>
> `#last:`去除下方边界线
### **页面导航**
> `div.page_nav:`宽200，内边距0 155 0 70%，position为sticky，距离顶部0px时
> 
> `div.pn_instructer:`窄页面时指示导航，通过js展开收起，内边距5 155 5 155，<span style="background:rgb(235, 238, 235);color:rgb(121, 150, 140);">背景颜色rgb(235, 238, 235)，字体颜色rgb(121, 150, 140)</span>
> 
> `#pn_text:`24px,颜色rgb(121, 150, 140)
> 
> `#pn_icon:`指示开合的+
> 
> > `ul.page_nav:`看就完了
> >
> > `li a.pn_item:`看就完了
---
## **基本元素**
> `body:`字体顺序：PingFangSC, Verdana, Arial, '微软雅黑','宋体'，超出隐藏
> 
> `a:`无outline， 但没有设置颜色，搭配以下< p >使用
> 
> > `~ span.emphasis:`可能是标准超链接格式？有下划线，悬浮变为强调色，需要设置最开始的颜色
> 
> `p:`各种段落样式，`注意`，p的默认样式设置为`p.body`的样式，以后应该不应使用body，body已删除
> 
> > `p.heading:`<span style="font-size: 30px;font-weight: bold;opacity: 0.9;color:rgba(57,159,99,1.00);">字号30，加粗，透明度0.9，颜色rgba(57,159,99,1.00)
> >
> > `-p.body（已经弃用并删除，请直接使用无类的p来表示正文）:`<span style="color:rgb(141, 148, 141);font-size: 18px;opacity: 0.9;">颜色rgb(141, 148, 141)，字体大小18px，透明度0.9</span>，`请使用无类的p`
> >
> > `p.date:`<span style="font-size: 14px;opacity: 0.9;font-family: 'Merriweather', serif;color:rgb(194, 196, 190);">字号14px，透明度0.9，字体`font-family: 'Merriweather', serif;`，颜色rgb(194, 196, 190)</span>使用了谷歌字体，所以显示不出来,要使用请在head部分添加
> >```
> ><link rel="preconnect" href="https://fonts.gstatic.com"> 
> >
> ><link href="https://fonts.googleapis.com/css2?family=Merriweather&display=swap" rel="stylesheet">
> >```
---
## **页脚**
> `div.foot:`12号字，自己看吧
---
## **@media，屏幕宽度小于1000px的时候**
> `div.content_box:`
> 
> `div.page_nav:`
> 
> `div.pn_instructer:`
> 
> `ul.page_nav:`
> 
> `#pn_text:`