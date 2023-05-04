---
layout: post
title: token说明
permalink: /token
---

OpenAI token 的计算包含两部分。

`输入`给 ChatGPT 模型的`token`数和 ChatGPT 模型`生成`文本的 `token` 数。

例如，你提问耗费了 200 token，GPT 根据你的输入，生成文本（也就是回答）了 200 token，那么一共消费的 token 数就是 400。

因此，如何提问，非常重要！

#### 如何计算文本的token数

如何计算文本的token数？[https://platform.openai.com/tokenizer](https://platform.openai.com/tokenizer)