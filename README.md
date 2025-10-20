### 感觉跳转加群有点流氓行为 改成

<img width="1708" height="884" alt="image" src="https://github.com/user-attachments/assets/ca35ae39-6971-4291-b182-28cb292c0353" />


###  Snippets

<img width="1128" height="801" alt="image" src="https://github.com/user-attachments/assets/ae108dd2-c543-4a63-b448-d56d4d520e1d" />

#### 加入多客户端支持 域名/你的uuid即可看见

###  配套工具

| 类型 | 描述 | 链接 |
| :--- | :--- | :--- |
|  **文字教程** | 详细的部署与使用说明博客文章 | [https://joeyblog.net/yuanchuang/1146.html](https://joeyblog.net/yuanchuang/1146.html) |
|  **Workers视频教程** | 直观的操作演示和功能讲解 | https://youtu.be/Rlypv_iswD8 |
|  **Snippets视频教程** | 直观的操作演示和功能讲解 | https://www.youtube.com/watch?v=xeFeH3Akcu8 |

###  部署
	
加入了千呼万唤的订阅每15分钟自动优选一次
| 变量名 | 值 | 说明 |
| :--- | :--- | :--- |
| `u` | `你的 UUID` | **必需**。 |
| `p` | `proxyip` | **可选**。 |
| `s` | `你的SOCKS5地址` | **可选**。用于将所有出站流量通过 SOCKS5 代理转发，格式为 `user:pass@host:port` 或 `host:port`。 |
| `d` | `你的订阅地址` | **可选**。不填就是/你的uuid |
| `yx` | `自定义优选IP/域名` | **可选**。自定义优选IP和域名，支持端口，格式：`1.1.1.1:8080,2.2.2.2,example.com:8443`。当设置此变量时，将只使用原生地址和自定义优选，不生成默认优选。 |
| `qj` | `no` | **可选**。降级控制，设置为`no`时启用降级模式：CF直连失败→SOCKS5连接→fallback地址。 |
| `dkby` | `yes` | **可选**。端口控制，设置为`yes`时禁用80端口节点，只保留443端口和其他非80端口节点。 |
| `yxby` | `yes` | **可选**。优选控制，设置为`yes`时关闭所有优选功能，只使用原生地址，不生成优选IP和域名节点。 |

###  新功能

#### 自定义优选支持
- 支持自定义优选IP和域名，完全替代默认优选
- 格式：`yx=1.1.1.1:8080,2.2.2.2,example.com:8443`
- 支持IPv4/IPv6地址和域名，支持自定义端口
- 设置后只生成原生地址+自定义优选，跳过默认优选

#### 智能降级
- 当CF直连失败时自动降级
- 设置：`qj=no` 启用降级模式
- 降级流程：CF直连失败 → SOCKS5连接 → fallback地址
- 提高连接成功率，增强容错能力

#### 端口控制
- 支持禁用特定端口节点
- 设置：`dkby=yes` 禁用80端口节点
- 只保留443端口和其他非80端口节点
- 适用于需要避免80端口限制的场景

#### 优选控制
- 支持完全关闭优选功能
- 设置：`yxby=yes` 关闭所有优选
- 只使用原生地址，不生成优选IP和域名节点
- 适用于需要简化节点列表的场景

###  致谢

  * 本项目基于 [zizifn/edgetunnel](https://github.com/zizifn/edgetunnel) 修改，感谢原作者的贡献。
  * 本项目内置ProxyIP 来自CM [[cmliu](https://github.com/cmliu)) ，感谢作者的贡献。
  * 本项目反代IP来着前端独苗kejiland 来自CM [[qwer-search](https://github.com/qwer-search)) ，感谢作者的贡献。
## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=byJoey/cfnew&type=Timeline)](https://www.star-history.com/#byJoey/cfnew&Timeline&LogScale)
