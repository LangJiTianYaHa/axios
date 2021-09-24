	
13.克隆远程的dev分支：
	git checkout -b dev origin/dev
	
13.克隆远程的dev分支：
	git checkout -b dev origin/dev
	
13.克隆远程的dev分支：
	git checkout -b dev origin/dev
	
	
	2d变换 综合变换变换属性的顺序是会影响最终渲染结果的
                如果scale 写在了translate 的前边   translate的平移值也会跟着scale的比例缩放
                如果rotate 写在了translate的前边  translate会按照旋转后新的坐标系 发生平移
	
	例：transform: scale(0.5) translate(200px,0);
            	      transform:  rotate(45deg) translate(200px,0);

3.让元素水平垂直居中的方法
①弹性布局
	-父元素display:flex; justify-content:center;align-items:center;

②通过translate
	-position:absolute; left:50%;top:50%;transform:translate(-50%,-50%);

③块级元素居中
	-margin:0 auto
④通过margin
	-position:absolute; top:0;right:0;bottom:0;left:0;margin:auto	
⑤绝对定位＋负margin
	-position:absolute;left:50%;top:50%;margin-left:-px;margin-top:-px(宽高的一半)

4.transitionend 可以用来判断过渡是否完成
需要用addEventListener 绑定
例： 
fn.addEventListener('transitionend',function () { })

5.onresize 事件会在窗口或框架被调整大小时发生。

6.
offsetX，offsetY
	- 相对于事件源元素（srcElement）的X,Y坐标
clientX,clientY 
	-获取当前鼠标点击的坐标（不包含滚动条）
pageX，pageY
	-获取当前鼠标点击的坐标（包含滚动条）
clientHeight
	- 元素的可见高度，指元素的内容区和内边距的高度（不包含滚动条）
offsetHeight
	- 整个元素的高度，包括内容区、内边距、边框
offsetLeft
	- 当前元素和定位父元素之间的偏移量
getBoundingClientRect()用于获得页面中某个元素的左，上，右和下分别相对浏览器视窗的位置。
	-对象有6个属性：top, left, bottom, right, width, height；
window.innerWidth
	-浏览器窗口的宽度  包含滚动条
window.outerWidth
	-获取浏览器总宽  包含外侧的阴影
screen.width
	-屏幕的总宽

5.data-* :自定义属性

6.cloneNode  克隆节点

7.classList 是元素对象的一个属性, 用来操作元素的 class 类
* add 增加类名
* remove 移除类名
* contains 是否包含指定的类名

8.- this
- this是函数的上下文对象，根据函数的调用方式不同会执向不同的对象
	1.以函数的形式调用时，this是window
	2.以方法的形式调用时，this是调用方法的对象
	3.以构造函数的形式调用时，this是新建的那个对象
	4.使用call和apply调用时，this是指定的那个对象
	5.在全局作用域中this代表window

9.instanceof的作用：
-instanceof 关键字在js中是用于判断一个变量是否属于某个对象的实例
例：function Fun(){
      }
     console.log(Fn.prototype instanceof Object) // true
- * 表达式: A instanceof B             A 实例对象（隐式）   B 构造函数（显式）
  * 如果B函数的显式原型对象在A对象的原型链上, 返回true, 否则返回false
	
例：  function Foo() {  }
  var f1 = new Foo()
  console.log(f1 instanceof Foo) // true
  console.log(f1 instanceof Object) // true

10.filter() 方法创建一个新的数组，新数组中的元素是通过检查指定数组中符合条件的所有元素
11.JS中如何判断一个对象是否为空 ---JSON.stringify(obj) != {}

12.JSON-->JS: JSON.parse()
     JS-->JSON:JSON.stringfy

