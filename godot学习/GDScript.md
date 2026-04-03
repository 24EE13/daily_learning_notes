

获取节点
`$节点名`
`get_node(节点名)`



激活（SetActive(true)）
与禁用（SetActive(false)）

get_tree().paused = true//游戏暂停
get_tree().paused = false//游戏继续



node.hide()：让节点“隐身”，玩家看不见它。
node.show()：让节点“现身”，玩家又能看见它了。

但是，这两个函数不能销毁节点，同时**不会自动停止节点的代码运行！！！**

与之相似的：
queue_free()	彻底删除节点（如：子弹击中目标后销毁）。
set_process(false) 仅停止逻辑计算，不改变外观。
set_process(true) 继续逻辑运算
