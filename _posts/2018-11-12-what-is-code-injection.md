---
layout: post
title:  "What is Code Injection?"
author: jhwimalasiri
categories: [ security, code injection ]
image: assets/images/code-injection.png
description: "My review of Inception movie. Acting, plot and something else in this short description."
featured: true
hidden: true
---

You may have heard the term before and some of you might have a basic understanding that code injection effects security threats anyhow first we’ll find out what code injection really is.

Code Injection is introducing or injecting code into a program which will alter the behavior of the program. Injection can result in data loss, installing malware, authentication control or even end up complete host takeover. Code injection vulnerabilities are prone to applications that depend on user input for execution.

Below is an illustration of a few types of code injection,

![Types of Code Injection](assets/images/code-injection.png)

**SQL injection:** Inject commands that can read or modify database

**HTML script injection:** Also known as Cross-site scripting, where an attacker inputs malicious code into a web script

**Dynamic evaluation vulnerabilities:** When an attacker can control an input that is fed into a function
Object injection: Since PHP allows object serialization, attackers could pass ad-hoc serialized strings to a vulnerable unserialize() call, resulting in an arbitrary PHP object(s) injection into the application scope

**Remote file injection:** An attacker can cause the web application to include a remote file by exploiting a web application that dynamically includes external files or scripts

**Format Specifier Injection:** The Format String exploit occurs when the submitted data of an input string is evaluated as a command by the application. Then the attacker can execute the code or read the stack

**Shell injection:** Also known as Command injection, exploits applications which are used to execute commands for the operating system

Code injection attacks can result in system hacking and cracking to gain information which are unfortunately very common. There are many ways to prevent code injection vulnerabilities such as performing proper input validation, using safe APIs, parameterization, input and output encoding etc.

So this is a basic understanding of what code injection is and in order to prevent these vulnerabilities we must have a sound understanding of how to prevent all these malicious attacks.

Hope this will give you a boost to find more about this and keep your applications safe!