#红黑树

####红黑树的特点
1. 树的每个节点不是黑色就是红色
2. 根节点一定是黑色
3. 红色节点的父节点一定是黑色
4. 每个节点到它的每一个叶子节点所经过的黑色节点数量相同
5. 叶子节点都是黑色（都为空）

####新增节点

1. 新增节点为根节点，直接设置为黑色
2. 新增节点的父节点为黑色，新增节点保持为红色
3. 新增节点的父节点为红色
    + 叔父节点为红色
        + 将父节点和叔父节点设置为黑色，将祖父节点设置为红色，再将祖父节点当左新增节点，
        再次进行修复操作
    + 叔父节点为黑色
        1. 如果新增节点和父节点、祖父节点为一条线（新增节点和父节点都为它们父节点的左节点或都为右节点），
        将父节点设置为黑色，将祖父节点设置为红色，旋转祖父节点（都为左节点时右旋，都为右节点时左旋）
        2. 如果新增节点和父节点、祖父节点不在一条线。新增节点是父节点的左节点，父节点是祖父节点的右节点
        时，先右旋父节点，再按照一条线的情况操作；新增节点是父节点的右节点，父节点是祖父节点的左节点时，
        先左旋父节点，再按照一条线的情况操作

####删除节点

待续......
