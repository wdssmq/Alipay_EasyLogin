# Alipay_EasyLogin

支付宝授权登录简易封装 For Z-BlogPHP；

## 安装

支付宝登录基础封装 - Z-Blog 应用中心：

[https://app.zblogcn.com/?id=29614](https://app.zblogcn.com/?id=29614 "支付宝登录基础封装 - Z-Blog 应用中心")

## 使用

· 发起登录：

在你的应用中直接调用`Alipay_EasyLogin_Login()`或者参考该函数组织自己的登录流程；

· 授权成功后的回调处理：

```php
// 在你的应用中挂载这个接口
Add_Filter_Plugin('Filter_Plugin_Alipay_EasyLogin_LoginSuccess', 'demoPlugin_LoginSuccess');

// 接口函数示例
function demoPlugin_LoginSuccess($alipay_user_id, $objAlipay)
{
  $usr_data = $objAlipay->GetData();
  $access_token = $objAlipay->access_token;
}
```
