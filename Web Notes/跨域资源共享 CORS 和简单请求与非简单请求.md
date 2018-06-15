---
title: 跨域资源共享 CORS 和简单请求与非简单请求
tags: CORS,请求
grammar_cjkRuby: true
---


### CORS是一个W3C标准
CORS全称是"跨域资源共享"（Cross-origin resource sharing），允许浏览器向跨源服务器，发出XMLHttpRequest请求，从而克服了AJAX只能同源使用的限制。
### CORS需要浏览器和服务器同时支持
CORS是浏览器自动完成，浏览器识别请求是属于跨来源，会添加附加的头部信息或发送option请求。
CORS是由服务器来实现，实现了CORS，即可进行跨原请求。
### CORS请求方式
CORS请求方式为简单请求和非简单请求
 - 简单请求
 满足两个条件：
 	1. 请求方法：
 		- HEAD
 		- GET
 		- POST
 	2. HTTP头部不超出以下字段：
		- Accept
		- Accept-Language
		- Content-Language
		- Last-Event-ID
		- Content-Type(限于application/x-www-form-urlencoded、multipart/form-data、text/plain)
- 非简单请求（不满足以上要求）

### 简单请求
对于简单请求，浏览器会在请求头部加上【Origin】字段说明来自哪个源（协议+域名+端口），服务器根据这个值决定是否允许请求（如果来源不满足访问条件服务器会返回提示CORS错误）。
如果头部信息不包含【Access-Control-Allow-Origin】，服务器会返回错误提示，错误会提示缺乏来源。
### 非简单请求
非简单请求时，浏览器会发送一个【预检（option请求）】，确定是否可以请求。头信息里面，关键字段是【Origin】，表示请求来自哪个源。
自定义头部，浏览器会检测到，并发送预检。

``` 自定义头部
xhr.setRequestHeader('Authorization', 'token');
```
![Request Headers 请求头][1]

![Response Headers 响应头][2]
【Response Headers】由服务器返回
除了【Origin】还会检测【Access-Control-Request-Method】和【Access-Control-Request-Headers】


  [1]: ./images/1529039060829.jpg
  [2]: ./images/1529043163794.jpg