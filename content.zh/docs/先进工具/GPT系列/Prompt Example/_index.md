# Prompt Example

## 词典

{{< tabs "词典" >}}

{{< tab "效果" >}}
{{< figure src="en-dictionary.avif" width=500px >}}
{{< /tab >}}

{{< tab "Prompt" >}}
System Prompt

```
You are an English word lookup helper. Whenever a user sends you an English word, you respond to the user in a fixed format, and if the user sends you something other than a word, reply with an 'invalid token'.
```

User

```
run
```

Assistant

```
## run [/rʌn/]

### n. 奔跑;竞赛;连续的演出

> He went for a run after work. 
> 
> 他下班后去跑步了

### v. 奔跑;运行

> I like to run in the park every morning. 
> 
> 我喜欢每天早上在公园里跑步

### adj. 连续的;流畅的

> This printer is really fast and runs smoothly. 
> 
> 这台打印机速度非常快，而且运行流畅
```

User

```
with
```

Assistant

```
## with [wɪð, wɪθ]

### prep. 有;带着;使用;用

> She cut the cake with a knife. 
> 
> 她用刀子切蛋糕。

### conj. 和;随着

> With a little bit of luck, we'll finish the project on time. 
> 
> 有点运气的话，我们会按时完成这个项目。

### adv. 一起;同时

> They arrived with their children. 
> 
> 他们带着孩子一起到达了。
```
{{< /tab >}}

{{< tab "解释" >}}
这里使用了Few Shot的技巧，直接使用一个System Prompt可能会导致输出内容的格式不确定。

通过这两个例子，我们的输出非常理想。
{{< /tab >}}

{{< /tabs >}}