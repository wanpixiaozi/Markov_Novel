# Markov_Novel
根据马尔科夫链和给定文本，生成新内容。

本py程序需要使用到的模块：

1）字典模块：将导入的文本变为字典。

得到的图：![pic](https://img9.doubanio.com/view/note/l/public/p71350435.webp)

2）统计模块：统计文本词频。

3）组合模块：当用户输入了某个字眼后，找出最有可能的第二个字；再根据第二个字，找出最有可能的第三个字……以此类推。有了第2步的统计，程序可以找出最有可能的搭配。

要结合上一张图来理解。

我选了其中一对：```‘利’：｛‘波’：2，‘多’：136，‘上’：1，‘站’：1｝```

假设我们传入的就是“利”字，程序会开始统计“利”后面接着的字的频次，136+2+1+1=140，那么```wordLen(wordict)```是```140```.

```ranindex```从```（1，140）```中取个随机值，比如是```70```.

然后用这个```70```逐一减去```value```（即文字后的数字）。

70-2= 68；

68 - 136 = -68

此时出现了负数，说明这是最大的可能性之一，程序会返回这个数（136）的键（“多”这个字）。

所以在这里，如果你输入了“利”，后面接着的会是“多”字。

还可以调整文章长度和输入的第一个字。

输入第一个字后，才会出现内容：

![PIC](https://img3.doubanio.com/view/note/l/public/p71351541.webp)
