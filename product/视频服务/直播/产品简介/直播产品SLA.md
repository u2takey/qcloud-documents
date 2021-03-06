腾讯云直播服务等级协议（Service Level Agreement，简称 “SLA”）规定了腾讯云面向客户提供的视频直播服务（LVB）服务的性能指标及赔偿方案。
### 名词定义
#### 1. 服务周期
一个服务周期为一个自然月，不满一个月不计算为一个服务周期。
#### 2. 视频播放失败
在服务周期内，终端用户没有获取到视频信息，导致用户无法观看视频。
以下情况导致用户无法观看视频不算作视频播放失败：
（1）由于视频内容违规或其他原因导致域名被封或者视频流被禁播；
（2）推流端异常无法推流导致视频播放失败；
（3）播放端异常无法播放导致视频播放失败；
（4）腾讯云设备以外的机房、网络等设备导致的视频播放失败；
（5）不可抗力以及其他非腾讯云因素引起的视频播放失败（例如自然灾害、战争等）；
（6）由于客户开启防盗链以及鉴权功能导致的视频播放失败；
（7）腾讯云预先通知客户的合理升级、变更导致的视频播放失败。
#### 3. 视频播放成功率
![](https://main.qcloudimg.com/raw/8509cffc7c04c310a94ded087eca2ea0.png)
#### 4. 视频加载时间
视频加载时间是指在非视频播放失败情况下，观众端从开始连接 CDN 分发的视频请求 URL 到开始播放视频第一帧的总耗时。
#### 5. 卡顿请求
CDN分发服务器本地流逝时间与视频流逝时间的差值定义，差值大于 0 则为卡顿。
（视频流逝时间可从传递的视频内容中获取到）
一起播放请求中，服务器记录时间流逝了 5 分钟，但是只传递了 4 分 59 秒的视频数据，则本次请求为一次卡顿请求。
#### 6. 卡顿率
腾讯云直播产品卡顿比的指标统计周期为 5 分钟。5 分钟内，视频播放的卡顿请求数和视频播放总请求数之间的比率。
![](https://main.qcloudimg.com/raw/9f094bd277cffee9eccec18775cf9790.png)

### 性能指标
#### 1. 视频加载成功率指标
一个服务周期内，视频加载成功率平均值不得低于 99.60%（包含99.60%）即：
![](https://main.qcloudimg.com/raw/243b475b0dc62a282423b34b3d071e99.png)
#### 2. 视频加载时间指标
单次视频加载时间不高于 850ms（包含 850ms）；
#### 3. 卡比率指标
视频卡顿比率不高于 4.00%（包含4.00%）
![](https://main.qcloudimg.com/raw/1a84aa725e2a81e86c142798eba7c8cf.png)

### 赔偿方案
服务赔偿指因腾讯云设备故障、设计缺陷或操作不当导致客户所购买的腾讯云视频直播服务未达到本服务等级协议承诺的性能指标，腾讯云将对客户进行赔偿。赔偿规则如下：

<table >
  <tr>
    <th colspan="2">性能指标</th>
    <th></th>
  </tr>
  <tr>
    <td rowspan="2">视频播放成功率</td>
    <td>视频播放成功率平均值在 95.0% ~ 99.6% 之间</td>
    <td>扣除当月视频总费用*（99.60%-实际播放成功率）</td>
  </tr>
  <tr>
    <td>播放成功率低于 95.0%（含 95.0%）</td>
    <td>扣除当月视频直播总费用</td>
  </tr>
  <tr>
    <td rowspan="2">视频加载时间</td>
    <td>加载时间 850ms-2s 之间</td>
    <td>扣除当月视频直播总费用的 1/60</td>
  </tr>
  <tr>
    <td>加载时间高于 2s（含 2s）</td>
    <td>扣除当月视频直播总费用的 1/30</td>
  </tr>
  <tr>
    <td rowspan="2">卡顿率</td>
    <td>卡比率 4%-6% 之间</td>
    <td>扣除当月视频直播总费用的 1/60</td>
  </tr>
  <tr>
    <td>卡顿比率高于 6%（含 6%）</td>
    <td>扣除当月视频直播总费用的 1/30</td>
  </tr>
</table>
