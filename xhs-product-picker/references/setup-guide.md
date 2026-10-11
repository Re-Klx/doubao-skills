# 飞书案例库配置指南

## 你为什么需要这个

本 skill 自带一份离线案例摘要，不连飞书也能用。但连上在线案例库后，你可以：
- 搜索 200+ 条真实小红书虚拟产品案例
- 获取持续更新的最新案例数据
- 用真实销量/定价数据验证选品方向

配置只需 2 步，2 分钟。

---

## 第 1 步：复制案例库到你的飞书

打开这个链接：

**https://my.feishu.cn/base/FbiAbRsyeaUTiOswW6Uc2l0TnQh?from=from_copylink**

点击右上角 **「复制到我的空间」**（或「另存为」），案例库会出现在你的飞书云空间里。

## 第 2 步：准备在线访问权限

打开你刚复制的 Base，确认当前运行环境使用的飞书连接器或安全配置可以访问它。不要把 token、Cookie、密码或个人访问凭证直接粘贴到聊天里。

如果当前环境没有飞书连接器：

- 继续使用 skill 自带的 `references/case-data.md` 静态摘要；
- 不要把静态摘要称为实时数据；
- 需要最新案例时，再在支持飞书连接器的环境中运行本 skill。

如果运行环境要求填写 Base Token，浏览器地址栏里的 URL 格式通常是：

```
https://xxx.feishu.cn/base/XXXXXXXXXXXXX
```

`/base/` 后面的那串字符通常就是 Base Token。把它填入运行环境提供的安全配置，不要改写并提交公开的 `SKILL.md`：

```yaml
# 你的本地/安全配置示例
base_token: YOUR_BASE_TOKEN_HERE
table_id: tblvkzwrwK6dFzwn
```

> Table ID 复制后一般不变。如果不一样，在你复制后的 Base 里点进数据表，URL 中 `/table/` 后面的就是 table_id。

## 第 3 步：告诉 Agent 配置完成

然后对这个 skill 说一句：**「我已配置好飞书案例库」**。只有当当前环境确实能调用飞书连接器并通过权限检查时，我才会开始用在线案例库做选品验证；否则继续使用离线摘要，并明确告诉你。

---

## 可选：方法论文档

如果你有选品方法论文档的飞书 wiki 权限，同样复制后填入 wiki token 和 doc obj_token。没有就跳过，不影响使用。
