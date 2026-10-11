# XiaoQi-sgmodule

小火箭（Shadowrocket）自用聚合去广告模块。

> 本仓库为个人自用，仅作模块托管，规则不定期更新。

## 模块作用

| 作用 | 覆盖范围 |
|---|---|
| **域名级广告/追踪拦截** | 全部 App 和网页：拦截广告联盟、数据埋点、追踪类域名约 4000 个，及 850+ 条广告 URL 路径 |
| **APP 启动页/开屏广告拦截** | 银行、购物、出行、视频、小说等 500+ 常用 App：开屏广告、首页弹窗、活动推荐位、悬浮广告 |
| **番茄小说去广告** | 章节内广告图、广告签名图、活动弹窗、数据埋点 |
| **白名单放行** | iCloud、GitHub、支付/登录接口、推送服务等易误杀域名优先放行，避免 App 功能异常 |

> 规则合并时已去重；白名单排在最前，运行时优先级最高。

## 订阅地址

仓库更新后，以下地址即为最新版（jsDelivr 有几分钟缓存）：

```
https://raw.githubusercontent.com/SherryBX/XiaoQi-sgmodule/main/xiaoqi.sgmodule
https://fastly.jsdelivr.net/gh/SherryBX/XiaoQi-sgmodule@main/xiaoqi.sgmodule
```

安装：Shadowrocket → 首页「配置」→ 模块 →「+」→ 输入上述 URL。

## 注意事项

- URL 级规则（URL-REGEX）与 [Script] 需要开启 MITM 解密才能匹配 HTTPS 流量；域名级拦截不受影响。请确保 Shadowrocket 已安装并信任 CA 证书。
- [Script] 引用远程脚本（raw.githubusercontent.com），国内网络拉取可能需要代理。
- 通配符黑名单中 7 条超宽泛模式（`ad.*`、`ads-*`、`ad-*.com` 等）已刻意跳过，避免误杀正常网站。
