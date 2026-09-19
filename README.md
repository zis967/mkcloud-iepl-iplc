# mkcloud 专线 VPS：广港 IEPL、沪日 IPLC 怎么选？全套餐价格、优惠码与避坑要点一次讲清

跨境电商跑店铺、独立站管账号，最怕的不是流量不够，而是 IP 关联和跨境链路抖动。mkcloud 专线 VPS 卖的就是这两件事的解决方案：IEPL/IPLC/IX 三类跨境专线，每台 VPS 配独立入口 IP 和独立出口 IP。这篇文章把它的线路差异、目前在售的全部套餐价格、优惠码用法和退款规则整理在一起，帮你下单前把账算清楚。

## mkcloud 专线 VPS 是什么？和普通 VPS 差在哪

先说结论：mkcloud 不是一家普通的云服务器商家，它卖的核心不是 CPU 和内存，而是「国内入口 → 境外出口」这段专线。2023 年上线，国人商家，主营三条传统专线和一类云厂接入产品：

- **广港 IEPL**：广东到香港的IEPL 专线，端内延迟 1~2ms，入口可选八线动态 BGP、电信、移动、联通或三线；
- **沪日 IPLC / 沪美 IPLC**：上海出发的物理专线，沪日端内延迟 25~28ms，沪美 124~134ms；
- **IX 上云专线（沪日、深港、沪港等）**：走云厂内网接入，价格便宜一截，但要求你先有一台 supported 的国内云服务器做前置。

配置本身并不豪华，入门档基本是 1 核 2G、20GB SSD 这类水平。多花的钱买的是三样东西：端对端的专线质量、每台机器一对独立 IP（1 个入口 + 1 个出口）、以及不会被平台风控盯上的干净 IPv4。第三方测评普遍提到它的 IP 在 scamalytics 一类检测里表现干净，做 eBay、Shopee 这类对 IP 敏感的平台账号有实际意义。

一句话概括区别：普通 VPS 是「租一台境外电脑」，mkcloud 是「租一条从国内某省出发到境外的固定通道，附带一台电脑」。

## 线路怎么选：先看你的业务在哪、人在哪

mkcloud 官网在售线路不止一条，选错线路是新手最容易踩的坑。核心判断只有两个变量：目标市场在哪，你或你的团队从哪个省份连入。

| 线路 | 端内延迟 | 出口 | 入口要求 | 适合场景 |
| --- | --- | --- | --- | --- |
| 广港 IEPL | 1~2ms | 香港 BGP | 广东本地或八线 BGP 直连 | 华南用户、做亚马逊/eBay/TikTok 通用账号 |
| 沪日 IPLC | 25~28ms | 日本 BGP | 电信/UCloud BGP | 面向日本市场、长三角用户 |
| 沪美 IPLC | 124~134ms | 美国 BGP | 电信 BGP | 美区业务、TikTok 美区、跨境 CI/CD |
| 沪日上云互联 IX | 25~28ms | 日本 BGP | 需云厂 BGP 前置 | 已有阿里/腾讯/百度云等云服务器的团队 |
| 深港/沪港 IXP | 1~2ms | 香港 | 需云厂 BGP 前置 | 预算敏感的香港出口需求 |

几个容易忽略的点：

1. 表里的延迟是「端内延迟」，也就是入口到出口这一段，不含你本地到入口的部分。官方知识库明确提醒过这一点，别拿它当「你到 Google 的延迟」理解。
2. IX 上云专线只允许云厂 BGP 网络连入，上海入口目前支持阿里云、腾讯云、百度云全网，以及火山云、华为云、UCloud 华东。前置云服务器本身要另外花钱，算总价时别漏掉。
3. 广港 IEPL 通用性最强，这也是它卖得贵一点的原因；如果只是个人偶尔用用境外网络，这个价位并不划算，后面会展开。

## 全套餐价格表：流量计费产品（月付，人民币）

下面这张表覆盖官网当前在售的流量计费套餐，配置为各档固定规格，价格来自商店页与官方知识库口径。计量型套餐的流量按**上行 + 下行双向合计**，超量后暂停，可自助购买流量重置或工单补差价升级——这条规则直接影响你该买哪一档，后面单独讲。

