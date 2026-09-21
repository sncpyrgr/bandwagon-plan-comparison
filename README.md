# 搬瓦工套餐：全系列在售配置与价格对比，看完直接知道该买哪款

在搬瓦工（BandwagonHost）官网上选套餐，是一件很考验耐心的事。KVM、CN2 GIA-E、SLA、香港、东京、大阪、新加坡、迪拜……同一个"20G"放在不同系列里，价格能差出好几倍；有人花 $49.99 买到的是一整年的入门套餐，有人花同样的 $49.99 买到的只是一个 CN2 GIA-E 的月付。标价方式不统一、机房可以自由迁移、限量套餐靠抢——这些加在一起，让“搬瓦工套餐怎么选”成了每一年都在被重新问一遍的问题。

这篇文章把官网当前展示的全部在售套餐摊开来讲：每个系列的配置、价格、计费周期、线路差别，以及哪些套餐适合什么人。价格信息以官网套餐页当前展示为准，优惠部分会单独说明。

## 先看全貌：在售套餐分几条线

搬瓦工目前所有方案都是 KVM 架构，管理面板是自家开发的 KiwiVM，官方标称 99.95% 在线率保证（SLA 系列为 99.99%）。套餐体系可以粗略分成六块：

| 系列 | 起步价格 | 线路特点 | 适合谁 |
| --- | --- | --- | --- |
| KVM PROMO | $49.99/年 | 普通线路，十余个机房自由迁移 | 预算有限、对中国方向线路不敏感 |
| CN2 GIA-E（ECOMMERCE） | $169.99/年 | 洛杉矶 CN2 GIA/CTGNet，可迁入香港、日本机房 | 大陆访问为主的大多数人 |
| SLA（洛杉矶） | $65.89/季起 | 99.99% SLA、NVMe、AMD 专属核心 | 生产环境、有稳定性合同需求 |
| 香港 / 东京 CN2 GIA | $89.99/月 | 大中华区直连，延迟最低 | 对延迟极度敏感、预算充足 |
| 大阪 / 新加坡 CN2 GIA | $49.99/月 | CN2 GIA 直连，价格低于港日 | 想要亚洲节点但不想付港日价格 |
| 限量版套餐 | $19/年起 | 不定期上架，卖完即止 | 会蹲补货、手快的用户 |

所有套餐都包含 1 个独立 IPv4、一个 routed /64 IPv6 段、免费自动备份、免费快照，以及在各自可选机房之间的免费迁移——最后这条是搬瓦工和很多便宜 VPS 拉开差距的地方：换机房不丢数据，随时可以在面板里操作。

