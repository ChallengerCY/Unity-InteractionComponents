# Unity-InteractionComponents
**Interaction Components**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;UI系统中处理交互的组件，如鼠标或触摸事件以及使用键盘或控制器进行交互。交互组件本身并不可见，需要结合可视化组件进行使用。

![InteractionComponents](https://github.com/ChallengerCY/Unity-InteractionComponents/blob/master/Unity-InteractionComponents/Picture%26Gif/Interaction%20Components.gif)

**Common Functionality**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;大多数交互组件都有一些共同之处。它们是可选的，它们共享一些内置功能，包括可视化状态之间的转换(normal, highlighted, pressed, disabled),还有通过键盘或者控制器导向到其他可选组件。这些内置功能在Selectable中展示。 可选组件最少有一个UnityEvent处于Invoked阶段，UI System 可以通过UnityEvent来捕获和记录附加到UnityEvent中代码的异常(变化)。

**Button**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Button组件有一个Onclick UnityEvent,当Button被点击时触发调用。

**Toggle**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Toggle组件有一个Is On 属性来确定它现在是开启还是关闭状态。这个值会在用户点击Toggle时进行变化，一个可视化的复选框也会相应的打开或者关闭。它有一个OnValueChanged UnityEvent ，当Toggle isOn发生变化时调用。

**Toggle Group**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Toggle Group可以将Toggles设置成一个组，可以使组里的Toggle具有互斥的作用(选择一个会关掉其他的)。

**Slider**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Slider有一个decimal Value，用户可以在最小值和最大值中间拖动。它可以是水平的也可以是垂直的。它有一个 OnValueChanged UnityEvent去定义当Slider值发生改变时调用。

**Scrollbar**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Scrollbar有一个decimal Number值在0~1中间，当用户拖动Scrollbar时，这个值将会变化。他经常和ScrollRect和Mask组成 Scrollview。手柄的取值在0~1之间，它决定了手柄的大小和整个滚动条的比例，用于指示在滚动视图中的显示范围。Scroll Rect可以自动实现这个功能。Scrollbar同样可以垂直放置或者水平放置。拥有一个OnValueChanged UnityEvent，当Scrollbar的值发生变化时触发调用。

**Dropdown**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dropdown有一个下拉列表可供选择。可以为每个选项设置一个文本字符串和一个Image。可以在Inspector 菜单中设置，也可以通过代码动态设置。它有一个OnValueChanged UnityEvent，当Dropdown选择不同值时候调用。

**Input Field**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Input Field可以让用户去编辑文字元素。他有两个UnityEvent 一个是当文字内容发生变化时会触发，一个是文字编辑结束时会触发。

**ScrollRect(ScrollView)**
>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当占用大量空间的内容需要显示在一个小区域时，可以使用ScrollRect。ScrollRect提供了滚动该内容的功能。通常ScrollRect会结合Mask创建一个滚动视图，这样只有在ScrollRect中的部分才会显示。ScrollRect可以另外结合一到两个Scrollbars来控制水平或垂直方向的拖动。