| 线路 | 套餐（月流量） | CPU/内存/硬盘 | 峰值带宽 | 端内延迟 | 月付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- |
| 广港 IEPL | 500GB | 1核2G/20GB | 150M | 1~2ms | ¥228 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 广港 IEPL | 1TB | 1核2G/20GB | 200M | 1~2ms | ¥358 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 广港 IEPL | 2TB | 2核4G/40GB | 300M | 1~2ms | ¥568 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 广港 IEPL | 4TB | 2核4G/40GB | 300M | 1~2ms | ¥998 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 广港 IEPL | 6TB | 4核8G/60GB | 500M | 1~2ms | ¥1388 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 广港 IEPL | 10TB | 4核8G/60GB | 500M | 1~2ms | ¥2288 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 广港 IEPL | 20TB | 4核8G/60GB | 1G | 1~2ms | ¥4500 | [ 查看广港 IEPL 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd) |
| 沪日 IPLC | 500GB | 1核2G/20GB | 150M | 25~28ms | ¥228 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪日 IPLC | 1TB | 1核2G/20GB | 200M | 25~28ms | ¥358 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪日 IPLC | 2TB | 2核4G/40GB | 300M | 25~28ms | ¥568 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪日 IPLC | 4TB | 2核4G/40GB | 300M | 25~28ms | ¥998 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪日 IPLC | 6TB | 4核8G/60GB | 500M | 25~28ms | ¥1388 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪日 IPLC | 10TB | 4核8G/60GB | 500M | 25~28ms | ¥2288 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪日 IPLC | 20TB | 4核8G/60GB | 1G | 25~28ms | ¥4500 | [ 查看沪日 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-jp-sh) |
| 沪美 IPLC | 100GB | 1核2G/20GB | 150M | 124~134ms | ¥198 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪美 IPLC | 500GB | 1核2G/20GB | 150M | 124~134ms | ¥258 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪美 IPLC | 1TB | 1核2G/20GB | 200M | 124~134ms | ¥428 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪美 IPLC | 2TB | 2核4G/40GB | 300M | 124~134ms | ¥698 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪美 IPLC | 4TB | 2核4G/40GB | 300M | 124~134ms | ¥1258 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪美 IPLC | 6TB | 4核8G/60GB | 500M | 124~134ms | ¥1758 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪美 IPLC | 10TB | 4核8G/60GB | 500M | 124~134ms | ¥2888 | [ 查看沪美 IPLC 套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-us-sh) |
| 沪日上云互联 IX | 1TB | 2核4G/40GB | 200M | 25~28ms | ¥166 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 2TB | 2核4G/40GB | 300M | 25~28ms | ¥268 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 3TB | 2核4G/40GB | 500M | 25~28ms | ¥358 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 6TB | 4核8G/40GB | 1G | 25~28ms | ¥688 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 10TB | 4核8G/40GB | 1G | 25~28ms | ¥1125 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 20TB | 4核8G/40GB | 1G | 25~28ms | ¥2150 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 30TB | 4核8G/60GB | 2G | 25~28ms | ¥3165 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 沪日上云互联 IX | 50TB | 8核8G/60GB | 2G | 25~28ms | ¥5222 | [ 查看沪日 IX 专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 深港 IXP | 入门共享档 | 1核2G/20GB | 200M | 1~2ms | ¥158 起 | [ 查看深港 IXP 现价](https://bit.ly/MKCLoud) |

除了这张表里的产品，官网还挂有港法 IPLC、上海 CN2、厦港/泉港高防等线路，以及 200M–2000M 的广东大带宽独享 IEPL。这几条属于更细分的场景（比如高防需求、欧洲出口），页面上没有统一标价，需要的话进商店按线路询价。

## 独享带宽套餐：不限流量，但按带宽付费

第二类产品逻辑完全不同：不计量流量，按独享带宽档位收费，适合需要长时间持续传输的场景——比如大文件同步、直播推流、AI 数据拉取。

| 线路 | 独享带宽 | 配置 | 月付 | 购买 |
| --- | --- | --- | --- | --- |
| 沪港 IPLC | 5M 独享 | 2核4G/40GB | ¥650 | [ 查看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-ex) |
| 沪美 IPLC | 5M 独享 | 2核4G/40GB | ¥850 | [ 查看沪美独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/shh-us-ex) |
| 沪美 IPLC | 10M 独享 | 2核4G/40GB | ¥1300 | [ 查看沪美独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/shh-us-ex) |
| 沪美 IPLC | 20M 独享 | 2核4G/40GB | ¥2560 | [ 查看沪美独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/shh-us-ex) |
| 沪美 IPLC | 50M 独享 | 4核8G/60GB | ¥6000 | [ 查看沪美独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/shh-us-ex) |
| 沪美 IPLC | 100M 独享 | 4核8G/60GB | ¥11500 | [ 查看沪美独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/shh-us-ex) |
| 上云互联沪港 IX | 100M 独享 | — | ¥1600 | [ 查看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 上云互联沪港 IX | 200M 独享 | — | ¥3000 | [ 查看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 上云互联沪港 IX | 500M 独享 | — | ¥6000 | [ 查看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 上云互联沪港 IX | 1G 独享 | — | ¥9000 | [ 查看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 上云互联沪港 IX | 2G 独享 | — | ¥16000 | [ 查看沪港独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 沪日上云 IX | 20M 独享 | — | ¥1000 | [ 查看沪日独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-ex) |
| 沪日上云 IX | 50M 独享 | — | ¥2250 | [ 查看沪日独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-ex) |
| 沪日上云 IX | 100M 独享 | — | ¥3700 | [ 查看沪日独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-ex) |
| 沪日上云 IX | 200M 独享 | — | ¥7000 | [ 查看沪日独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-ex) |
| 沪日上云 IX | 500M 独享 | — | ¥17500 | [ 查看沪日独享带宽](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-ex) |
| 厦港高防 IEPL | 200M 独享 | 100Gbps DDoS 高防 | ¥6000 | [ 查看厦港高防专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/xm-hk-ex) |
| 厦港高防 IEPL | 500M 独享 | 100Gbps DDoS 高防 | ¥13500 | [ 查看厦港高防专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/xm-hk-ex) |
| 厦港高防 IEPL | 1G 独享 | 100Gbps DDoS 高防 | ¥24000 | [ 查看厦港高防专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/xm-hk-ex) |
| 厦港高防 IEPL | 2G 独享 | 100Gbps DDoS 高防 | ¥46000 | [ 查看厦港高防专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/xm-hk-ex) |
| 厦港高防 IEPL | 5G 独享 | 100Gbps DDoS 高防 | ¥110000 | [ 查看厦港高防专线](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/xm-hk-ex) |

官方知识库里对沪港独享入门给过 388 元/月（5Mbps）的口径，商店页目前展示的 5M 独享档为 650 元/月，两边存在出入。以你下单时购物车的实时标价为准，这是唯一的最终口径。

## 流量计费还是独享带宽？算一笔账就明白了

两条产品线的选择，本质是「你传多少」和「你传多久」的问题。

流量计费按双向合计。举个例子：沪日 IPLC 1TB 档，你上传 600GB、下载 400GB，额度就用完了，超量会直接暂停而不是慢速继续跑。日常店铺管理、账号运营这种突发式、总量可控的用法，流量计费几乎总是更便宜。

独享带宽不限流量，但速率封顶。沪美 5M 独享月付 850，看起来比 1TB 流量档的 428 贵一倍，但 5Mbps 持续跑满一个月大约能传 1.5TB 以上，对持续传输场景反而划算。第三方测评也算过类似的账，结论一致：**间歇性使用选流量计费，7×24 持续传输选独享**。

还有一个官方明确说过的点：共享和独享不影响账号能否通过平台审核，别为「主号必须独享」这类说法多花钱。

## 优惠码和省钱顺序

目前多方 2026 年的优惠信息汇总如下。需要注意，官方活动页对部分优惠码标注了「活动期内有效」，实际能不能抵扣以结算页为准：

| 优惠码 | 适用范围 | 折扣 |
| --- | --- | --- |
| MK-8.8 | 流量计费套餐 | 8.8 折（多方信息显示可循环使用） |
| MK-7.8 | 独享带宽产品 | 首月 7.8 折 |
| MK-IEPL-WELCOME | IEPL 线路 | 9 折 |
| MK-IPLC-WELCOME | IPLC 线路 | 9 折 |
| CLOUD-2T-NEW | 上云互联 2TB 档 | 专项优惠 |

下单时的顺序建议：先选线路和套餐，再在购物车「优惠劵码」一栏填码，系统会显示是否循环生效。广港 IEPL 1TB/2TB 这两个档位用 MK-8.8 之后分别是 315 元和 500 元左右，是第三方推荐频率最高的组合。IXCLOUD、US-6.9 这类码出自已结束的预售活动，官方已标注失效，别按历史折后价做预算。

## 购买流程和退款规则，下单前看一眼

流程本身不难：注册账号（站内有实名认证环节）→ 选线路进商店 → 选套餐和系统 → 填优惠码 → 支付。官方称多数专线 VPS 支持下单后约 1 分钟自动开通。

开通后你会拿到入口地址和登录信息，Windows 用 RDP、Linux 用 SSH 连上去就能用。注意一个常见误解：连上的是入口，业务流量从境外出口向外访问，海外出口端不接受外部连入。官方知识库建议开通后用 ping、mtr 和 iperf3 分段测一下本地到入口、入口到出口的质量，这比看宣传延迟实在。

退款政策比较严格，直接引用官方口径：**仅质量问题支持退款**，需要在工单中提交测试截图和具体问题，由商家审核判断；不支持开通后更换到其他地域。所以线路方向拿不准的时候，先用最小档位（比如沪美 100GB 档 198 元）验证链路，再决定要不要上大套餐。

## 适合谁买，不适合谁

适合的情况：团队在做跨境电商多账号运营（Shopee、eBay、亚马逊、TikTok），需要独立 IP 隔离关联风险；做独立站或海外社媒矩阵，对国内连入境外服务器的稳定性有要求；或者有对港、对日的持续传输需求。

不适合的情况也说清楚。mkcloud 最便宜的共享入门档也要 158~228 元/月，只是偶尔需要境外网络的个人用户，普通机场或消费级 VPN 的成本不到它的零头，没必要上这个配置。另外，IX 上云专线必须搭配指定的国内云服务器做前置，如果你连云厂前置都不想维护，直接看 IEPL/IPLC 直连款。

最后提醒一句价格之外的事：计量型套餐超量即停、退款仅限质量问题，这两条决定了「先小档验证、再升级扩容」是最稳的入手路径。需要的时候可以从[👉 广港 IEPL 套餐页](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/sh-hk-gd)或[👉 沪日 IX 专线页](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh)进入，按当月实际标价和优惠码抵扣结果做最终决定。
