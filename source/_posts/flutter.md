# flutter

## 基础 Widget
* Text：该 widget 可让创建一个带格式的文本。
* Row、 Column： 这些具有弹性空间的布局类Widget可让您在水平（Row）和垂直（Column）方向上创建灵活的布局。其设计是基于web开发中的Flexbox布局模型。
* Stack： 取代线性布局 (译者语：和Android中的LinearLayout相似)，Stack允许子 widget 堆叠， 你可以使用 Positioned 来定位他们相对于Stack的上下左右四条边的位置。Stacks是基于Web开发中的绝度定位（absolute positioning )布局模型设计的。
* Container： Container 可让您创建矩形视觉元素。container 可以装饰为一个BoxDecoration, 如 background、一个边框、或者一个阴影。 Container 也可以具有边距（margins）、填充(padding)和应用于其大小的约束(constraints)。另外， Container可以使用矩阵在三维空间中对其进行变换。
* Theme.of(context)将查找Widget树并返回树中最近的Theme。
* Icon、 IconButton, 和Text 都是无状态widget, 他们都是 StatelessWidget的子类。
* stateful widget 是动态的. 用户可以和其交互 (例如输入一个表单、 或者移动一个slider滑块),或者可以随时间改变 (也许是数据改变导致的UI更新). Checkbox, Radio, Slider, InkWell, Form, and TextField 都是 stateful widgets, 他们都是 StatefulWidget的子类。

## 布局
### 对齐 widgets
* 您可以控制行或列如何使用`mainAxisAlignment`和`crossAxisAlignment`属性来对齐其子项。 对于行(Row)来说，主轴是水平方向，横轴垂直方向。对于列（Column）来说，主轴垂直方向，横轴水平方向。


## 状态
* 有些widgets是有状态的, 有些是无状态的
* 如果用户与widget交互，widget会发生变化，那么它就是有状态的.
* widget的状态（state）是一些可以更改的值, 如一个slider滑动条的当前值或checkbox是否被选中.
* widget的状态保存在一个State对象中, 它和widget的布局显示分离。
* 当widget状态改变时, State 对象调用setState(), 告诉框架去重绘widget.
* 状态的值，放到私有变量中，通过`setState`方法，来改变变量值，从而触发UI更新