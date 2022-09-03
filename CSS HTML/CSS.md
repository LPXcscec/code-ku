CSS:层叠样式表
   基本语法：CSS写在style标签里，style标签一般写在head标签里，title标签下面
    <style>
     p(p是选择器，查找标签){
        color:red;
     } 
    <style>
CSS引入方式：内嵌式：写在style标签里，作用于当前页面，使用于小案例里
            外联式：CSS写在单独的CSS文件内，通过link标签引入，多用于项目中
            行内式：CSS写在标签的style属性中，作用于当前标签，配合js使用

基础选择器：
        1.标签选择器：  标签名{CSS属性名：属性值;}
        2.类选择器：    .类名{CSS属性名：属性值;} 
                    注意：1.所有标签都有class属性， class属性的属性值即为类名
                         2.类名可以由数字、字母、下划线、中划线组成，但不能以数字或者中划线开头
                         3.一个标签可以有多个类名，类名之间以空格隔开
                         4.类名可以重复，一个类选择器可以同时选择多个标签
        3.id选择器： #id{}
                    注意：所有标签都有id属性且是唯一的，一个id选择器只能选中一个标签。
        4.通配选择器：  *{CSS属性名：属性值}  （很少使用）

字体样式：
        1.字体大小： 属性名：font-size  取值：数字 + px
        2.字体粗细： 属性名：font-weight  取值： 关键字：正常 normal    加粗  bold    纯数字（取100-900的整数）：正常  100    加粗  700
        3.字体倾斜： 属性名：font-style  取值： 正常（默认值） normal   倾斜：italic
        4.字体系列： 属性名 font-family  取值： 具体字体1，具体字体2，具体字体3。。。。 （假如字体中存在多个单词的，推荐使用引号包裹。但最后一项字体不需要引号包裹）
          常见字体系列：  无衬线字体 sans-serif（网页中最常用）   衬线字体 serif   等宽字体 monospace
        5.字体font相关属性的连写：  font：style weight size family  （要省略只能省略前两个，前两个以默认值设置）

文本样式：
        1.文本缩进： 属性名：text-indent   
                    取值： 数字+px   数字+em(推荐使用，1em等于当前标签的font-size大小)
        2.文本水平对齐方式： 属性名：text-align  
                    取值：left center right （如果需要让文本水平居中，text-align属性给文本所在标签（文本的父元素）设置）
        3.水平居中方法总结： text-align:center    
                    可以用于：1.文本  2.span标签、a标签  3.input标签、img标签 （text-align属性给文本所在标签（文本的父元素）设置）
        4.文本修饰： 属性名： text-decoration   
                    取值： underline 下划线    line-through 删除线    overline 上划线    none 无装饰线
                    注意：开发中会使用text-decoration：none；清除a标签默认的下划线
        5.行高： 属性名 line-height
                 取值： 数字+px    倍数（当前标签font-size的倍数）
                 注意：行高与font连写的注意点：font：style weight size/line-height family；
        6.颜色常见取值（了解）：属性名： 文字颜色 color    背景颜色 background-color 
                              最常用是rgba表示法及十六进制表示法
        7.标签水平居中方法总结（拓展）： margin：0 auto  (让盒子居中)
