---
title: "子账号配额管理"
description: verify
weight: 15
draft: false
---

主账户可以创建多个子账户(Sub User)，每个子账户可自主管理和部署名下的资源。子账户之间的资源是相互隔离的，同时所有子账户会共享主账户的配额。默认子账户共享主账户的余额，主账户可以将子账户设为独立计费，使其有独立的余额，可自行充值，名下资源消费也从其余额中扣除。

## 配置入口

点击控制台顶部导航 **用户头像** > **子账户**。

![](../../_images/user-verify-entry.png)

## 开启独立配额

进入欲分配独立配额的子账户详情页。

进入详情页后，点击 **配额** 页签。当子账户还没有独立配额时，您会看到如下页面：

![子账户未开启独立配额](../../_images/indep-quota-disabled.png)

如您想给这个子账户分配独立配额，请点击 **设置独立配额** 按钮。 点击按钮之后，页面里出现一个分配表单，您可以在这里填写分配资源的数量。

![填写资源数量](../../_images/indep-quota-grant.png)

> **说明**
>
> - 分配数量的上限，必须小于等于主账户可用资源数量。
> - 有一些资源是有依赖性的。比如：想要创建一台主机，需要主机、CPU、内存、硬盘这些资源。当您填写完资源数量后，点击表单底部的 **修改独立配额** 按钮，就可以让此子账户拥有独立配额了。
> - 分配给子账户的资源配额，会立即从主账户的可用资源里扣除响应的数量。

## 修改独立配额

云平台支持随时调整子账户的独立配额，点击进入欲修改独立配额的子账户详情页。

进入详情页后，点击 **配额** 页签。页面将展示分配表单，您可以在这里修改资源的数量。

> **说明**
>
> <li>如果您想分配更多的资源给子账户，请先确认主账户有足够的可用资源。
>
> <li>如果修改后的资源数量小于子账户已经使用的资源数量，不会对您已用的资源有任何影响，但是该子账户不能再创建更多的资源。同时，这部分超过配额的资源用量，会计入主账户的已用资源用量里。

完成修改后，请点击表单底部的 **修改独立配额** 按钮。

## 回收独立配额

云平台也支持回收子账户的独立配额。独立配额被回收后，不会影响您已经创建的资源。点击进入欲回收独立配额的子账户详情页。

进入详情页后，点击 **配额** 页签。您会看到分配表单。滚动页面到表单底部，点击 **回收独立配额** 按钮，点击后子帐户回到共享主账户配额的状态。

