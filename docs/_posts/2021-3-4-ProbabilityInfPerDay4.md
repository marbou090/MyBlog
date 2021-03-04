---
title: 確率情報理論4日目
tags: 
 - 確率情報理論
 - TeX
---

春休みに１日１問、確率情報理論を解く会に使った問題をのせています。3月４日の問題です。  
[問題PDF](https://marbou090.github.io/MyBlog/folder/sec04.pdf)  
[解答PDF](https://marbou090.github.io/MyBlog/folder/ans04.pdf)  
問題出典：東京図書発行 藤田岳彦著「弱点克服　大学生の確率・統計」  

以下は解答PDFと同じ内容です。

## 本日の問題解答
確率変数$$X$$が標準正規分布に従うとき、以下を求めよ。
(1) $$f_X(x)$$  
   Xが標準正規分布に従うとき、$$f_X(x)=ce^{-\frac{x^2}{2}}$$（cは定数）
   となる。このとき、cについて求めると、
   \begin{equation}
     \begin{split}
       \int_{-\infty}^{\infty} e^{-\frac{x^2}{2}} dx =& 2 \int_{0}^{\infty} e^{-\frac{x^2}{2}} dx \\\\\\
        &= 2 \int_{0}^{\infty} e^{-u}\sqrt{2}\frac{1}{2} u^{-\frac{1}{2}}du \ \ \ \  (x=\sqrt{2u}) \\\\\\
        &= \sqrt{2} \  \Gamma \left( \frac{1}{2} \right) \\\\\\
        &= \sqrt{2\pi}
     \end{split}
   \end{equation}
   よって、$$\sqrt{2\pi} c =1$$となることから、 \\\\\\
   \begin{equation}
   \therefore c=\frac{1}{\sqrt{2\pi}}
   \end{equation}
  より、
   \begin{equation}
    f_X(x)=\frac{1}{2\pi} e^{-\frac{x^2}{2}}
   \end{equation}
(2) $$E[X]$$  
  $$\displaystyle xe^{-\frac{x^2}{2}}$$が奇関数であることを利用する。
  \begin{equation}
    \begin{split}
      E[X]&= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty}xe^{-\frac{x^2}{2}}dx \\\\\\
      &= \frac{1}{\sqrt{2\pi}} \left[ -e^{-\frac{x^2}{2}} \right]_{-\infty}^{\infty} \\\\\\
      &= 0
    \end{split}
  \end{equation} 
(3) $$V[X]$$  
  $$V[X]=E(X^2)-(E(X))^2$$を利用する。 
  \begin{equation}
    \begin{split}
      E[X^2]&=\frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} x^2 e^{-\frac{x^2}{2}}dx \\\\\\
      &= 2 \frac{1}{\sqrt{2\pi}} \int_{0}^{\infty} x^2e^{-\frac{x^2}{2}} dx \\\\\\
      &= 2 \frac{1}{\sqrt{2\pi}} \int_{0}^{\infty} (2u)e^{-u} \sqrt{2} \frac{1}{2}u^{-\frac{1}{2}}du \\\\\\
      &= 2 \frac{1}{\sqrt{2\pi}} \Gamma \left( \frac{3}{2} \right) \\\\\\
      &= 1
    \end{split}
  \end{equation}
  よって、
  \begin{equation}
    \begin{split}
      V[X]&=E(X^2)-(E(X))^2 \\\\\\
      &= 1-0^2 \\\\\\
      &=1 
    \end{split}
  \end{equation}

## 本日の問題解説
### 標準正規分布
\begin{equation}
    $$\displaystyle f_X(x)=\frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}$$
\end{equation}

### 正規分布
  $$Y=\mu + \sigma X$$とすると、
  \begin{equation}
    $$\displaystyle f_Y(x)=\frac{1}{\sqrt{2\pi}\sigma} e^{-\frac{(x-\mu)^2}{2\sigma ^2}}$$
  \end{equation}

### ガンマ関数
    **定義**　$$\displaystyle \Gamma (s)=\int_{0}^{\infty}x^{s-1}e^{-x}dx \. \. \. (s>0)$$  
    （また、$$e^{-x}=u$$と置換すると、$$\displaystyle \Gamma (s)=\int_{0}^{1}(-\log u)^{s-1} du$$となる。）

 標準正規分布と正規分布は暗記さえすれば期待値と分散がわかればすぐに密度関数を求められる。
 解答にあるように標準正規分布から正規分布を求めることもできるので、一度はガンマ関数を用いて求めてみてもよいと思う。
  

## おかわり問題解答
確率変数$$A,B$$がそれぞれ$$A\sim N(0,1),~B\sim (N2,5)$$となっている。
このことを用いて以下を求めよ。
(1 )$$E[A^{99}]$$  
  奇関数の定積分は０であることから、 
  \begin{equation}
    \begin{split}
      E(C^{99}) &= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} x^{99} e^{-\frac{x^2}{2}} dx \\\\\\
      =0
    \end{split}
  \end{equation} 
(2 )$$f_B(x)$$
   \begin{equation}
     \begin{split}
       F_B(x)&=P(B\le x) \\\\\\
       &=P(2+\sqrt{5}A \le x)\\\\\\
       &=P\left( A\le \frac{2-x}{\sqrt{5}} \right) \\\\\\
       &=\Phi \left( \frac{x-2}{\sqrt{5}} \right) 
     \end{split}
   \end{equation}
   両辺をxで微分して、
   \begin{equation}
     \begin{split}
       f_B(x) &= \Phi' \left( \frac{x-2}{\sqrt{5}} \right) \left( \frac{x-2}{\sqrt{5}} \right)'\\\\\\
       &= \frac{1}{\sqrt{10\pi}}e^{-\frac{(x-2)^2}{10}}
     \end{split}
   \end{equation}
   (補足：$$\Phi (x)=P(N(0,1)\le x)$$は標準正規分布の分布関数 \\\\\\ 

## おかわり問題解説
(2)は正規分布の公式を暗記していれば計算０ですぐ答えが出る。ここでは実際に標準正規分布から計算を行う方法を用いた。
$$B=2+\sqrt{5}A$$であることから分布関数を経由して求めた。正規分布は式が面倒であるため、$$\Phi (x)$$という形で整理してから
計算を行うとミスが少ないと思う（体感）。
