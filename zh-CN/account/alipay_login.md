---
name: 支付宝登录
---
    
### 前端访问链接

    http://weiduchuangzao.xyz/weidu/api/v1/users/alipay/auth_url


    中间url：  https://openauth.alipay.com/oauth2/publicAppAuthorize.htm?app_id=2021002128644356&scope=auth_user&redirect_uri=http://weiduchuangzao.xyz/auth/redirect

  ### 回调接口返回样例

    curl 'http://weiduchuangzao.xyz/auth/redirect?app_id=2021002128644356&source=alipay_wallet&scope=auth_user&auth_code=275864cc74604d7a8a2c6e179606ZX02' \
      -H 'Connection: keep-alive' \
      -H 'Pragma: no-cache' \
      -H 'Cache-Control: no-cache' \
      -H 'Upgrade-Insecure-Requests: 1' \
      -H 'User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/88.0.4324.96 Safari/537.36' \
      -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9' \
      -H 'Accept-Language: zh-CN,zh;q=0.9' \
      --compressed \
      --insecure

    HTTP/1.1 200 OK
    Server: nginx
    Date: Mon, 22 Feb 2021 06:24:13 GMT
    Content-Type: application/json
    Content-Length: 0
    Connection: keep-alive
    Set-Cookie: weichuangAUTHTOKEN=wtfeio3zojb99k5xk9asx98anw; Path=/; Domain=0.0.0.0; Expires=Mon, 22 Feb 2021 06:24:13 GMT; HttpOnly
    Set-Cookie: weichuangUSERID=o4cnejab1ff1tece3et8xajaxw; Path=/; Domain=0.0.0.0; Expires=Mon, 22 Feb 2021 06:24:13 GMT
    Set-Cookie: weichuangCSRF=jfp8haz3o38h8ntkuiw35cpoew; Path=/; Domain=0.0.0.0; Expires=Mon, 22 Feb 2021 06:24:13 GMT
    Token: wtfeio3zojb99k5xk9asx98anw
    X-Request-Id: ehoijgsoapgaek6iauaakquwpw


