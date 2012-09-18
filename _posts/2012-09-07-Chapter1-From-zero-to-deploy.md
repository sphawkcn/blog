---
layout: post
title: 从零开始部署
tags: 翻译
comment: true
published: true
description: 
---

###Chapter 1

##From zero to deploy

Welcome to the Ruby on Rails Tutorial. The goal of this book is to be the best answer to the question, “If I want to learn web development with Ruby on Rails, where should I start?” By the time you finish the Ruby on Rails Tutorial, you will have all the skills you need to develop and deploy your own custom web applications with Rails. You will also be ready to benefit from the many more advanced books, blogs, and screencasts that are part of the thriving Rails educational ecosystem. Finally, since the Ruby on Rails Tutorial uses Rails 3, the knowledge you gain here represents the state of the art in web development. (The most up-to-date version of the Ruby on Rails Tutorial can be found on the book’s website at http://railstutorial.org/; if you are reading this book offline, be sure to check the online version of the Rails Tutorial book at http://railstutorial.org/book for the latest updates.)

###第一章

##从零开始部署

欢迎来到这个Ruby on Rails 教程。这本书将完美为您解答 “如果我想学习Ruby on Rails网络开发，我应该从哪里开始呢？” 这个问题。当您完成这个Ruby on Rails教程，您会拥有使用Rails开发和部署自己的web应用程序所必需的所有技能。您也将受益于其他高端书籍、博客和视频等一系列丰富多彩的Rails学习资源。最后，本Ruby on Rails 教程使用Rails 3.*版，您在这里获得的知识代表网络开发的最先进技术 (此书的最新版可参阅官网：[http://railstutorial.org/](http://railstutorial.org "Ruby on Rails Tutorial官网")。如果您正在离线阅读本书, 请确认您阅读的是本书的最新版本。)

Note that the goal of this book is not merely to teach Rails, but rather to teach web development with Rails, which means acquiring (or expanding) the skills needed to develop software for the World Wide Web. In addition to Ruby on Rails, this skillset includes HTML & CSS, databases, version control, testing, and deployment. To accomplish this goal, the Ruby on Rails Tutorial takes an integrated approach: you will learn Rails by example by building a substantial sample application from scratch. As Derek Sivers notes in the foreword, this book is structured as a linear narrative, designed to be read from start to finish. If you are used to skipping around in technical books, taking this linear approach might require some adjustment, but I suggest giving it a try. You can think of the Ruby on Rails Tutorial as a video game where you are the main character, and where you level up as a Rails developer in each chapter. (The exercises are the minibosses.)

请注意，这本书的目的不仅仅是教您Rails，而是教您如何使用Rails进行网络应用程序开发，这意味着您获得的是开发互联网应用程序的通用技术。除了 Ruby on Rails本身的技术之外，还包括Html与CSS、数据库、版本控制、测试以及部署技术。为了达成这个目标，本书采用一种整体式方法：您将按照我们的示例从零开始搭建一个功能完备的应用程序实例来学习Rails。正如Derek Sivers的笔记中的前言所说的那样，本书采用一种线性叙事的方式，设计为从头开始阅读，直到本书结束。如果您过去习惯于采用跳跃式的方式来阅读技术类书籍，采用线性方式阅读本书可能需要您勉强改变一下阅读习惯，但是我还是建议您这样试一试。您学习这个Ruby on Rails教程就像玩视频游戏一样，在这里，您就是主角，在这里您将通过每一章节的学习不断地升级为更高一级的Rails开发者（练习题就是每个关卡的守关Boss）。

In this first chapter, we’ll get started with Ruby on Rails by installing all the necessary software and by setting up our development environment (Section 1.2). We’ll then create our first Rails application, called (appropriately enough) first_app. The Rails Tutorial emphasizes good software development practices, so immediately after creating our fresh new Rails project we’ll put it under version control with Git (Section 1.3). And, believe it or not, in this chapter we’ll even put our first app on the wider web by deploying it to production (Section 1.4).

在第一章里，我们将从安装Ruby on Rails所需的必要软件以及设置开发环境开始（1.2节），然后，我们将创建我们的第一个难度适中的Rails程序，叫做first_app。本Rails教程注重完整的开发实践体验，所以，在创建完我们的第一个Rails程序后，我们将把他加入我们的git版本控制系统（1.3节）。并且，信不信由你，我们甚至会把我们创建的这个程序作为一个可以正式运行的成品部署到互联网中（1.4节）。

In Chapter 2, we’ll make a second project, whose purpose is to demonstrate the basic workings of a Rails application. To get up and running quickly, we’ll build this demo app (called demo_app) using scaffolding (Box 1.1) to generate code; since this code is both ugly and complex, Chapter 2 will focus on interacting with the demo app through its URIs (sometimes called URLs)1 using a web browser.

在第二章，我们将建立第二个项目来演示Rails应用程序的基本工作方式。为了快速建立并启动程序，我们将使用脚手架功能（scaffolding） (1.1版)来自动生成代码。因此，这些代码是丑陋而又复杂的，不过，我们的重点主要集中在使用浏览器通过URL地址来与我们的程序产生交互，不必在意代码。

The rest of the tutorial focuses on developing a single large sample application (called sample_app), writing all the code from scratch. We’ll develop the sample app using test-driven development (TDD), getting started in Chapter 3 by creating static pages and then adding a little dynamic content. We’ll take a quick detour in Chapter 4 to learn a little about the Ruby language underlying Rails. Then, in Chapter 5 through Chapter 9, we’ll complete the foundation for the sample application by making a site layout, a user data model, and a full registration and authentication system. Finally, in Chapter 10 and Chapter 11 we’ll add microblogging and social features to make a working example site.

教程剩下的部分将着重于从零开始，亲自编写代码，完成一个独立的大型范例程序（叫做sample_app）的开发。我们将使用“测试驱动开发（TDD）”方式来开发这个范例程序。在第三章，我们将从建立一个静态页面开始，然后添加一点动态内容。在第四章，我们将快速学习一些关于Rails需要用到的Ruby语法知识。然后，从第五到第九章，我们将通过建立网站布局、一个用户数据模型和一个完整的注册和认证系统来完成这个范例程序的基本架构。最后，在第十、十一章，我们将通过添加微博和社交功能来建立一个可工作的示例站点。

The final sample application will bear more than a passing resemblance to a certain popular social microblogging site—a site which, coincidentally, was also originally written in Rails. Though of necessity our efforts will focus on this specific sample application, the emphasis throughout the Rails Tutorial will be on general principles, so that you will have a solid foundation no matter what kinds of web applications you want to build.

最终的范例程序与曾经一个微博社交网站非常相似，巧合的是，这个网站曾经也是用Rails搭建的。尽管我们将我们的注意力集中在这个特定的范例程序中，但是，重要的是我们通过他学到的是通用的原则，所以，无论您将要搭建一个什么样的应用程序，你都会有一个坚实的基础。

####Box 1.1.Scaffolding: Quicker, easier, more seductive

From the beginning, Rails has benefited from a palpable sense of excitement, starting with the famous 15-minute weblog video by Rails creator David Heinemeier Hansson. That video and its successors are a great way to get a taste of Rails’ power, and I recommend watching them. But be warned: they accomplish their amazing fifteen-minute feat using a feature called scaffolding, which relies heavily on generated code, magically created by the Rails generate command.

When writing a Ruby on Rails tutorial, it is tempting to rely on the scaffolding approach—it’s quicker, easier, more seductive. But the complexity and sheer amount of code in the scaffolding can be utterly overwhelming to a beginning Rails developer; you may be able to use it, but you probably won’t understand it. Following the scaffolding approach risks turning you into a virtuoso script generator with little (and brittle) actual knowledge of Rails.

In the Ruby on Rails Tutorial, we’ll take the (nearly) polar opposite approach: although Chapter 2 will develop a small demo app using scaffolding, the core of the Rails Tutorial is the sample app, which we’ll start writing in Chapter 3. At each stage of developing the sample application, we will write small, bite-sized pieces of code—simple enough to understand, yet novel enough to be challenging. The cumulative effect will be a deeper, more flexible knowledge of Rails, giving you a good background for writing nearly any type of web application.
