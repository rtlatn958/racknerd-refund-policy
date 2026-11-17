# RackNerd 退款政策：默认不退是真的吗？取消服务能拿回钱吗？年付买错了怎么处理（附工单流程与全套餐对比）

RackNerd 的服务条款里，关于退款只有一句话：付款后默认不退，退款按个案酌情处理。官方没有 30 天退款保证，也没有 7 天无理由，网上流传的"30 天退款"说法与条款对不上。已经付了钱的，下面有取消和 Billing 工单的具体走法；还在犹豫的，往下看怎么把试错成本压到最低。

> **多数人的选择**：只想试试水，买 KVM VPS 月付 1 GB（第三方整理标价 $17.99/月），跑一两周不合适就停；目标机房测过、确定要长期用，再上年付特价 1 GB Special（$21.99/年）。
> 👉 [查看 RackNerd 当前套餐与实时价格](https://bit.ly/RacKnerd)

## 官方条款到底怎么写的

服务条款里那句原文是：

> Refunds are issued on a case-by-case basis since by default no refunds are provided once payment is received.

中文意思是：付款完成后默认不退款，退款申请按个案酌情处理。

这句话留了个口子，个案可以谈。但它没有给出任何退款窗口，没有"几天内可退"的条款，也没有按剩余周期比例退款的规则。官方知识库的措辞比条款更硬，直接写明不提供退款，也没有退款保证（money back guarantee），并建议想试用的用户先按月付下单，确认满意再转长期。

几个容易漏掉的细节：

- **账户余额不退。** 提前充进账户的 prepaid credit 明确不能退，只能用于后续下单。
- **退款不会自动批。** 服务开通的那一刻，机房和硬件的成本就已经产生，每笔退款都要人工看。
- **拒付代价很高。** 走信用卡 chargeback 会触发 $125–$250 行政费，账户可能被暂停，之后想继续用要先结清这笔钱。$125 起跳的罚款已经远超一台年付 VPS 的价钱。

这条政策跟它的定价是一套的。年付套餐压到二十几美元一年，再支持随时退款，这个价格撑不住。

## 取消服务和申请退款是两条流程

客户端那个 Request Cancellation 按钮只停服务，不处理钱。点完之后系统会自动开一张工单通知 billing 团队，客服不会因为这张工单主动考虑退款。要退钱得另开一张 Billing 工单。

取消服务的步骤：

1. 登录 RackNerd 客户中心
2. Services → My Services，点进要取消的服务
3. 点 Request Cancellation
4. 填取消原因，选类型：Immediate（立即取消）或 End of Billing Period（到期取消）
5. 先把数据备份到本地

第 5 步是重点。选 Immediate 之后，系统在 24 小时内终止服务，磁盘数据立即删除且不可恢复。官方条款里也写明 RackNerd 不对数据完整性负责，建议用户自行保留异地备份。误点了 Immediate，发现得早可以马上提工单让客服重新开通，过了 24 小时这个窗口就难办了。选 End of Billing Period 则是服务用到周期结束，期间一切正常，到期不续费。

申请退款另开一张工单，部门选 Billing，内容写清楚三件事：什么时候买的、遇到什么问题、希望怎么处理。如果是技术故障，附上 ping、traceroute 或截图，让客服能判断问题出在服务端。礼貌提出你能接受的替代方案，比单纯要求全额退款更容易推进。

👉 [下单前先核对配置，省掉后面整套取消流程](https://bit.ly/RacKnerd)

## 什么情况有戏，什么情况基本没戏

先说不乐观的那一类。以下情形被拒的概率很高：

- 服务已经用了一段时间，哪怕只有几天
- 年付订单已经开通，机房成本已经计入
- 纯个人需求变更，没有技术故障
- 已经跑满当月带宽或资源额度

再看相对有空间的情形。这些不是官方承诺，是按条款 "case-by-case" 整理的常见处理逻辑：

- 刚开通几分钟就发现服务异常，比如 VPS 起不来、IP 不通
- 独立服务器超过 72 小时仍未交付（官方对 Dedicated Server 的交付承诺是 72 小时内）
- 明显技术故障导致服务无法正常使用
- 还没有产生实际使用记录

被拒之后，客服通常会主动给几个替代方案：退款转成账户余额供下次抵扣、换机房位置、换更高配置的套餐补差价。前提是你愿意继续在 RackNerd 体系里消费。想直接拿回现金，难度明显更高。

被拒时别威胁拒付。行政费按 $125–$250 收，账号还可能被停，为一台二十几美元的年付机器不值当。

👉 [还在犹豫的话，先用月付方式跑一个月](https://bit.ly/RacKnerd)

## 全套餐对比

下面是 RackNerd 官网公开的主要产品线。价格和配置来自第三方整理的资料，本次没有与官网价格页逐项交叉核对，实际以下单页显示为准，促销价也随时可能调整。

### KVM VPS 常规套餐

| 套餐 | vCPU / 内存 | 存储 | 月流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| 512 MB | 1 vCore / 512 MB | 30 GB RAID-10 | 500 GB | $26.99/年 * | [ 选择此方案](https://bit.ly/RacKnerd) |
| 1 GB | 2 vCore / 1 GB | 50 GB RAID-10 | 1 TB | $17.99/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 2 GB | 3 vCore / 2 GB | 75 GB RAID-10 | 2 TB | $20.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 4 GB | 4 vCore / 4 GB | 130 GB RAID-10 | 3 TB | $24.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 6 GB | 5 vCore / 6 GB | 170 GB RAID-10 | 4 TB | $27.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 8 GB | 6 vCore / 8 GB | 220 GB RAID-10 | 5 TB | $36.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 12 GB | 7 vCore / 12 GB | 300 GB RAID-10 | 6 TB | $55.99/月 | [ 选择此方案](https://bit.ly/RacKnerd) |

\* 512 MB 这一档在公开整理资料里表头标"月付"、价格却写成 $26.99/年，两个字段对不上，下单前请在配置页确认计费周期，别按"$26.99 一个月"来理解。

### KVM VPS 年付特价

| 套餐 | vCPU / 内存 | 存储 | 月流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| 1 GB Special | 1 vCore / 1 GB | 20 GB PURE SSD | 3 TB | $21.99/年 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 2 GB Special | 2 vCore / 2 GB | 35 GB PURE SSD | 5 TB | $35.99/年 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 4 GB Special | 3 vCore / 4 GB | 60 GB PURE SSD | 7 TB | $59.99/年 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 6 GB Special | 6 vCore / 6 GB | 100 GB PURE SSD | 12 TB | $89.99/年 | [ 选择此方案](https://bit.ly/RacKnerd) |
| 8 GB Special | 7 vCore / 8 GB | 150 GB PURE SSD | 20 TB | $119.99/年 | [ 选择此方案](https://bit.ly/RacKnerd) |

### Hybrid Dedicated Server

| 机型 | 核心 / 内存 | 存储 | 月流量 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| Dual Xeon E5-2690 2.90GHz | 2 核 / 4 GB | 120 GB HDD | 5 TB | $39/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2690 2.90GHz | 4 核 / 8 GB | 250 GB HDD | 5 TB | $59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2690 2.90GHz | 6 核 / 16 GB | 500 GB HDD | 10 TB | $79/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2690 2.90GHz | 8 核 / 32 GB | 750 GB HDD | 10 TB | $99/月 | [ 选择此方案](https://bit.ly/RacKnerd) |

### Dedicated Server

| 机型 | 内存 | 存储 | 流量 / IPv4 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- |
| Intel Xeon E3-1230 v2 | 16 GB | 480 GB SSD | 35 TB / 5 个 | $139/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Intel Xeon E3-1270 v3 | 32 GB | 2×1 TB SSD | 35 TB / 5 个 | $169/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2650 v2 | 64 GB | 1 TB SSD | 100 TB / 5 个 | $199/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2650 v2 | 128 GB | 1 TB SSD + 3 TB HDD | 50 TB / 5 个 | $245/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2650 v2 虚拟化节点 | 256 GB | 4×2 TB SSD | 100 TB / 29 个 | $349/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2680 v4 | 256 GB | 4×2 TB SSD | 100 TB / 61 个 | $399/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Dual Xeon E5-2640 v2（存储服务器） | 64 GB | 256 GB SSD + 10×16 TB HDD | 200 TB / 5 个 | $479/月 | [ 选择此方案](https://bit.ly/RacKnerd) |

### Shared Hosting 与 Reseller Hosting

| 套餐 | 空间 / 流量 | 价格 | 购买 |
| --- | --- | --- | --- |
| Shared 30 GB | 30 GB / 2 TB | $5.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Shared 100 GB | 100 GB / 3 TB | $9.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Shared 100 GB Pro | 100 GB / 5 TB | $15.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Reseller 40 GB | 40 GB / 2 TB / 50 个 cPanel | $14.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |
| Reseller 100 GB | 100 GB / 不限 / 100 个 cPanel | $22.59/月 | [ 选择此方案](https://bit.ly/RacKnerd) |

## 月付 1 GB 和年付 1 GB Special 的配置不一样

这两者的差价常被拿来对比，但配置本身就不是一回事，不只是一年付一次还是每月付一次的区别。

|  | 月付 1 GB | 年付 1 GB Special |
| --- | --- | --- |
| vCPU | 2 vCore | 1 vCore |
| 内存 | 1 GB | 1 GB |
| 存储 | 50 GB RAID-10 | 20 GB PURE SSD |
| 月流量 | 1 TB | 3 TB |
| 价格 | $17.99/月 | $21.99/年 |

按年算，月付 1 GB 一年是 $215.88，年付特价 $21.99，差 $193.89。省下的钱是真的，少掉的那个 vCore 和 30 GB 存储也是真的。跑轻量站点、代理、小工具，1 vCore 够用。要跑编译、数据库或多个容器，2 vCore 和更大的盘更踏实。

选的时候按"我需要几个 vCore、多少 SSD"来定，别只看总价。

## 买之前能做的三件事

退款难争取，把功夫花在下单前更有效。

**用 Looking Glass 测延迟。** 官网给每个机房都提供了 looking glass，选你关注的城市跑 ping 和下载测试，能提前避掉"机房选错"这种最难退的理由。

**下载测试文件。** 每个机房有公开的 test IP 和 100 MB / 1 GB 测试文件，能跑满你本地带宽，说明线路没问题。

**先月付跑一两个计费周期。** 月付多花的钱相当于试错保险，确认稳定后再转年付。

还有一条容易被忽略：RackNerd 的 KVM VPS 不允许嵌套虚拟化，在 VPS 里再开虚拟机、跑 hypervisor 需要书面批准。Docker、LXC/LXD、Kubernetes 这类容器不受限制。如果你买 VPS 的目的是在里面开小鸡，下单前就得换方案，别等开通了再申请退款。

## 支付方式和争议机制

RackNerd 支持信用卡（AMEX、VISA、MasterCard、Discover）、PayPal、比特币和支付宝。

信用卡和 PayPal 有外部争议通道，但 chargeback 会触发 $125–$250 行政费并可能导致账号暂停，只适合金额远大于罚款的纠纷。比特币和支付宝没有外部争议机制，只能走平台内工单。

客服方面，官方博客写明提供 24×7 工单支持，平均响应时间在 10 分钟以内。工单是这个品牌唯一的支持渠道，没有在线客服，遇到问题别指望即时聊天窗口。

## 最后：按你的情况选

- 只是想试试 RackNerd 稳不稳：月付 1 GB，跑一两周再决定
- 机房测过、配置确认够用：年付特价，1 GB Special 或 2 GB Special
- 第一次接触 VPS、不熟悉命令行：Shared Hosting 30 GB 起步，cPanel 可视化操作
- 已经买错年付套餐：别 chargeback，开 Billing 工单，提出换机房或转余额

下单前再确认三件事：目标机房测过没有、备份方案想好没有、取消时选的是 Immediate 还是 End of Billing Period。第一件事决定你会不会想退，后两件事决定真要退的时候损失多大。

👉 [前往 RackNerd 查看全部套餐并下单](https://bit.ly/RacKnerd)
