# Wizard 

Wizard是基于Laravel开发框架开发的一款开源项目（API）文档管理工具。

在线预览体验地址：http://wizard.aicode.cc/

## 特性

- 支持markdown文档
- 支持Swagger文档
- 支持用户权限管理
- 支持团队协作，文档变更记录，文档对比
- 支持项目分组
- 支持标签
- 支持文档搜索
- 支持阅读模式
- 完全开源，内网部署


## 安装

安装依赖

    composer install --prefer-dist

安装配置数据库

    cp .env.example .env
    
    php artisan migrate:install
    php artisan migrate
    
文件上传支持需要执行以下命令

    php artisan storage:link
    
执行该命令后会在public目录下创建`storage/app/public`目录的符号链接。

## 更新

更新只需要到项目目录下执行
    
    git pull
    php artisan migrate

就可以完成更新。

### 使用Docker运行

    docker-compose up

## TODO

* [ ] __开发框架升级Laravel 5.8__
* [ ] 新版本更新
    * [ ] 自动检测是否有新版本
    * [ ] 无损更新版本
* [x] markdown编辑器增加json转换为markdown表格的功能
* [ ] 增加空间管理，类似于命名空间，不同部门在自己的空间中管理项目，文档等
* [x] 项目功能
    * [x] 项目新增
    * [x] 项目配置
    * [x] 项目权限分配
    * [x] 项目删除
    * [x] 支持对项目进行分组，首页分组展示
    * [x] 关注项目优先展示
* [x] 文档历史管理，文档恢复
* [x] 操作日志记录
* [ ] 国际化支持
* [x] markdown编辑器增加图片上传支持
* [x] 文档差异比较，文档历史版本差异比较
* [ ] 基于git的文档差异分析
* [x] 文档多人编辑避免内容冲突覆盖
* [ ] 个人文档置顶（个人关注的文档，在首页增加展示区域，方便快速进入）
* [ ] 全局文档置顶（重要的常用文档，由管理员设置在首页特定区域展示，方便快速进入）
* [ ] 全文检索（文档，项目，评论，标签） 
* [ ] **搜索功能优化，大部分用户都认为首页项目栏目顶部的搜索是用来搜索文档的，因此搜索不到**
* [ ] 图片拖拽，复制自动上传
* [ ] 文档管理
    * [x] 文档编辑
    * [x] 新增文档
    * [x] 支持Swagger格式文档
    * [x] 支持markdown文档
    * [x] 文档删除
    * [ ] **跨项目移动文档（移动时级联选择项目-目录）**
    * [ ] 文档点赞
* [x] 文档菜单支持折叠
* [x] 权限组，分组权限，管理员权限
    * [x] 项目按照分组分配读写权限
    * [x] 项目按照用户分配读写权限
* [ ] 文档模板管理
    * [x] 另存为模板
    * [x] 编辑器选择模板
    * [x] 模板列表
    * [x] 模板更新
    * [x] 模板删除
* [x] 文档排序，支持在文档配置中国年修改文档排序
* [ ] 文档排序优化：以拖动的方式进行排序
* [ ] 文档快速在项目内部变更目录
* [x] 项目排序
* [x] 文档标签
* [ ] 文档评论
    * [x] 实现最基本的评论功能
    * [x] 实现评论回复，带层级的评论
    * [x] 实现评论支持@某人
    * [ ] 评论点赞，类似Github issue评论后的emoji
    * [ ] 实现评论支持@用户组下所有用户
* [ ] 消息通知功能
    * [x] 支持@某人后收到消息
    * [x] 支持消息列表
    * [x] 新的消息提示
    * [x] 消息全部已读，部分已读
    * [ ] 新消息邮件提醒
    * [ ] 消息接收配置（站内信，邮件，接收类型）
* [x] 关注项目
    * [x] 关注项目，取消关注
    * [x] 已关注项目列表
    * [ ] 关注项目变更后接收消息通知
* [ ] 支持导出文件
    * [ ] 导出pdf
    * [ ] 导出markdown、swagger
    * [ ] 导出word
    * [ ] 文档批量导出
* [ ] 实现API接口管理，自动根据接口数据判断接口是否需要修改
* [ ] 对接postman，实现自动生成接口文档，接口测试
* [ ] 实现页面中之间互相引用
* [x] 项目列表分页展示，增加按照项目标题搜索
* [x] 文档增加标题搜索
* [x] 文档保存后弹框提示选择：继续编辑还是创建新文档
* [ ] 文档分享
    * [x] 分享链接
    * [x] 分享后的文档页面，单页面模式
    * [ ] 分享链接管理
    * [ ] 分享链接有效期设置
    * [ ] 分享链接删除
* [x] 文档附件
    * [x] 附件上传
    * [x] 附件展示
    * [x] 附件删除
    * [x] 附件重传（历史附件）
    * [ ] 文档，评论内引用附件 
* [x] 用户管理
    * [ ] **用户姓名自动转拼音，用于引用该用户时快速提示和搜素**
    * [ ] 用户部门管理，用于不同部门使用不同空间
    * [x] 用户登录，注册，找回密码
    * [x] 基本信息修改
    * [x] 修改密码
    * [x] 管理员分配
    * [x] 用户分组管理
        * [x] 管理员管理分组
        * [x] 分组基础数据结构支持
    * [ ] **用户管理页面，增加为用户分配用户组的功能，简化新员工入职时，权限分配的工作量**
    * [ ] **LDAP支持**
* [ ] 统计信息查看
    * [x] 用户数量统计
    * [x] 文档数量统计
    * [x] 评论数量统计
    * [ ] 用户活跃度统计
    * [ ] 文档更新统计

