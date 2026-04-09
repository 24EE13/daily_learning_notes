# MVC架构

*架构：代码的专属工位表* 

- 数据模型 Model（数据与修改数据的方法）
- 视图 View（）
- 控制器 Controller（）



View里只有监听的用户与界面的交互，还有界面本身的显示以及显示方法。不提供其他诸如显示逻辑、交互逻辑之类的。说白了View只提供交互事件和显示方法，不提供具体的实现。

常用事件：

```cs
//Button的onClick.AddListener可以添加事件（在按钮按下时执行）
btn_Start.onClick.AddListener(() => StartClicked?.Invoke());
//RemoveListener可以移除监听器



```





Controller里接收View发出的事件以及取Model里的数据，用这些写出交互逻辑和具体效果实现。
