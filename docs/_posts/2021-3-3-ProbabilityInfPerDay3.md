---
title: 確率情報理論3日目
tags: 
 - 確率情報理論
 - TeX
---

春休みに１日１問、確率情報理論を解く会に使った問題をのせています。3月3日の問題です。  
[問題PDF](https://marbou090.github.io/MyBlog/folder/sec03.pdf)  
[解答PDF](https://marbou090.github.io/MyBlog/folder/ans03.pdf)  
問題出典：東京図書発行 藤田岳彦著「弱点克服　大学生の確率・統計」  

以下は解答PDFと同じ内容です。


## 本日の問題解答
１〜５の数字が書かれたカードがある。それぞれのカードを引く確率が、書かれた数字に比例する場合を考える。$$(\Omega=\{ 1,2,3,4,5\})$$

(1) 確率関数$$P(X=k)$$を求めよ。
  \begin{equation}
      1+2+3+4+5=15
  \end{equation} 
  確率は書かれた数字に比例することから、
  \begin{equation}
    P(X=k)=\frac{k}{15}
  \end{equation}
(2) $$E[X]$$を求めよ。
  \begin{equation}
    \begin{split}
      E[X] &= {1}\times \frac{1}{15}+{2}\times \frac{2}{15}+{3}\times \frac{3}{15}+{4}\times \frac{4}{15}+{5}\times \frac{5}{15} \\\\\\
      &=\frac{55}{15}
    \end{split}
  \end{equation} 
(3) 確率変数$$X(\omega)=\omega$$の分布関数$$F(X)$$を求めて図示せよ。（図は省略）  
 $$
  \begin{equation}
    F(X)= \begin{cases}
      {0~~~X<1}\\\\\\
      {\dfrac{1}{15}~~~1\le X<2}\\\\\\
      {\dfrac{3}{15}~~~2\le X<3}\\\\\\
      {\dfrac{6}{15}~~~3\le X<4}\\\\\\
      {\dfrac{10}{15}~~~4\le X<5}\\\\\\
      {\dfrac{15}{15}~~~5\le X}
    \end{cases}
  \end{equation} 
  $$



## おかわり問題解答
裏と表が描かれてるコインがある。表の出る事象を１、裏の出る事象を０とする(確率変数$$Y= \{ 0,1 \}$$)。このとき、上の問題の確率変数$$X$$との同時確率を考えていく。

(1) $$X$$と$$Y$$の同時確率を求めよ。
  \begin{equation}
    \begin{split}
      &P(X=1,Y=0)=P(X=1,Y=1)=\frac{1}{30}\\\\\\
      &P(X=2,Y=0)=P(X=2,Y=1)=\frac{2}{30}\\\\\\
      &P(X=3,Y=0)=P(X=3,Y=1)=\frac{3}{30}\\\\\\
      &P(X=4,Y=0)=P(X=4,Y=1)=\frac{4}{30}\\\\\\
      &P(X=5,Y=0)=P(X=5,Y=1)=\frac{5}{30}\\\\\\
    \end{split}
  \end{equation}

(2 )条件付き期待値$$E[X=k|Y=1]$$を求めよ。
  \begin{equation}
    \begin{split}
      E(X=k|Y=1)&=\sum_{k=1}^5 k(P(X=k|Y=1))\\\\\\
      &=\sum_{k=1}^5 k\times \frac{P(X=k,Y=1)}{P(Y=1)}\\\\\\
      &=\frac{110}{30}
    \end{split}
  \end{equation} 