👉 [点这里直达全部在售套餐列表，按配置慢慢挑](https://bit.ly/BandwagonHost)

## 入门 KVM 系列：价格门槛最低的一档

这是搬瓦工最经典的入门系列，6 个配置，全部走普通线路。特点是机房选择多（洛杉矶、圣何塞、纽约、弗里蒙特、荷兰等十余个），可以随意迁移，但晚高峰对中国方向的表现一般——电信用户走的是普通 163 骨干网。

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| KVM 20G | 2 核 / 1 GB / 20 GB | 1 TB | 1 Gbps | — | $49.99 | [ 查看KVM套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=44) |
| KVM 40G | 3 核 / 2 GB / 40 GB | 2 TB | 1 Gbps | —（半年付 $52.99） | $99.99 | [ 查看KVM套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=45) |
| KVM 80G | 4 核 / 4 GB / 80 GB | 3 TB | 1 Gbps | $19.99 | $199.99 | [ 查看KVM套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=46) |
| KVM 160G | 5 核 / 8 GB / 160 GB | 4 TB | 1 Gbps | $39.99 | $399.99 | [ 查看KVM套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=47) |
| KVM 320G | 6 核 / 16 GB / 320 GB | 5 TB | 1 Gbps | $79.99 | $799.99 | [ 查看KVM套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=48) |
| KVM 480G | 7 核 / 24 GB / 480 GB | 6 TB | 1 Gbps | $119.99 | $1199.99 | [ 查看KVM套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=49) |

两个容易踩的坑：20G 只有年付，40G 只有半年付和年付，不存在月付选项；而 80G 往上反而有月付，计费周期设置并不对称，下单前要确认自己选的周期。如果服务器只是跑个博客、机器人或者挂个小服务，用户不在意大陆晚高峰速度，$49.99/年的 20G 就是整个搬瓦工在售套餐里最便宜的正价选择。

## CN2 GIA-E：大多数大陆用户真正该看的系列

要理解这个系列为什么贵，得先看官方对线路的解释。搬瓦工在官网把中国方向的 IP 链路分成四档：普通 163 骨干网（AS4134）高峰期丢包率可能超过 30%；CN2 GT（AS4809 GT）2019 年之后拥堵程度已经和 163 差不多；真正稳定的是 CN2 GIA（AS4809 GIA）和较新的 CTGNet（AS23764），但 GIA 传输成本最高，官方举例说某些市场 1 Gbps 的 GIA 连接一个月账单能到约 10 万美元——所以 GIA 套餐的价格下不来，是成本决定的，不是溢价。

CN2 GIA-E 系列全部走洛杉矶 CN2 GIA/CTGNet，其中官方主推的 USCA_9 机房把中国大陆方向流量分成三路：电信 CN2 GIA、联通 9929 精品网（AS10099）、移动 CMIN2，三家各走各的优质线路。同时这个系列还开放了十几个可迁移机房，包括香港 CN2 GIA 和日本 JPOS_1——花 $169.99/年，将来想换成香港机房也只需要在面板里点一下。

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| GIA-E 20G | 2 核 / 1 GB / 20 GB | 1 TB | 2.5 Gbps | $49.99 | $169.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| GIA-E 40G | 3 核 / 2 GB / 40 GB | 2 TB | 2.5 Gbps | $89.99 | $299.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=88) |
| GIA-E 80G | 4 核 / 4 GB / 80 GB | 3 TB | 2.5 Gbps | $56.99 | $549.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=89) |
| GIA-E 160G | 6 核 / 8 GB / 160 GB | 5 TB | 5 Gbps | $86.99 | $879.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=90) |
| GIA-E 320G | 8 核 / 16 GB / 320 GB | 8 TB | 5 Gbps | $159.99 | $1599.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=91) |
| GIA-E 640G | 10 核 / 32 GB / 640 GB | 10 TB | 10 Gbps | $289.99 | $2759.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=92) |
| GIA-E 1280G | 12 核 / 64 GB / 1280 GB | 12 TB | 10 Gbps | $549.99 | $5399.99 | [ 前往CN2 GIA-E购买页](https://bandwagonhost.com/aff.php?aff=79616&pid=93) |

重点提醒一次：20G 套餐的 $49.99 是**月付**价格，$169.99 才是年付。它和 KVM 20G 的 $49.99/年数字完全一样，含义完全不同。另外 80G 档月付 $56.99 比 40G 的 $89.99 还低，这是官方定价本身的特点，不是写错了。

多数面向大陆访客的博客、企业官网、代理服务，从 20G 或 40G 这两档选就够了。如果拿不准配置，先买小的，搬瓦工支持换机房，迁移免费。

👉 [查看CN2 GIA-E当前在售配置，直接选机房下单](https://bandwagonhost.com/aff.php?aff=79616&pid=87)

## 香港、东京 CN2 GIA：延迟最低，价格也最高

港日系列定位很明确：把服务器放到离大陆最近的地方。香港机房位于 Equinix HK2，电信 CN2 GIA、联通、移动三网直连；东京在 Equinix TY8，回程优先走 CN2 GIA。两个系列的配置和价格完全对齐，最低档 $89.99/月（年付 $899.99），比洛杉矶系列贵一个量级。

| 位置 | 套餐 | CPU / 内存 / 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 香港 | HK 40G | 2 核 / 2 GB / 40 GB | 500 GB | 1 Gbps | $89.99 | $899.99 | [ 查看香港套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=95) |
| 香港 | HK 80G | 4 核 / 4 GB / 80 GB | 1 TB | 1 Gbps | $155.99 | $1559.99 | [ 查看香港套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=96) |
| 香港 | HK 160G | 6 核 / 8 GB / 160 GB | 2 TB | 1 Gbps | $299.99 | $2999.99 | [ 查看香港套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=97) |
| 香港 | HK 320G | 8 核 / 16 GB / 320 GB | 4 TB | 1 Gbps | $589.99 | $5899.99 | [ 查看香港套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=98) |
| 香港 | HK 640G | 10 核 / 32 GB / 640 GB | 6 TB | 1 Gbps | $989.99 | $9989.99 | [ 查看香港套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=122) |
| 香港 | HK 1280G | 12 核 / 64 GB / 1280 GB | 8 TB | 1 Gbps | $1889.99 | $18989.99 | [ 查看香港套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=124) |
| 东京 | TYO 40G | 2 核 / 2 GB / 40 GB | 500 GB | 1.2 Gbps | $89.99 | $899.99 | [ 查看东京套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=108) |
| 东京 | TYO 80G | 4 核 / 4 GB / 80 GB | 1 TB | 1.2 Gbps | $155.99 | $1559.99 | [ 查看东京套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=109) |
| 东京 | TYO 160G | 6 核 / 8 GB / 160 GB | 2 TB | 1.2 Gbps | $299.99 | $2999.99 | [ 查看东京套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=110) |
| 东京 | TYO 320G | 8 核 / 16 GB / 320 GB | 4 TB | 1.2 Gbps | $589.99 | $5899.99 | [ 查看东京套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=111) |
| 东京 | TYO 640G | 10 核 / 32 GB / 640 GB | 6 TB | 1.2 Gbps | $989.99 | $9989.99 | [ 查看东京套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=123) |
| 东京 | TYO 1280G | 12 核 / 64 GB / 1280 GB | 8 TB | 1.2 Gbps | $1889.99 | $18989.99 | [ 查看东京套餐库存与价格](https://bandwagonhost.com/aff.php?aff=79616&pid=125) |

值不值要看场景。如果业务是大陆用户实时连麦、游戏、低延迟远程桌面，港日机房的延迟优势是洛杉矶给不了的；如果只是普通建站，洛杉矶 GIA-E 晚高峰也能跑出不错的体验，一年能省下小一千美元。

## 大阪、新加坡 CN2 GIA：亚洲节点的折中方案

这两组和港日规格接近，但起步价降到 $49.99/月（年付 $499.99），是“想要亚洲机房又不想付香港价格”的折中选择。大阪固定在大阪 Equinix，回程走 CN2 GIA/CTG；新加坡在 Equinix SG1。高配套餐的流量和带宽规格略高于港日同档。

| 位置 | 套餐 | CPU / 内存 / 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 大阪 | OSA 40G | 2 核 / 2 GB / 40 GB | 500 GB | 1.5 Gbps | $49.99 | $499.99 | [ 查看大阪套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=134) |
| 大阪 | OSA 80G | 4 核 / 4 GB / 80 GB | 1 TB | 1.5 Gbps | $86.99 | $869.99 | [ 查看大阪套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=135) |
| 大阪 | OSA 160G | 6 核 / 8 GB / 160 GB | 2 TB | 1.5 Gbps | $165.99 | $1665.99 | [ 查看大阪套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=136) |
| 大阪 | OSA 320G | 8 核 / 16 GB / 320 GB | 4 TB | 1.5 Gbps | $329.99 | $3279.99 | [ 查看大阪套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=137) |
| 大阪 | OSA 640G | 10 核 / 32 GB / 640 GB | 6 TB | 1.5 Gbps | $549.99 | $5549.99 | [ 查看大阪套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=138) |
| 大阪 | OSA 1280G | 12 核 / 64 GB / 1280 GB | 8 TB | 1.5 Gbps | $1059.99 | $10559.99 | [ 查看大阪套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=139) |
| 新加坡 | SG 40G | 2 核 / 2 GB / 40 GB | 500 GB | 1.5 Gbps | $49.99 | $499.99 | [ 查看新加坡套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=173) |
| 新加坡 | SG 80G | 4 核 / 4 GB / 80 GB | 1 TB | 1.5 Gbps | $86.99 | $869.99 | [ 查看新加坡套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=174) |
| 新加坡 | SG 160G | 6 核 / 8 GB / 160 GB | 2 TB | 2.5 Gbps | $165.99 | $1665.99 | [ 查看新加坡套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=175) |
| 新加坡 | SG 320G | 8 核 / 16 GB / 320 GB | 4 TB | 2.5 Gbps | $329.99 | $3199.00 | [ 查看新加坡套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=176) |
| 新加坡 | SG 640G | 10 核 / 32 GB / 640 GB | 6 TB | 5 Gbps | $549.99 | $5549.99 | [ 查看新加坡套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=177) |
| 新加坡 | SG 1280G | 12 核 / 64 GB / 1280 GB | 8 TB | 5 Gbps | $1059.99 | $10559.99 | [ 查看新加坡套餐当前价格](https://bandwagonhost.com/aff.php?aff=79616&pid=178) |

## SLA 系列：给“宕机要赔”的场景准备

SLA 系列全部位于洛杉矶，是搬瓦工唯一明确写入 99.99% 服务等级协议的产品线。硬件规格也和其他系列不同：本地 NVMe RAID-10 存储、AMD 专属核心、ECC 内存，机房为 Tier III 设施，官方列出的认证包括 SOC 1/2 Type 2、ISO 27001、PCI DSS 等。洛杉矶到中国的路由同样是 CN2 GIA/CTGNet + 联通 9929 + 移动 CMIN2 的组合，另外还与 Google、Apple、字节等网络有直接对等互联。

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 带宽 | 计费周期与价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| SLA 20G | 2 核 / 1 GB / 20 GB NVMe | 1 TB | 2.5 Gbps | $65.89/季 或 $239.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=164) |
| SLA 40G | 3 核 / 2 GB / 40 GB NVMe | 2 TB | 2.5 Gbps | $116.99/季 或 $399.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=165) |
| SLA 80G | 4 核 / 4 GB / 80 GB NVMe | 3 TB | 2.5 Gbps | $69.99/月 或 $699.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=166) |
| SLA 160G | 6 核 / 8 GB / 160 GB NVMe | 5 TB | 5 Gbps | $109.99/月 或 $1099.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=167) |
| SLA 320G | 8 核 / 16 GB / 320 GB NVMe | 8 TB | 5 Gbps | $199.99/月 或 $1999.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=168) |
| SLA 640G | 10 核 / 32 GB / 640 GB NVMe | 10 TB | 10 Gbps | $369.99/月 或 $3699.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=169) |
| SLA 1280G | 12 核 / 64 GB / 1280 GB NVMe | 12 TB | 10 Gbps | $699.99/月 或 $6999.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=170) |
| SLA 1280G（15TB流量） | 12 核 / 64 GB / 1280 GB NVMe | 15 TB | 10 Gbps | $879.99/月 或 $8799.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=171) |
| SLA 1280G（20TB流量） | 12 核 / 64 GB / 1280 GB NVMe | 20 TB | 10 Gbps | $1159.99/月 或 $11598.99/年 | [ 按配置挑选SLA套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=172) |

