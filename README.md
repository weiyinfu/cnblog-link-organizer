# 链接整理工具

把链接进行归类梳理是构建知识体系的重要组成部分。

# 目录说明

- public：存放不需要编译的用户可随意访问的资源
- server：后端
- vues：前端代码
- test：测试

# 树结构规范

- 每个树只有一个根节点，像 XML 一样
- 如果结点是叶子结点，那么结点有 label、url 两个属性；如果结点是非叶子节点，那么结点有 label、children 两个属性，其中 children 是数组。

# 说明

如果开发模式，把依赖打包到一个文件里面，不适用 externals 来减小体积，这样能够加速开发时网络速度，访问 dev.html。如果是生产模式，把依赖通过 externals 引入，这样能够加快加载速度。  
开发时，使用 run-dev 命令运行程序，这样在服务端代码更新时自动重启服务器，忽略前端代码，因为前端代码的变动可以由 webpack 自动刷新，速度远远快于重启重新打包。

# TODO

- 添加 JSON 校验，用户保存的内容不能太长
- indicator 不显示
- 添加 loading
- 多选，方向键多选
- 方向键选中
- 添加结点上下文菜单
- 多选+拖动，模仿 chrome
- 添加操作历史，添加撤销功能
- 点击文件夹也可以前进后退
- 拖动时的样式，悬浮时的样式
- allowDrop 时一切都是实时的
- 把两个树的数据都设置成 computed 会不会导致计算量太大，每次更新都计算一遍。如果把左面目录中的文件设置为不可见，又会显示展开菜单，这很丑陋
- 插入在前面、后面、里面三种，而不是只能放在里面
- 上下文菜单：重命名、删除、添加文件夹
- 左面视图控制，设置为 flat 形式展示，全部展开，全部折叠
- 添加历史，可以前进后退
- 排序，拖动放到前后。现在只能拖动到内部
- 添加导入普通文件夹功能
- 写接口添加频控
