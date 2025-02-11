---
title: "备案基础知识"
description: Test description
weight: 2
---



### 什么情况需要做 ICP 备案？

备案是中国大陆的一项法规。只要在互联网能访问并且使用大陆公网 IP 地址的域名，都需要在服务器提供商处提交备案申请。

如果您使用的是中国大陆地区以外的服务器（包括中国港澳台及其他国家、地区），则无需备案。

#### 不备案的影响

对于使用大陆公网 IP 地址提供互联网访问的域名，需要在取得备案号后才能开通网站，否则会被阻断。

未备案域名的网站在申请备案期间需要关闭且停止解析服务，否则备案将无法通过管局审核; 已经通过备案的网站可以在域名备案转接入期间正常开放。如果网站在未备案状态下上线访问，则网站一经查实将被隔离域名使用且上级运营商将会封停 IP 地址。

如果您没有提交过备案，需要将域名解析至青云购买的中国大陆服务器，请登录青云备案管理系统，提交网站和域名资料，办理 ICP 备案。


![](../../_images/block.png)

### 我的域名在其它接入商那里备案过，使用青云需要重新备案吗？

如果你的顶级域名（例如 abc.com）在其它接入商备案过，然后搬迁到青云，域名要进行新增接入；如果你的顶级域名不迁移到青云，而只是二级域名（例如 m.abc.com）放到青云，现在按管局要求也需要进行备案接入，同一个网站可以同时有多个接入商，不互斥。 新增接入备案不影响您的网站正常运行。

### 备案需要多少时间完成？

时间跟各省的通管局审核有关，一般在5-20个工作日左右完成，备案通过或拒绝会有短信及邮件通知。 建议您统筹安排 ICP 备案及服务器部署。

### 国外域名需要备案吗？

由于各省管局规则不同所以备案情况也不同，目前北京地区不允许国外域名的备案，其它具体情况可与青云的备案专员确认。

### 可以备案论坛（BBS）、博客（Blog）吗？

BBS、Blog 划归为交互式网站，目前个人已经无法备案了。企业可以备案，但需要相应的前置审批，具体政策法规请查询工信部备案管理网站。

### 带有备案信息的公网 IP 在欠费后，系统会如何处理？

通过青云备案信息验证的公网 IP 请尽快进行 ICP 备案信息的绑定，通过后会在欠费暂停服务后继续保留3天，并发出欠费提醒的邮件；对于不需要备案或没有绑定 ICP 备案信息的公网 IP，一旦欠费就会被系统释放回资源池。

### 如何进行备案信息的查询？

登录工信部 ICP/IP 地址域名信息备案管理系统网站（https://beian.miit.gov.cn/），在搜索栏中输入单位名称、域名或主体备案号即可查询备案信息。

### 个人备案有什么限制吗？

个人名义备案：不含有企业、单位等非个人网站的信息。

### 为什么80端口被禁用？

根据上级网管要求，对于一些对备案要求较为严格的区域，例如北京2区（PEK2），用户需要完成备案才能使用80端口提供服务，在完成备案之前，80端口将被禁用。 在完成备案流程之后，用户需要将申请到的备案号填入公网 IP 对应的 “ICP 备案” 信息字段中（具体操作在公网 IP 的右键菜单 “设置 ICP 备案信息” 中）， 待管理员审核通过之后，才能正常使用80端口的服务。

### 一个青云账号最多可以备案几个主体？

最多可备案 5 个主体。

### 二级域名是否需要备案

请根据一级域名是否完成备案，判断二级域名是否需要备案。具体如下：

#### 一级域名有备案号

- 如果一级域名与二级域名为同一接入商，一级域名备案成功后使用二级域名无需备案（政府组成部门的二级域名需要备案）。

- 如果一级域名与二级域名为不同接入商，一级域名备案成功后，还需在接入商处进行新增接入备案，并将所接入二级域名填写在备案信息备注中。

  示例：

  一级域名.com在 A 接入商备案，二级域名***.***.com在青云接入（域名解析到青云 IP），则.com也需要在青云申请新增接入备案。

- 政府机构、事业单位后缀为.gov.cn的二级域名需要备案。

#### 一级域名没有备案号

需要将一级域名提交[首次备案](	../../manual/first_filing/)。待备案成功后，一级或二级域名便可正常解析使用青云IP。

### 中文域名是否支持备案

青云备案平台支持中文域名备案。所支持的中文域名可参见[中国互联网域名体系](http://domain.miit.gov.cn)。

### 没有购买云产品能否备案

不可以。

只有购买了青云产品资源（例如云服务器、公网 IP），青云才是您的接入商，才可以代操作申请网站备案。

### 只有域名能否备案

域名无法单独备案。

### 服务器在青云，域名不在青云，是否可以备案

可以。

如果您有业务部署在青云服务器（含弹性公网 IP），即可通过青云备案，与域名注册服务商没有关系。

示例：

如果您的主体和域名均为第一次备案，即在[工信部](https://beian.miit.gov.cn/)无任何备案信息。请参见[首次备案](	../../manual/first_filing/)。

如果您的主体和域名已在其他接入商备案过，现需将顶级域名或其子域名解析在青云，应申请新增接入备案。请参见[新增接入](../../manual/add_access/)。

> 说明：
> 1. 可以用于青云备案的服务器，请参见[准备可备案服务器](../../prepare/prepare_vm/)。
> 2. 域名实名认证信息（包括“域名持有者”、“证件类型”、“证件号码”）需与备案主体信息需保持一致。

#### 我应该在哪里提交 ICP 备案

您需要在服务器提供商处提交 ICP 备案，与域名服务商（域名购买地点）无关。

示例：

问：我在某域名注册服务商（非青云）处购买了域名，但在青云购买了绑定公网IP的云服务器。我需要在哪里提交 ICP 备案？

答：由于您的服务器是在青云购买的，因此需要在青云提交 ICP 备案申请。

### 分公司或子公司网站是否可以备案到总公司备案中

不可以。

应使用分公司或子公司名义独立进行备案。

### 已备案网站接入青云还要备案吗

如果您的网站之前在别的接入商办理过备案，现网站需转接入到青云。因接入商有变更，所以需要申请[新增接入](../../manual/add_access/)备案。
> 说明：  
> 新增接入的网站，如原已备案信息资源有效，网站可正常使用。接入备案成功后，该网站域名可解析至青云IP。

### 备案期间网站可以访问吗

针对不同的备案类型，网站访问情况有所不同。

- 新增备案（首次备案）、新增网站：

  没有备案的 IP 和域名不允许上线访问。

- 变更备案：

  变更备案期间，已备案的域名访问不受影响，同时需确保网站内容与备案信息相符。网站下新添加的域名备案成功后才可上线访问。

- 新增接入：

  如原备案的IP仍然有效，则可继续访问；接入备案成功后，即可解析到青云IP。

