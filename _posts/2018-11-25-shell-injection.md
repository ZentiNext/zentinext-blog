---
layout: post
title:  "Shell Injection"
author: jhwimalasiri
categories: [ Tech ]
tags: [ code injection ]
image: assets/images/shell-injection-cover.png
description: "Shell Injection"
featured: false
hidden: false
---

It’s time to learn about another type of Code Injection which is **Shell Injection!**

Shell Injection also known as Command Injection is an attack which allows an attacker to execute commands on the server side via malicious user inputs. These attacks can occur when a software application takes unsafe user input and execute corresponding commands directly to give output.

So let’s take a simple example where an application shows the file content as output, based on the file name taken as its user input,

    <?php
    print(“Please specify the name of the file”);
    $file=$_GET[‘filename’];
    system(“cat $file”);
    ?>

Here if an attacker gives an input `‘ account.txt ’`, corresponding file’s content will be shown.

Also an attacker can exploit this even more by giving input `‘ account.txt; rm -rf /; ’` which will delete the files in the root directory.

So as you can see, this is a serious vulnerability which needs to be taken into consideration as developers.

### Now lets see how we can prevent it,

1. Verify user input
2. Never execute direct commands taken as user inputs
3. Replace or ban arguments with characters like ; , &, | .etc
4. Limit the length of the user input data

So that’s all for shell injection, hope it will be helpful to make your application less vulnerable.

