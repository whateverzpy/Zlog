+++
weight = {{ mul (sub (readDir "content/post" | len) 1) -1}}
image = ''
categories = ['']
date = '{{ .Date }}'
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
description = ''
tags = ['']
lastmod = '{{ .Date }}'

<!-- 记得删除草稿配置，否则会被忽略 -->
draft = true
+++
