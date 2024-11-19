---
title: "Introduction"
date: "`r Sys.Date()`"
weight: 2
chapter : false
pre: " <b> 1. </b> "
---

#### Introdution

**In this mini workshop**, we'll setup a simple architecture combine between Amazon SNS and Amazon Lambda. With purpose send SNS message to Messaging API (In this situation is telegram api).

#### Amazon Simple Notifications Service

**Amazon SNS** is a managed messaging service that lets you send notifications to lots of different devices and platforms. Amazon SNS was introduced in 2009 and has come a long way since then. It started out as a tool for mobile app notifications but has since expanded to support a wide range of use cases, including email alerts, SMS messages, and integration with other AWS services. With its ability to scale seamlessly and deliver messages to millions of recipients, Amazon SNS has become a cornerstone for building real-time communication and notification systems.

<div style="text-align: right">
<a href="https://docs.aws.amazon.com/sns/">More informations about Amazon Simple Notifications Service</a>
</div>

#### Amazon CloudWatch

Launched in 2008, AWS **Lambda**, a groundbreaking service introduced by Amazon Web Services in November 2014, revolutionized the way developers build and deploy applications. It pioneered the concept of serverless computing, allowing developers to run code in response to events without the need to manage underlying infrastructure.
 It allows developers to run code in response to events without provisioning or managing servers. This means you can build and deploy applications without worrying about the underlying infrastructure. Lambda automatically scales your application based on the workload, ensuring optimal performance and cost-efficiency. It supports various programming languages like Python, Java, Node.js.
<div style="text-align: right">
<a href="https://docs.aws.amazon.com/lambda/">More informations about Amazon Lambda</a>
</div>