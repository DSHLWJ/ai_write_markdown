---
title: Postman基本使用
description: Postman基本使用
date: 2022-06-09T20:12:52+08:00
lastmod: 2022-06-09T20:12:52+08:00
tags:
  - Postman
  - 测试
categories:
  - Test
---

# Postman基本使用方法

## 请求创建

![](assets/c0b4e55f142c5d829d16abc86805b0c1e30c3d9e.png)

## GET请求

![](assets/2025-07-28-18-13-25-image.png)

## POST请求

![](assets/2025-07-28-19-05-08-image.png)

## 设置（请求头）Headers

请求头是客户端发送给服务器的附加信息，主要包括以下几种：

- `Accept`：用于指示客户端可以接受的MIME类型，例如`text/html, application/json`表示接受HTML和JSON格式的数据。
- `Accept-Charset`：用于指示客户端可以接受的字符集，例如`utf-8`表示接受UTF-8编码的数据。
- `Accept-Encoding`：用于指示客户端可以接受的内容编码，例如`gzip, deflate`表示接受Gzip和Deflate编码的数据。
- `Accept-Language`：用于指示客户端可以接受的语言，例如`en-US`表示接受美国英语。
- `Authorization`：用于包含客户端提供的身份验证信息，例如`Basic dXNlcm5hbWU6cGFzc3dvcmQ=`表示使用基本身份验证，用户名为`username`，密码为`password`。
- `Cookie`：用于发送客户端的cookie信息。
- `Expect`：用于指示客户端期望服务器满足的要求，例如`100-continue`表示客户端期望服务器在接收完请求头后返回100 Continue状态码。
- `From`：用于指示发送请求的用户的电子邮件地址。
- `Host`：用于指示请求的目标服务器，例如`www.example.com`表示请求的目标服务器为www.example.com。
- `If-Match`：用于指示客户端提供的实体标记，如果实体标记匹配，则请求成功。
- `If-Modified-Since`：用于指示客户端提供的日期和时间，如果资源自该时间以来未被修改，则返回304 Not Modified状态码。
- `If-None-Match`：用于指示客户端提供的实体标记，如果实体标记不匹配，则请求成功。
- `Referer`：用于指示当前请求页面的来源页面地址。
- `User-Agent`：用于指示客户端的信息，例如浏览器类型、操作系统等

虽然请求头包含的信息很多，但是对于开发主要更关注的是请求头cookie，auth鉴权，可以通过这个信息，验证请求是否鉴权

![](assets/2025-07-28-21-14-39-image.png)



## 创建请求集

需要登录后才可以创建

![](assets/2025-07-28-19-06-28-image.png)

## Postman中的几种Auth Type

### 1.**No Auth**（不使用认证）

- **描述**：不使用任何认证。这适用于不需要身份验证的请求。

- **用途**：如果你的接口不需要认证，选择此选项即可。

### 2. **Bearer Token**

- **描述**：用于传递 **Bearer token**，通常是 OAuth2 或 JWT 认证中使用的方式。

- **用途**：常用于使用 token 进行身份验证的 API。

- **使用方法**：
  
  - 在 **Token** 输入框中填入你的 `token`（如 `JWT` 或 `OAuth2` token）。

### 3. **Basic Auth**

- **描述**：通过 HTTP Basic Authentication 进行身份验证。请求头会添加一个 `Authorization` 字段，内容为 `Basic <base64(username:password)>`。

- **用途**：常用于用户名和密码组合的身份验证。

- **使用方法**：
  
  - 输入 **用户名** 和 **密码**，Postman 会自动将其编码为 `Base64` 格式。

### 4. **Digest Auth**

- **描述**：使用 **Digest Authentication**，它是比 Basic Auth 更安全的认证方式，通过加密传输密码和其他请求头信息。

- **用途**：适用于需要 Digest Auth 的 API。

- **使用方法**：
  
  - 输入 **用户名**、**密码** 和其他 Digest 认证所需的字段（如 `Realm` 和 `Nonce`）。

### 5. **OAuth 1.0**

- **描述**：用于 OAuth 1.0 的认证方式，通常需要提供 **Consumer Key** 和 **Consumer Secret** 等信息。

- **用途**：适用于 OAuth 1.0 认证的 API，如 Twitter API 等。

- **使用方法**：
  
  - 填入 `Consumer Key`、`Consumer Secret`、`Token` 和 `Token Secret`，并且选择 **Signature Method**（如 HMAC-SHA1）。

### 6. **OAuth 2.0**

- **描述**：适用于 OAuth 2.0 认证方式，广泛应用于许多现代 Web 服务。

- **用途**：常用于 Google API、GitHub、Facebook、Twitter 等服务的 OAuth 2.0 身份验证。

- **使用方法**：
  
  - 输入 **Client ID**、**Client Secret**，并通过 **Access Token** 或使用 **Authorization Code** 流程进行认证。

### 7. **API Key**

- **描述**：通过 API 密钥进行身份验证，通常将 API 密钥放在请求头或查询参数中。

- **用途**：适用于使用 API 密钥验证的 API 服务。

- **使用方法**：
  
  - 输入 **Key** 和 **Value**，你可以选择 **Key** 放在请求头或 URL 参数中。

### 8. **Hawk Authentication**

- **描述**：Hawk 是一种基于 HTTP 协议的认证机制，用于保护与 API 进行的通信。

- **用途**：适用于需要 Hawk 认证的 API。

- **使用方法**：
  
  - 填入 **ID**、**Key**、**Algorithm** 等 Hawk 所需的字段。

### 9. **AWS Signature**

- **描述**：适用于 AWS（Amazon Web Services）API 的签名认证方式，使用 AWS Access Key 和 Secret Key 来生成签名。

- **用途**：用于 AWS 服务的认证。

- **使用方法**：
  
  - 填入 **AWS Access Key**、**AWS Secret Key**、**AWS Region** 和 **Service Name**。

### 10. **NTLM Authentication**

- **描述**：用于 Microsoft NTLM 认证协议，常用于 Windows 集成认证。

- **用途**：适用于要求 NTLM 认证的企业级服务。

- **使用方法**：
  
  - 输入 **Domain**、**Username** 和 **Password**。
