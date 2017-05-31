---
title: "Contributing to Falcon Ecosystem"
linktitle: "Contribtuing to Falcon Ecosystem"
author: "Ritesh Kadmawala"
date: 2017-06-01
weight: 10

description: "Over the last month i have been working on open sourcing some of the stuff that we built while using `falcon` web framework for one of our projects. We have open sourced three falcon libraries along with proper documentations and tests"
---

At Loanzen, most of our backend is written in python. For most of our services, until now we have been using `Flask` as our 
web framework of choice. However, recently, for one of our new services that we needed, I decided to give `Falcon` a try. For this particular service, performance was of utmost importance. Besides being a reasonably small service, we thought it would be good project to try out Falcon . 

Falcon is quite small in footprint as compared to its illustrious cousins like `Flask` and `Django`. However it also suffers from a limited support of extensions/plugins/middlewares in comparison. We were quite surprised to find no proper libraries to handle authentication or a middleware to force ssl in particular. Despite these shortcoming, i was really smitten by the simplicity of falcon. It had absolutely no magic going on and it was extremely simple to understand how does a request-response cylce works in falcon. So we decided to stick with Falcon for this project and built the authentication middleware and SSL middleware from scratch without using any library.

Last month we started an initiative to actively promote `Open Source` at Loanzen. I discussed at length some of those initiative [here](http://engineering.loanzen.in/post/oss/). As part of that initiative, we open source three falcon libraries that was missing from the falcon ecosytem, and was needed by our Falcon powered web service.

+ [Falcon-SSlify](https://falcon-sslify.readthedocs.io/en/latest/) A middleware that forces SSL and enables HSTS

+ [Falcon-Auth](http://falcon-auth.readthedocs.io/) A falcon middleware + authentication backends that adds authentication layer to you falcon powered app/api service.

+ [Falcon-Resource-Factory](https://github.com/loanzen/falcon-resource-factory) A simple falcon library that allows defining a single resource class to handle requests for a single item as well as multiple items

We have tried our best to add proper documentation to these libraries, and support them with good test coverage. We have been using these packages internally for few months now without any issue. If you are using falcon web framework, i recommend you to check them out and see if they might be useful for your project.