# 网上商城

#### 需求分析:
##### 使用MySQL和flask实现,所有功能需和数据库互联,需要网页交互
#### 创建数据库shop,通过flask连接数据库,使用flask建表
##### 1.用户注册,登录,退出,修改个人信息
登录框,注册框,个人信息修改页面.登录成功跳转到首页,注册成功跳转到登录页面,
用户信息包含昵称,密码,手机号(手机号不可重复,可以用手机号登录,自动生成账号,
可以通过账号登录,账号不可改变),(地址,订单信息先不写),可以在修改信息页面修
改昵称,密码,手机号,地址,可以添加若干地址,并设置一个默认地址,在提交订单是显
示默认地址.

##### 2.首页商品图片轮播展示,显示热销和推荐购买,搜索商品
显示商品热销(根据商品销量),显示商品推荐(根据用户搜索或者浏览),每个商品图片
需要有一个链接,用于跳转到商品详情页,右上角有登录|注册,登录成功有用户头像,
用户点击可以查看用户信息,并可以退出登录.正上方有搜索框,可以搜索商品,可以根
据商品名称关键字搜索商品,跳转到一个类似首页但没有轮播展示,可以下拉的包含所有
符合条件商品的页面,没有相关商品则返回'未找到相关商品'.

##### 3.查看商品详细信息,加入购物车,清空购物车,加减商品数量
商品详情页(一个框架,包含商品图片,商品价格,加入购物车按钮)
购物车页面:显示用户所有购物车商品,可以加减或者移除,选中部分或者所有商品提交订
单,提交成功跳转到支付页面（吴谦）

##### 4.提交订单,设置默认收货地址,显示支付宝二维码,查看订单详情
支付页面:若没有设置收货地址,则必须填写地址,有则显示默认地址,可以修改地址,点击
提交弹出支付宝二维码(意思意思),再点击二维码下方提交跳转到成功界面,点击取消则返
回支付页面,再点击取消返回购物车页面
订单详情页面:查看订单详情

##### 5.用户管理,可以查看,删除,更改所有用户信息,可以查看所有订单信息
登录管理员账号跳转到此页,可以搜索查看某个用户的信息,可以修改用户的状态(正常,冻
结,注销),可以选择删除已注销用户.可以添加用户.可以查看所有订单信息.

##### 6.商品管理,可以查看,删除,更改所有商品信息,可以查看商品销量排行
登录店家账号跳转到此页(目前先假设只有一家店).
商品至少包含图片,价格属性.

#### 初步产品需求,欢迎各位修改,每个人选一个,先到先得,你们商量一下,我选剩下的
####数据库表包含用户表
### 数据备份
#### 1. 备份命令格式
mysqldump -u root -p shop > ./shop.sql(保存在当前文件夹)

#### 2. 恢复命令格式
mysql -u root -p shop < shop.sql(恢复当前文件夹的shop数据库)
