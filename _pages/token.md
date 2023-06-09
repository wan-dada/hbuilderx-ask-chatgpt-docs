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

#### token是什么？

在自然语言处理(NLP)中，token是指一组相关的字符序列，例如一个单词或一个标点符号。

将文本分解为token是NLP的一项基本任务，因为它是许多其他任务的先决条件，例如词性标注、命名实体识别和机器翻译。

在文本处理中，token可以是一个词语、数字、标点符号、单个字母或任何可以成为文本分析的单个元素。

在分解文本时，通常会根据空格、标点符号和其他特定的分割符号来确定token的边界。

例如，在以下句子中，标点符号和空格用于分解成为不同的token：

> "我喜欢吃冰淇淋。"

在这个句子中，每个汉字和标点符号都可以切分开成一个token。

但是，一个字一个字去理解整句话的意思，可能反而会理解错误。

例如“冰淇淋”，就是一个完整的词，分开成“冰”“淇”“淋”三个字反而无法理解了。

类似的，NLP中，token还可以是比词更高级别的语言单位，例如短语或句子。

例如，对于短语token，“红色的苹果”可以被视为一个token，而不是单独的“红色”和“苹果”token。

因为存在不同的切分方式，所以“红色的苹果”，就需要切分成“红”“红色”“的”“苹果”“果”“红色的苹果”等多个token去理解。

在处理文本时，理解token的概念是非常重要的，因为它是许多文本分析任务的基础。NLP算法会使用token来构建文本的表示形式，理解自然语言，以便进行其他分析任务。

因此，对于NLP系统来说，选择正确的分词方法（tokenization）非常重要，它将直接影响到其他任务的准确性和效率。


#### ChatGPT API的价格

再回来看ChatGPT API的

> “$0.002 per 1k tokens”

在英语中“一个 token 通常对应大约 4 个字符”，而1个汉字大致是2~2.5个token。

1000 tokens大概是750单词。那也就是说，大概2美元可以问100万个token，相当于750000个单词。75万个单词只要不到15块钱人民币，相比人类作家，够便宜的了！

当然，虽然100万个token看起来很多。但其实，发送一段供API响应的文本可能就会花费不少token。

根据大家的经验，基本问清楚1个问题就要耗费100~200个token，算起来其实不少的，尤其在连续会话中，为了保持对话的连续性，必须每次都要回传历史消息，并且输入都要算 token 数算钱的，满打满算，按量付费其实也不便宜。


备注：以上部分回答，来源于: https://zhuanlan.zhihu.com/p/612954797