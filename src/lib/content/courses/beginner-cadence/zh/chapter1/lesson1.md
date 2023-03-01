---
title: 学习区块链概念
lesson: 1
language: zh
excerpt: basic blockchain concepts
---

# 第一节-第一天-学习区块链概念

你好！没错，就是我。你最喜欢的开发者，Jacob。您当前正在浏览整个课程的第一天。让我们一起开始这段旅程。

让我们从复习看似复杂的术语开始我们的第一天，在接下来的旅程中您需要了解这些术语。

## 区块链到底是什么？

![drawing](/courses/beginner-cadence/blockchain.png)

如果您已经了解区块链是什么，或者您根本不在乎，您可以跳过本节。

在学习区块链时，你可能会发现一些复杂的文章。很容易完全迷失在其中，想要放弃。所以，我将以一种非常简单的方式解释区块链，可能有一些不准确/遗漏的信息，但旨在帮助您入门。具体来说，我将从编写智能合约或做一些去中心化应用的角度来帮助您理解区块链（这两种方式我们都会！）

一句话：区块链是一个开放的、分散的、共享的数据库，任何人都可以公开存储东西。

Okay，这是什么意思呢？

1. **开放的**: 任何人都能与区块链交互，这没有限制。
2. **去中心化**: 没有人拥有它。 没有中心化的权威来规定东西。
3. **数据库**: 你能够在上边存储信息。
4. **公开的**: 任何人都能够浏览上边的数据

根据这些特性，我们可以随心所欲地与区块链进行交互。很多时候，我们可能想要设置“规则手册”来确定人们如何与区块链的特定部分进行交互，以便它具有一些功能——特别是我们将要定义的应用程序。这是通过智能合约完成的。

要注意现在有许多不同的区块链。例如，以太坊可能是最受欢迎的区块链。在本课程中，我们将学习精彩的 Flow 区块链，因为那是我的专长！

## 智能合约？听起来很酷

![drawing](/courses/beginner-cadence/smart%20contract.png)

是的，智能合约非常酷。智能合约是开发人员制作的程序或“规则手册”。开发人员创建它们是因为它允许我们指定一些用户可以与它交互的功能。例如，如果我想制作一个允许用户将他们最喜欢的水果存储在区块链上的应用程序，我需要制作一个智能合约：

1. 有一个所有人都能调用的函数
2. 传入参数（这个人最喜欢的水果）
3. 用一些数据储存那个参数
4. 将更新的数据发送到区块链（自动触发）

如果我创建了这个智能合约并将其“部署”到区块链上（部署意味着我们将合约放在区块链上，以便人们可以与之交互），那么任何人都可以将他们最喜欢的水果放在区块链上，它会永远存在！除非我们也有删除该数据的函数。

那么，我们为什么要使用智能合约？

1. **速度，效率和确定性**: 智能合约速度很快，而且没有中间人。也不需要文件审批。如果我想通过使用允许我调用某些函数的智能合约来更新区块链上的数据，不需要得到我父母或银行的批准就可以做到。
2. **可信和透明**: 如果我们这样做，区块链以及智能合约将非常安全。几乎不可能破解或改变区块链的状态，虽然这是由于很多种原因，但主要是因为智能合约。如果智能合约不允许我做某事，我根本做不到。没有办法解决它。

有哪些缺点呢？

1. **很难做对**: 虽然只能合约非常酷，但它不是智能的。它们需要开发人员方面的高级专业知识，确保它们没有安全问题，它们是低级的，并且可以按照我们的意愿去做。稍后我们将了解所有这些。
2. **如果开发人员做坏，它们可能是恶意的**: 如果开发人员想要制作一个智能合约来窃取您的资金，然后诱使您调用执行此操作的函数，那么您的资金将被窃取。在区块链的世界中，您必须确保与安全的智能合约进行交互。
3. **无法撤销**: 你无法撤销一些事，除非你有一个函数允许你这样做。

## 交易和脚本

![drawing](/courses/beginner-cadence/transaction.jpeg)

_“好的，所以我们有一个智能合约。我该如何与之交互？你一直说调用一个函数，但这意味着什么！？”_

**交易是一种优美的、付费的函数调用。**这几乎是我能解释的最简单的了。重要的是要知道，交易会改变区块链上的数据，而且通常是我们可以改变区块链上数据的唯一方式。不同区块链，交易可能会花费不同的金额。在以太坊上，要将你最喜欢的水果存储在区块链上，它的成本可能接近 100 美元。在 Flow 上，它只有几美分。

另一方面，脚本用于查看区块链上的数据，他们不会更改它。脚本不用花钱。

这是正常的工作流程：

1. 开发者在区块链上部署智能合约
2. 用户执行一个“交易”，该“交易”会收取一些款项（支付 gas 费、执行所需的费用等），该“交易”会调用智能合约中的某些函数
3. **智能合约更改它的数据**

## “主网”和“测试网”

![drawing](/courses/beginner-cadence/tvm.PNG)

您可能听说过这些术语，但它们的实际含义是什么？

**测试网**是开发人员在将其应用程序发布之前对其进行测试的环境。这是一个完美的空间，可以在将应用程序实际发布使用之前找出问题。以下是一些附加说明：

- 一切都是虚假的
- 不涉及实际资金
- 交易花费的是虚假的钱
- 开发人员在向公众发布之前测试其智能合约和应用程序的好方法
- 如果某些坏事发生，没人在意

**主网**是一个一切都是真实的环境。当您向公众发布您的应用程序时，您将其放在主网上。在主网上，一切都是实时的，所以一切都需要真实的钱，存在风险，你必须确保一切正常。以下是一些附加说明：

- 一切都是真实的
- 涉及到钱
- 交易花费真实的钱
- 当您的应用程序完全准备好后，您将其放在主网上供用户交互。
- 如果发生了不好的事情，那真的很糟糕。

## 去中心化应用（DApps）

![drawing](/courses/beginner-cadence/dapps.jpeg)

这听起来很复杂。没有！它不复杂。 DApps 实际上只是普通的应用程序（Javascript、Python 等），它们也涉及智能合约。

之后，我们将构建这些 DApps

## 为什么要关心这些？

因为这就是这门课程的全部内容！在本课程中，我们将制作自己的智能合约，特别是在 Flow 区块链上。此外，我们将制作使用这些智能合约的去中心化应用程序。

## 结论

Jacob 是最好的。不，不。这不是结论。结论是，尽管所有这些东西听起来都非常复杂，但实际上并非如此。如果你仍然不明白这些，那完全没关系。有时最好实际操作示例，这些会更容易理解。我们将在接下来的几天里这样做。

## 任务

您可以用您自己的语言自由回答这些问题。

1. 用你自己的话解释什么是区块链。你可以阅读这篇文章来帮助你：https://www.investopedia.com/terms/b/blockchain.asp
2. 解释什么是智能合约，你可以阅读这篇文章: https://www.ibm.com/topics/smart-contracts
3. 解释脚本和交易的区别