最低档 20G 采取季付起步（$65.89/季），不提供月付。个人玩票项目用不上这套配置；跑正经电商、支付相关或者对可用率有硬指标的业务，它才是对症的选项。

## 迪拜 ECOMMERCE：新增的中东机房系列

迪拜系列是相对较新的产品线，固定在迪拜 AEDXB_1 机房，同时开放迁移到洛杉矶 GIA 机房等其他位置。月付门槛是全站在售系列里最低的（20G 档 $19.99/月），年付与 GIA-E 对齐。需要注意社区测评对它面向中国方向的表现普遍持保留态度，有第三方评测明确给出“不推荐迪拜机房用于中国方向”的结论；如果用户在中东或欧洲，它才有作为第一机房的意义。

| 套餐 | CPU / 内存 / 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| DUBAI 20G | 2 核 / 1 GB / 20 GB | 500 GB | 1 Gbps | $19.99 | $169.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=114) |
| DUBAI 40G | 3 核 / 2 GB / 40 GB | 1 TB | 1 Gbps | $32.99 | $299.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=115) |
| DUBAI 80G | 4 核 / 4 GB / 80 GB | 2 TB | 1 Gbps | $56.99 | $549.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=116) |
| DUBAI 160G | 6 核 / 8 GB / 160 GB | 3 TB | 1 Gbps | $86.99 | $879.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=117) |
| DUBAI 320G | 8 核 / 16 GB / 320 GB | 4 TB | 1 Gbps | $159.99 | $1599.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=118) |
| DUBAI 640G | 10 核 / 32 GB / 640 GB | 5 TB | 1 Gbps | $289.99 | $2759.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=119) |
| DUBAI 1280G | 12 核 / 64 GB / 1280 GB | 6 TB | 1 Gbps | $549.99 | $5399.99 | [ 查看迪拜套餐详情](https://bandwagonhost.com/aff.php?aff=79616&pid=120) |

## 限量版套餐：便宜，但靠抢

除了常年在售的系列，搬瓦工会不定期放出限量款，数量有限、卖完下架，能不能买到取决于运气和手速：

- **THE PLAN 限量版**：2 核 / 2 GB / 40 GB SSD / 1 TB 月流量 / 2.5 Gbps，$99/年或 $29/季，可在 18 个机房之间迁移，包括香港 HK85 和日本 JPOS_1——等于用 $99 拿到一张覆盖港日 CN2 GIA 机房的“通票”。近期处于有货状态，但这类套餐随时可能售罄。
- **MINICHICKEN 限量版**：1 核 / 1 GB / 20 GB / 1 TB / 1 Gbps，$19/年，固定美国弗里蒙特机房，不可迁移。这是搬瓦工多年来价格最低的年付套餐，性能别抱期待，适合当备用机。
- **日本软银限量版**（JAPAN LIMITED EDITION）：1 核 / 512 MB / 10 GB / 500 GB，$69.99/年，固定大阪软银线路，不定期补货。
- **香港 HK85 限量版**：20 GB SSD / 500 GB 月流量 / 1 Gbps，$79.99/年，同样是隔很久才补一次的款式。

限量款的共同问题是补货节奏完全不可预测，官方也没有固定补货计划，第三方有每 5 分钟刷新的库存监控页和补货通知群可以蹲。想试试手气的话，从套餐列表进入看哪些限量款当前有货：[👉 查看限量套餐当前补货情况](https://bit.ly/BandwagonHost)

## 优惠码和省钱方式：能省的不多，但都值得拿

搬瓦工的正价套餐很少打折，能稳定拿到的折扣是长期循环优惠码。目前多个优惠信息站仍在同步的可用码是 **BWHCGLUKKB**，约 **6.77%** 循环折扣——重点是“循环”：首单生效，之后每次续费同价折扣。结账页的 Promotional Code 输入框填入即可。历史规律是每年双十一和黑五会出现力度更大的全场折扣码（往年在 10% 上下），大型活动码通常只活几天，比如 2026 年 2 月的 NODESEEK2026 上线两天就失效了。

下单页支持支付宝和主流国际信用卡付款。还有一件事比优惠码更值钱：搬瓦工续费按原价走，不存在“续费涨价”，但选择长周期本身就便宜——KVM 40G 月付不存在，半年付 $52.99、年付 $99.99，摊到每月差了 40% 以上。确定长期用，直接选年付。

👉 [选购时在结账页填入优惠码BWHCGLUKKB，循环6.77%折扣](https://bit.ly/BandwagonHost)

## 搬瓦工套餐怎么选：按场景对号入座

把上面所有信息压成几条决策路径：

1. **大陆访问为主，预算正常**：CN2 GIA-E 20G（$169.99/年）或 40G（$299.99/年）。绝大多数博客、企业站、轻量应用的答案就在这两档里。
2. **纯预算导向，不在意大陆晚高峰**：KVM 20G 年付 $49.99，或蹲 $19/年的 MINICHICKEN。
3. **延迟敏感、实时业务**：香港或东京 CN2 GIA，$89.99/月起；预算不够就买 GIA-E 然后迁移到香港机房试试，或者蹲 THE PLAN。
4. **生产环境、有可用率要求**：洛杉矶 SLA 系列，99.99% SLA 写进合同，$65.89/季起。
5. **中东、欧洲方向用户**：迪拜系列有它的位置，中国方向用户基本可以忽略。
6. **想低成本占个亚洲坑位**：大阪、新加坡 CN2 GIA 的 $49.99/月档位。

一个通用建议：搬瓦工的套餐普遍支持在各自机房池内免费迁移且不丢数据，所以“买小一点、不够再换机房”在这个平台上是成立的策略，不必第一次下单就顶配。

## 常见问题

**月付和年付差价为什么这么大？**
官方定价策略就是用长周期换低价，GIA-E 20G 月付 $49.99、年付 $169.99，年付相当于打了约 2.9 折的月均价格。短期试用可以月付，确定留下就转年付。

**买错机房怎么办？**
在 KiwiVM 面板里发起迁移即可，套餐可选范围内的机房之间免费切换、数据自动带走。GIA-E 系列的可选池覆盖十几个机房，包括香港和日本。

**为什么有的套餐显示缺货？**
常规系列偶尔缺货通常很快恢复；限量款则完全看官方放量，没有固定时间表。第三方库存监控页每 5 分钟更新一次全系列库存状态。

**支持哪些系统？**
官方套餐页列出的可装系统包括 AlmaLinux、RockyLinux、CentOS、Debian、Ubuntu、CentOS Stream、Fedora，也支持自行挂载 ISO 安装。

**优惠码对所有套餐都有效吗？**
循环码 BWHCGLUKKB 适用于全站 VPS 套餐并在续费时持续生效；限量款本身已是特价，叠加效果以结账页实际显示为准。
