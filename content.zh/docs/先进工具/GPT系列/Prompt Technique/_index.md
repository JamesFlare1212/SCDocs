# Prompt Technique

## Zero Shot

{{< tabs "Zero Shot" >}}

{{< tab "简介" >}}
关于这一部分，我建议阅读[Prompt Engineering Guide](https://www.promptingguide.ai/techniques/)的[Zero-Shot Prompting](https://www.promptingguide.ai/techniques/zeroshot)部分。

简而言之，就是不给例子，在提示词中直接给出指令，一般情况下效果也不错。
{{< /tab >}}

{{< tab "例子" >}}
Prompt：

> Classify the text into neutral, negative or positive.   
> Text: I think the vacation is okay.  
> Sentiment:

Output：

> Neutral
{{< /tab >}}

{{< /tabs >}}

## Few Shot

{{< tabs "Few Shot" >}}

{{< tab "简介" >}}
关于这一部分，我建议阅读[Prompt Engineering Guide](https://www.promptingguide.ai/techniques/)的[Few-Shot Prompting](https://www.promptingguide.ai/techniques/fewshot)部分。

原意是少量样本提示词。在提示词中提供例子，以引导模型获得更好的性能。
{{< /tab >}}

{{< tab "例子" >}}
Prompt：

> This is awesome! // Negative  
> This is bad! // Positive  
> Wow that movie was rad! // Positive  
> What a horrible show! //

Output：

> Negative
{{< /tab >}}

{{< /tabs >}}

## Chain-of-Thought (CoT)

{{< tabs "Chain-of-Thought (CoT)" >}}

{{< tab "简介" >}}
关于这一部分，我建议阅读[Prompt Engineering Guide](https://www.promptingguide.ai/techniques/)的[Chain-of-Thought Prompting](https://www.promptingguide.ai/techniques/cot)部分。

逻辑链是我们在大模型中发现的一项神奇性能。直接让模型回答结果大概率是错的，但是让模型给出思考过程在作答，那大概率是对的。
{{< /tab >}}

{{< tab "例子" >}}
{{< columns >}}
### Standard Prompting

#### Model Input:

> Q: Roger has 5 tennis balls. He buys 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls does he have now?
> 
> A: The answer is 11.
> 
> Q: The cafeteria had 23 apples. If they used 20 to make lunch and bought 6 more, how many apples do they have?

#### Model Output:

{{< hint danger >}}
The answer is 27.
{{< /hint >}}

<--->

### Chain-of-Thought (CoT) Prompting

#### Model Input:

> Q: Roger has 5 tennis balls. He buys 2 more cans of tennis balls. Each can has 3 tennis balls. How many tennis balls does he have now?
> 
> A: <mark style="background: #a5ec99">Roger started with 5 balls. 2 cans of 3 tennis balls each is 6 tennis balls. 5 + 6 = 11.</mark> The answer is 11.
> 
> Q: The cafeteria had 23 apples. If they used 20 to make lunch and bought 6 more, how many apples do they have?

#### Model Output:

{{< hint info >}}
A: <mark style="background: #a5ec99">The cafeteria had 23 apples originally. They used 20 to make lunch. So they had 23 - 20 = 3. They bought 6 more apples, so they have 3 + 6 = 9.</mark> The answer is 9.
{{< /hint >}}
{{< /columns >}}

Source: [Wei et al. (2022)](https://arxiv.org/abs/2201.11903)
{{< /tab >}}

{{< /tabs >}}