---
title: 確率情報理論2日目
tags: 
 - 確率情報理論
 - TeX
---

春休みに１日１問、確率情報理論を解く会に使った問題をのせています。3月2日の問題です。  
[問題PDF](https://marbou090.github.io/MyBlog/folder/sec02.pdf)  
[解答PDF](https://marbou090.github.io/MyBlog/folder/ans02.pdf)  
問題出典：東京図書発行 藤田岳彦著「弱点克服　大学生の確率・統計」  

以下は解答PDFと同じ内容です。

## 本日の問題解答
$$f_X(x)=2e^{-2x}~~~(0<x\le 3),~ce^{-4x}~~~(x>3),~0~~~(Otherwise)$$ のとき、  
(1) 定数cを求めよ。  
   \begin{equation}
     \begin{split}
       1 =& \int_{0}^{3}e^{-2x}dx + \int_{3}^{\infty}ce^{-4x}dx \\\\\\
       & = \left[ -e^{-2x} \right]_0^3 + \left[ c \frac{e^{-4x}}{-4} \right]_3^\infty \\\\\\
       & = 1-e^{-6} + c\frac{e^{-12}}{4} \\\\\\
     \end{split}
   \end{equation}
   よって、 $$c=4e^6 $$ である。
(2) E[X]を求めよ。  
  \begin{equation}
    \begin{split}
      E[X] &= \int_{0}^{3} x2e^{-2x} dx + c\int_{3}^{\infty}xe^{-4x}dx \\\\\\
      &= \int_{0}^{6} ue^{-u}\frac{du}{2} + c\int_{12}^{\infty}\frac{u}{4}e^{-u}\frac{du}{4} \\\\\\
      &= \frac{1}{2}\left[ -(u+1)e^{-u}  \right]_0^6 + \frac{c}{16}\left[ -(u+1)e^{-u} \right]_{12}^\infty \\\\\\
      &= \frac{1-7e^{-6}}{2} + \frac{13e^{-6}}{4} \\\\\\
      &= \frac{2-e^{-6}}{4} \\\\\\
    \end{split}
  \end{equation} 

## 本日の問題解説
(1) 場合わけに注意しながら、全範囲で１になることから積分して求める問題。  
(2) (1)と同じく、場合わけに注意して期待値を計算する。解答ではuと置いているが、そのままでも部分積分で簡単に求められる。