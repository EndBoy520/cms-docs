# 常见问题


## 启动失败

### 示例1：
```bash
RuntimeError: this license key is expired (1:11086)
```

**版本过期了，升级到最新版即可**


### 示例2：

```bash
cloud-media-sync  | INFO:     2025-03-03 22:26:05,135 - main      :  54 ➜ 开始校验捐赠码....
cloud-media-sync  | ERROR:    2025-03-03 22:26:05,142 - mhttp     : 156 ➜ HTTP请求失败: 连接错误
cloud-media-sync  | ERROR:    2025-03-03 22:26:05,146 - mhttp     : 156 ➜ HTTP请求失败: 连接错误
cloud-media-sync  | INFO:     2025-03-03 22:26:05,147 - main      :  56 ➜ 校验捐赠码结束....
```

**你的docker连不上cms的授权服务器，可以给docker加上代理启动，如下示例**

```yaml
- HTTP_PROXY=http://192.168.2.118:7890
- HTTPS_PROXY=http://192.168.2.118:7890
- NO_PROXY=localhost,127.0.0.0/8,10.0.0.0/8,172.0.0.0/8,192.168.0.0/16
```
