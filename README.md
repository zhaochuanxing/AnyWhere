# AnyWhere
这是我仿造美团外卖做的一款APP，用户需要注册账号，然后浏览用户附近外卖餐厅，进行自助点餐，最后生成外卖订单。APP提供从点餐到送餐的一条龙服务，极大地方便了人民生活。
	
	主页部分实现了广告栏自动循环播放的效果，利用RelativeLayout+ScrollView实现了内容区域单独滑动的效果，商户展示栏可以额外展示优惠信息、美团专送和新商家等等，程序会在运行时通过百度地图SDK来获取用户地理位置，与周边商家经纬度进行比对计算出距离显示在商家信息上。

	通过继承Application来自定义一个Application并在清单文件中注册，通过这个自定义的Application来实现全局缓存及信息的传递、各种开源框架及SDK的初始化等操作。

	用户模块可以通过手机号注册，填写正确的手机号后服务器会发送一条验证码短信到用户的手机上，通过BroadCastReceiver监听短信广播，获取到短信内容，判断是否为本服务器发送的短信，并截取短信中的验证码信息自动填写到对应的注册表格中。

	用户也可以通过QQ、微信等方式进行第三方的登录。

	个人界面未登录状态下头像框显示默认灰色袋鼠头像，登陆后显示为个人头像，以及昵称，右上角的齿轮按钮通过ClickAble验证登录后可跳转至用户设置Activity，所有与用户相关的操作都需要登录后才可执行。

	订单页面通过RelativeLayout Visiable实现未登录状态下显示登录界面点击跳转登录，登录后如果没有近期订单则显示近期没有订单，如有则显示为订单列表。

	钱包页面可以显示个人钱包余额，通过支付宝、微信提供的API可以跳转至用户手机中的支付宝APP、微信APP实现充值操作。

	美团外卖红包里显示用户持有的红包，可以在下单时使用，使用后不可再次使用，并显示为“已使用”，代金券同上。

	商家入驻可以上传商家信息提交到系统审核。在个人页面下方还有一个更多选项，里面隐藏了一个内嵌的商户端APP，可以添加上传菜式等。

	收货地址支持新增、修改及删除。收货地址信息需要验证手机号，接入了百度地图SDK后通过地图搜索选择收货地址。

	订单模块支持多选及购物车查看，可以通过余额、支付宝、微信进行订单的支付。确认收货后可以对订单进行评价，这些评价将会显示在商户评价信息栏里，系统会自动评定优质评价并在评价内容上刻上“优质评价”的盖章。

	点击客服将自动打开手机QQ并自动跳转至客服QQ聊天界面。还有更多内容就不再赘述了。
