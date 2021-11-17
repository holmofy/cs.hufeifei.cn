---
title: Latex
categories: Latex
mathjax: true
keywords: Latex,公式,参考手册
description: Latex公式参考手册
---

## get started

<style>
.h3-section-list {
    columns: 1 !important;
}
.MarkdownBody table td:first-child {
    white-space: normal;
}
</style>

### 函数、符号及特殊字符

|               声调/变音符号                |                                              |
| :----------------------------------------: | -------------------------------------------- |
| `\dot{a}, \ddot{a}, \acute{a}, \grave{a}`  | $ \dot{a}, \ddot{a}, \acute{a}, \grave{a} $  |
| `\check{a}, \breve{a}, \tilde{a}, \bar{a}` | $ \check{a}, \breve{a}, \tilde{a}, \bar{a} $ |
|      `\hat{a}, \widehat{a}, \vec{a}`       | $ \hat{a}, \widehat{a}, \vec{a} $            |

|                           标准函数                           |                                                              |
| :----------------------------------------------------------: | ------------------------------------------------------------ |
|             `\exp_a b = a^b, \exp b = e^b, 10^m`             | $ \exp_a b = a^b, \exp b = e^b, 10^m $                       |
|             `\ln c, \lg d = \log e, \log_{10} f`             | $ \ln c, \lg d = \log e, \log_{10} f $                       |
|       `\sin a, \cos b, \tan c, \cot d, \sec e, \csc f`       | $ \sin a, \cos b, \tan c, \cot d, \sec e, \csc f $           |
|              `\arcsin a, \arccos b, \arctan c`               | $ \arcsin a, \arccos b, \arctan c $                          |
|              `\arccot d, \arcsec e, \arccsc f`               | $\arccot d, \arcsec e, \arccsc f$                            |
|             `\sinh a, \cosh b, \tanh c, \coth d`             | $ \sinh a, \cosh b, \tanh c, \coth d $                       |
| `\operatorname{sh}k, \operatorname{ch}l, \operatorname{th}m, \operatorname{coth}n` | $ \operatorname{sh}k, \operatorname{ch}l, \operatorname{th}m, \operatorname{coth}n $ |
| `\operatorname{argsh}o, \operatorname{argch}p, \operatorname{argth}q` | $ \operatorname{argsh}o, \operatorname{argch}p, \operatorname{argth}q $ |
|              `\sgn r, \left\vert s \right\vert`              | $ \sgn r, \left\vert s \right\vert $                         |
|                    `\min(x,y), \max(x,y)`                    | $ \min(x,y), \max(x,y) $                                     |

|                界限                |                                      |
| :--------------------------------: | ------------------------------------ |
|  `\min x, \max y, \inf s, \sup t`  | $ \min x, \max y, \inf s, \sup t $   |
|   `\lim u, \liminf v, \limsup w`   | $ \lim u, \liminf v, \limsup w $     |
| `\dim p, \deg q, \det m, \ker\phi` | $ \dim p, \deg q, \det m, \ker\phi $ |

|                   投射                   |                                            |
| :--------------------------------------: | ------------------------------------------ |
| `\Pr j, \hom l, \lVert z \rVert, \arg z` | $ \Pr j, \hom l, \lVert z \rVert, \arg z $ |

|                                                           微分及导数                                                           |                                                                                                                                  |
| :----------------------------------------------------------------------------------------------------------------------------: | -------------------------------------------------------------------------------------------------------------------------------- |
|                                           `dt, \mathrm{d}t, \partial t, \nabla\psi`                                            | $ dt, \mathrm{d}t, \partial t, \nabla\psi $                                                                                      |
| `dy/dx, \mathrm{d}y/\mathrm{d}x, \frac{dy}{dx}, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\partial^2}{\partial x_1\partial x_2}y` | $ dy/dx, \mathrm{d}y/\mathrm{d}x, \frac{dy}{dx}, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\partial^2}{\partial x_1\partial x_2}y $ |
|                               `\prime, \backprime, f^\prime, f', f'', f^{(3)}, \dot y, \ddot y`                                | $ \prime, \backprime, f^\prime, f', f'', f^{(3)}, \dot y, \ddot y $                                                              |

|                              类字母符号及常数                              |                                                                              |
| :------------------------------------------------------------------------: | ---------------------------------------------------------------------------- |
|      `\infty, \aleph, \complement, \backepsilon, \eth, \Finv, \hbar`       | $ \infty, \aleph, \complement, \backepsilon, \eth, \Finv, \hbar $            |
| `\Im, \imath, \jmath, \Bbbk, \ell, \mho, \wp, \Re, \circledS, \S, \P, \AA` | $ \Im, \imath, \jmath, \Bbbk, \ell, \mho, \wp, \Re, \circledS, \S, \P, \AA $ |

|                 模算数                 |                                          |
| :------------------------------------: | ---------------------------------------- |
|        `s_k \equiv 0 \pmod{m}`         | $ s_k \equiv 0 \pmod{m} $                |
|              `a \bmod b`               | $ a \bmod b $                            |
| `\gcd(m, n), \operatorname{lcm}(m, n)` | $ \gcd(m, n), \operatorname{lcm}(m, n) $ |
|  `\mid, \nmid, \shortmid, \nshortmid`  | $ \mid, \nmid, \shortmid, \nshortmid $   |

|                            根号                            |                                                              |
| :--------------------------------------------------------: | ------------------------------------------------------------ |
| `\surd, \sqrt{2}, \sqrt[n]{}, \sqrt[3]{\frac{x^3+y^3}{2}}` | $ \surd, \sqrt{2}, \sqrt[n]{}, \sqrt[3]{\frac{x^3+y^3}{2}} $ |

|                    运算符                     |                                                 |
| :-------------------------------------------: | ----------------------------------------------- |
|          `+, -, \pm, \mp, \dotplus`           | $ +, -, \pm, \mp, \dotplus $                    |
| `\times, \div, \divideontimes, /, \backslash` | $ \times, \div, \divideontimes, /, \backslash $ |
|    `\cdot, * \ast, \star, \circ, \bullet`     | $ \cdot, * \ast, \star, \circ, \bullet $        |
|   `\boxplus, \boxminus, \boxtimes, \boxdot`   | $ \boxplus, \boxminus, \boxtimes, \boxdot $     |
|  `\oplus, \ominus, \otimes, \oslash, \odot`   | $ \oplus, \ominus, \otimes, \oslash, \odot $    |
|   `\circleddash, \circledcirc, \circledast`   | $ \circleddash, \circledcirc, \circledast $     |
|       `\bigoplus, \bigotimes, \bigodot`       | $ \bigoplus, \bigotimes, \bigodot $             |

|                              集合                               |                                                                   |
| :-------------------------------------------------------------: | ----------------------------------------------------------------- |
|            `\{ \}, \O \empty \emptyset, \varnothing`            | $ \{ \}, \O \empty \emptyset, \varnothing $                       |
|               `\in, \notin \not\in, \ni, \not\ni`               | $ \in, \notin \not\in, \ni, \not\ni $                             |
|                  `\cap, \Cap, \sqcap, \bigcap`                  | $ \cap, \Cap, \sqcap, \bigcap $                                   |
|   `\cup, \Cup, \sqcup, \bigcup, \bigsqcup, \uplus, \biguplus`   | $ \cup, \Cup, \sqcup, \bigcup, \bigsqcup, \uplus, \biguplus $     |
|               `\setminus, \smallsetminus, \times`               | $ \setminus, \smallsetminus, \times $                             |
|                  `\subset, \Subset, \sqsubset`                  | $ \subset, \Subset, \sqsubset $                                   |
|                  `\supset, \Supset, \sqsupset`                  | $ \supset, \Supset, \sqsupset $                                   |
| `\subseteq, \nsubseteq, \subsetneq, \varsubsetneq, \sqsubseteq` | $ \subseteq, \nsubseteq, \subsetneq, \varsubsetneq, \sqsubseteq $ |
| `\supseteq, \nsupseteq, \supsetneq, \varsupsetneq, \sqsupseteq` | $ \supseteq, \nsupseteq, \supsetneq, \varsupsetneq, \sqsupseteq $ |
|     `\subseteqq, \nsubseteqq, \subsetneqq, \varsubsetneqq`      | $ \subseteqq, \nsubseteqq, \subsetneqq, \varsubsetneqq $          |
|     `\supseteqq, \nsupseteqq, \supsetneqq, \varsupsetneqq`      | $ \supseteqq, \nsupseteqq, \supsetneqq, \varsupsetneqq $          |

|                                   关系符号                                    |                                                                                 |
| :---------------------------------------------------------------------------: | ------------------------------------------------------------------------------- |
|                      `=, \ne, \neq, \equiv, \not\equiv`                       | $ =, \ne, \neq, \equiv, \not\equiv $                                            |
|      `\doteq, \doteqdot,` `\overset{\underset{\mathrm{def}}{}}{=},` `:=`      | $\doteq, \doteqdot,$ $\overset{\underset{\mathrm{def}}{}}{=},$ $:=$             |
| `\sim, \nsim, \backsim, \thicksim, \simeq, \backsimeq, \eqsim, \cong, \ncong` | $ \sim, \nsim, \backsim, \thicksim, \simeq, \backsimeq, \eqsim, \cong, \ncong $ |
|        `\approx, \thickapprox, \approxeq, \asymp, \propto, \varpropto`        | $ \approx, \thickapprox, \approxeq, \asymp, \propto, \varpropto $               |
|              `<, \nless, \ll, \not\ll, \lll, \not\lll, \lessdot`              | $ <, \nless, \ll, \not\ll, \lll, \not\lll, \lessdot $                           |
|               `>, \ngtr, \gg, \not\gg, \ggg, \not\ggg, \gtrdot`               | $ >, \ngtr, \gg, \not\gg, \ggg, \not\ggg, \gtrdot $                             |
|         `\le, \leq, \lneq, \leqq, \nleq, \nleqq, \lneqq, \lvertneqq`          | $ \le, \leq, \lneq, \leqq, \nleq, \nleqq, \lneqq, \lvertneqq $                  |
|         `\ge, \geq, \gneq, \geqq, \ngeq, \ngeqq, \gneqq, \gvertneqq`          | $ \ge, \geq, \gneq, \geqq, \ngeq, \ngeqq, \gneqq, \gvertneqq $                  |
|    `\lessgtr, \lesseqgtr, \lesseqqgtr, \gtrless, \gtreqless, \gtreqqless`     | $ \lessgtr, \lesseqgtr, \lesseqqgtr, \gtrless, \gtreqless, \gtreqqless $        |
|                     `\leqslant, \nleqslant, \eqslantless`                     | $ \leqslant, \nleqslant, \eqslantless $                                         |
|                     `\geqslant, \ngeqslant, \eqslantgtr`                      | $ \geqslant, \ngeqslant, \eqslantgtr $                                          |
|                  `\lesssim, \lnsim, \lessapprox, \lnapprox`                   | $ \lesssim, \lnsim, \lessapprox, \lnapprox $                                    |
|                   `\gtrsim, \gnsim, \gtrapprox, \gnapprox`                    | $ \gtrsim, \gnsim, \gtrapprox, \gnapprox $                                      |
|                 `\prec, \nprec, \preceq, \npreceq, \precneqq`                 | $ \prec, \nprec, \preceq, \npreceq, \precneqq $                                 |
|                 `\succ, \nsucc, \succeq, \nsucceq, \succneqq`                 | $ \succ, \nsucc, \succeq, \nsucceq, \succneqq $                                 |
|                         `\preccurlyeq, \curlyeqprec`                          | $ \preccurlyeq, \curlyeqprec $                                                  |
|                         `\succcurlyeq, \curlyeqsucc`                          | $ \succcurlyeq, \curlyeqsucc $                                                  |
|               `\precsim, \precnsim, \precapprox, \precnapprox`                | $ \precsim, \precnsim, \precapprox, \precnapprox $                              |
|               `\succsim, \succnsim, \succapprox, \succnapprox`                | $ \succsim, \succnsim, \succapprox, \succnapprox $                              |

|                                   几何符号                                    |                                                                                 |
| :---------------------------------------------------------------------------: | ------------------------------------------------------------------------------- |
|           `\parallel, \nparallel, \shortparallel, \nshortparallel`            | $ \parallel, \nparallel, \shortparallel, \nshortparallel $                      |
|          `\perp, \angle, \sphericalangle, \measuredangle, 45^\circ`           | $ \perp, \angle, \sphericalangle, \measuredangle, 45^\circ $                    |
|  `\Box, \blacksquare, \diamond, \Diamond \lozenge, \blacklozenge, \bigstar`   | $ \Box, \blacksquare, \diamond, \Diamond \lozenge, \blacklozenge, \bigstar $    |
|            `\bigcirc, \triangle, \bigtriangleup, \bigtriangledown`            | $ \bigcirc, \triangle, \bigtriangleup, \bigtriangledown $                       |
|                         `\vartriangle, \triangledown`                         | $ \vartriangle, \triangledown $                                                 |
| `\blacktriangle, \blacktriangledown, \blacktriangleleft, \blacktriangleright` | $ \blacktriangle, \blacktriangledown, \blacktriangleleft, \blacktriangleright $ |

|                                              逻辑符号                                              |                                                                                                    |
| :------------------------------------------------------------------------------------------------: | -------------------------------------------------------------------------------------------------- |
|                                    `\forall, \exists, \nexists`                                    | $ \forall, \exists, \nexists $                                                                     |
|                                    `\therefore, \because, \And`                                    | $ \therefore, \because, \And $                                                                     |
|                                `\or \lor \vee, \curlyvee, \bigvee`                                 | $ \or \lor \vee, \curlyvee, \bigvee $                                                              |
|                            `\and \land \wedge, \curlywedge, \bigwedge`                             | $ \and \land \wedge, \curlywedge, \bigwedge $                                                      |
| `\bar{q}, \bar{abc}, \overline{q}, \overline{abc},` `\lnot \neg, \not\operatorname{R}, \bot, \top` | $\bar{q}, \bar{abc}, \overline{q}, \overline{abc},$ $\lnot \neg, \not\operatorname{R}, \bot, \top$ |
|                              `\vdash \dashv, \vDash, \Vdash, \models`                              | $ \vdash \dashv, \vDash, \Vdash, \models $                                                         |
|                             `\Vvdash \nvdash \nVdash \nvDash \nVDash`                              | $ \Vvdash \nvdash \nVdash \nvDash \nVDash $                                                        |
|                             `\ulcorner \urcorner \llcorner \lrcorner`                              | $ \ulcorner \urcorner \llcorner \lrcorner $                                                        |

|                                                                                    箭头                                                                                     |                                                                                                                                                                               |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                                                         `\Rrightarrow, \Lleftarrow`                                                                         | $ \Rrightarrow, \Lleftarrow $                                                                                                                                                 |
|                                                            `\Rightarrow, \nRightarrow, \Longrightarrow \implies`                                                            | $ \Rightarrow, \nRightarrow, \Longrightarrow \implies $                                                                                                                       |
|                                                                  `\Leftarrow, \nLeftarrow, \Longleftarrow`                                                                  | $ \Leftarrow, \nLeftarrow, \Longleftarrow $                                                                                                                                   |
|                                                        `\Leftrightarrow, \nLeftrightarrow, \Longleftrightarrow \iff`                                                        | $ \Leftrightarrow, \nLeftrightarrow, \Longleftrightarrow \iff $                                                                                                               |
|                                                                    `\Uparrow, \Downarrow, \Updownarrow`                                                                     | $ \Uparrow, \Downarrow, \Updownarrow $                                                                                                                                        |
|                                                              `\rightarrow \to, \nrightarrow, \longrightarrow`                                                               | $ \rightarrow \to, \nrightarrow, \longrightarrow $                                                                                                                            |
|                                                               `\leftarrow \gets, \nleftarrow, \longleftarrow`                                                               | $ \leftarrow \gets, \nleftarrow, \longleftarrow $                                                                                                                             |
|                                                          `\leftrightarrow, \nleftrightarrow, \longleftrightarrow`                                                           | $ \leftrightarrow, \nleftrightarrow, \longleftrightarrow $                                                                                                                    |
|                                                                    `\uparrow, \downarrow, \updownarrow`                                                                     | $ \uparrow, \downarrow, \updownarrow $                                                                                                                                        |
|                                                                  `\nearrow, \swarrow, \nwarrow, \searrow`                                                                   | $ \nearrow, \swarrow, \nwarrow, \searrow $                                                                                                                                    |
|                                                                           `\mapsto, \longmapsto`                                                                            | $ \mapsto, \longmapsto $                                                                                                                                                      |
| `\rightharpoonup \rightharpoondown \leftharpoonup \leftharpoondown \upharpoonleft \upharpoonright \downharpoonleft \downharpoonright \rightleftharpoons \leftrightharpoons` | $ \rightharpoonup \rightharpoondown \leftharpoonup \leftharpoondown \upharpoonleft \upharpoonright \downharpoonleft \downharpoonright \rightleftharpoons \leftrightharpoons $ |
|                           `\curvearrowleft \circlearrowleft \Lsh \upuparrows \rightrightarrows \rightleftarrows \rightarrowtail \looparrowright`                            | $ \curvearrowleft \circlearrowleft \Lsh \upuparrows \rightrightarrows \rightleftarrows \rightarrowtail \looparrowright $                                                      |
|                          `\curvearrowright \circlearrowright \Rsh \downdownarrows \leftleftarrows \leftrightarrows \leftarrowtail \looparrowleft`                           | $ \curvearrowright \circlearrowright \Rsh \downdownarrows \leftleftarrows \leftrightarrows \leftarrowtail \looparrowleft $                                                    |
|                            `\hookrightarrow \hookleftarrow \multimap \leftrightsquigarrow \rightsquigarrow \twoheadrightarrow \twoheadleftarrow`                            | $ \hookrightarrow \hookleftarrow \multimap \leftrightsquigarrow \rightsquigarrow \twoheadrightarrow \twoheadleftarrow $                                                       |

|                                     特殊符号                                      |                                                                                     |
| :-------------------------------------------------------------------------------: | ----------------------------------------------------------------------------------- |
|                 `\amalg \P \S \% \dagger \ddagger \ldots \cdots`                  | $ \amalg \P \S \% \dagger \ddagger \ldots \cdots $                                  |
|                 `\smile \frown \wr \triangleleft \triangleright`                  | $ \smile \frown \wr \triangleleft \triangleright $                                  |
| `\diamondsuit, \heartsuit, \clubsuit, \spadesuit, \Game, \flat, \natural, \sharp` | $ \diamondsuit, \heartsuit, \clubsuit, \spadesuit, \Game, \flat, \natural, \sharp $ |

|                                       未排序                                        |                                                                                       |
| :---------------------------------------------------------------------------------: | ------------------------------------------------------------------------------------- |
|   `\diagup \diagdown \centerdot \ltimes \rtimes \leftthreetimes \rightthreetimes`   | $ \diagup \diagdown \centerdot \ltimes \rtimes \leftthreetimes \rightthreetimes $     |
| `\eqcirc \circeq \triangleq \bumpeq \Bumpeq \doteqdot \risingdotseq \fallingdotseq` | $ \eqcirc \circeq \triangleq \bumpeq \Bumpeq \doteqdot \risingdotseq \fallingdotseq $ |
|          `\intercal \barwedge \veebar \doublebarwedge \between \pitchfork`          | $ \intercal \barwedge \veebar \doublebarwedge \between \pitchfork $                   |
|         `\vartriangleleft \ntriangleleft \vartriangleright \ntriangleright`         | $ \vartriangleleft \ntriangleleft \vartriangleright \ntriangleright $                 |
|        `\trianglelefteq \ntrianglelefteq \trianglerighteq \ntrianglerighteq`        | $ \trianglelefteq \ntrianglelefteq \trianglerighteq \ntrianglerighteq $               |
|                     `\not6, \frac{1\not6}{\not64}=\frac{1}{4}`                      | $ \not6, \frac{1\not6}{\not64}=\frac{1}{4} $                                          |

### 上标、下标及积分等

|                                                          功能                                                           |                                  语法                                   |                                   效果                                    |
| :---------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------: | :-----------------------------------------------------------------------: |
|                                                          上标                                                           |                                  `a^2`                                  |                                  $ a^2 $                                  |
|                                                          下标                                                           |                                  `a_2`                                  |                                  $ a_2 $                                  |
|                                                          组合                                                           |                                `a^{2+2}`                                |                                $ a^{2+2} $                                |
|                                                                                                                         |                                `a_{i,j}`                                |                                $ a_{i,j} $                                |
|                                                       结合上下标                                                        |                                 `x_2^3`                                 |                                 $ x_2^3 $                                 |
|                                                       前置上下标                                                        |                             `{}_1^2\!X_3^4`                             |                             $ {}_1^2\!X_3^4 $                             |
|                                                    导数 （**HTML**）                                                    |                                  `x'`                                   |                                  $ x' $                                   |
|                                                    导数 （**PNG**）                                                     |                               `x^\prime`                                |                               $ x^\prime $                                |
|                                                    导数 （**错误**）                                                    |                                `x\prime`                                |                                $ x\prime $                                |
|                                                         导数点                                                          |                                `\dot{x}`                                |                                $ \dot{x} $                                |
|                                                                                                                         |                               `\ddot{y}`                                |                               $ \ddot{y} $                                |
|                                                          向量                                                           |                                `\vec{c}`                                |                                $ \vec{c} $                                |
|                                                                                                                         |                          `\overleftarrow{a b}`                          |                          $ \overleftarrow{a b} $                          |
|                                                                                                                         |                         `\overrightarrow{c d}`                          |                         $ \overrightarrow{c d} $                          |
|                                                                                                                         |                       `\overleftrightarrow{a b}`                        |                       $ \overleftrightarrow{a b} $                        |
|                                                                                                                         |                            `\widehat{e f g}`                            |                            $ \widehat{e f g} $                            |
| 上弧 <br/>（注: 正确应该用 \overarc，但在这里行不通。要用建议的语法作为解决办法。）（使用\overarc时需要引入{arcs}包。） |                         `\overset{\frown} {AB}`                         |                         $ \overset{\frown} {AB} $                         |
|                                                         上划线                                                          |                           `\overline{h i j}`                            |                           $ \overline{h i j} $                            |
|                                                         下划线                                                          |                           `\underline{k l m}`                           |                           $ \underline{k l m} $                           |
|                                                         上括号                                                          |                      `\overbrace{1+2+\cdots+100}`                       |                      $ \overbrace{1+2+\cdots+100} $                       |
|                                                                                                                         |                  `\overbrace{ 1+2+\cdots+100 }^{5050}`                  |                  $ \overbrace{ 1+2+\cdots+100 }^{5050} $                  |
|                                                         下括号                                                          |                       `\underbrace{a+b+\cdots+z}`                       |                       $ \underbrace{a+b+\cdots+z} $                       |
|                                                                                                                         |                   `\underbrace{ a+b+\cdots+z }_{26}`                    |                   $ \underbrace{ a+b+\cdots+z }_{26} $                    |
|                                                          求和                                                           |                           `\sum_{k=1}^N k^2`                            |                           $ \sum_{k=1}^N k^2 $                            |
|                                                                                                                         |             `\begin{matrix} \sum_{k=1}^N k^2 \end{matrix}`              |             $ \begin{matrix} \sum_{k=1}^N k^2 \end{matrix} $              |
|                                                          求积                                                           |                           `\prod_{i=1}^N x_i`                           |                           $ \prod_{i=1}^N x_i $                           |
|                                                                                                                         |             `\begin{matrix} \prod_{i=1}^N x_i \end{matrix}`             |             $ \begin{matrix} \prod_{i=1}^N x_i \end{matrix} $             |
|                                                          上积                                                           |                          `\coprod_{i=1}^N x_i`                          |                          $ \coprod_{i=1}^N x_i $                          |
|                                                                                                                         |            `\begin{matrix} \coprod_{i=1}^N x_i \end{matrix}`            |            $ \begin{matrix} \coprod_{i=1}^N x_i \end{matrix} $            |
|                                                          极限                                                           |                        `\lim_{n \to \infty}x_n`                         |                        $ \lim_{n \to \infty}x_n $                         |
|                                                                                                                         |          `\begin{matrix} \lim_{n \to \infty}x_n \end{matrix}`           |          $ \begin{matrix} \lim_{n \to \infty}x_n \end{matrix} $           |
|                                                          积分                                                           |                    `\int_{-N}^{N} e^x\, \mathrm{d}x`                    |                    $ \int_{-N}^{N} e^x\, \mathrm{d}x $                    |
|                                                                                                                         |      `\begin{matrix} \int_{-N}^{N} e^x\, \mathrm{d}x \end{matrix}`      |      $ \begin{matrix} \int_{-N}^{N} e^x\, \mathrm{d}x \end{matrix} $      |
|                                                        双重积分                                                         |               `\iint_{D}^{W} \, \mathrm{d}x\,\mathrm{d}y`               |               $ \iint_{D}^{W} \, \mathrm{d}x\,\mathrm{d}y $               |
|                                                        三重积分                                                         |        `\iiint_{E}^{V} \, \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z`        |        $ \iiint_{E}^{V} \, \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z $        |
|                                                        四重积分                                                         | `\iiiint_{F}^{U} \, \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t` | $ \iiiint_{F}^{U} \, \mathrm{d}x\,\mathrm{d}y\,\mathrm{d}z\,\mathrm{d}t $ |
|                                                闭合的曲线积分、曲面积分                                                 |           `\oint_{C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y`            |           $ \oint_{C} x^3\, \mathrm{d}x + 4y^2\, \mathrm{d}y $            |
|                                                          交集                                                           |                            `\bigcap_1^{n} p`                            |                            $ \bigcap_1^{n} p $                            |
|                                                          并集                                                           |                            `\bigcup_1^{k} p`                            |                            $ \bigcup_1^{k} p $                            |



### 分数、矩阵和多行列式

|        功能        |                                                                                                      语法                                                                                                       |                                                                                                       效果                                                                                                        |
| :----------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|        分数        |                                                                                                `\frac{2}{4}=0.5`                                                                                                |                                                                                                $ \frac{2}{4}=0.5 $                                                                                                |
|                    |                                                                                                  `{2 \over 3}`                                                                                                  |                                                                                                  $ {2 \over 3} $                                                                                                  |
|                    |                                                                                              `{{a+b} \over {a-b}}`                                                                                              |                                                                                             $ { {a+b} \over {a-b} } $                                                                                             |
|      小型分数      |                                                                                              `\tfrac{2}{4} = 0.5`                                                                                               |                                                                                              $ \tfrac{2}{4} = 0.5 $                                                                                               |
|  大型分数（嵌套）  |                                                                                `\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a`                                                                                 |                                                                                $ \cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a $                                                                                 |
| 大型分数（不嵌套） |                                                                   `\dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a`                                                                    |                                                                   $ \dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a $                                                                    |
|     二项式系数     |                                                                        `\dbinom{n}{r}=\binom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r}`                                                                         |                                                                        $ \dbinom{n}{r}=\binom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r} $                                                                         |
|                    |                                                                 `n \choose n-r, n^2 \choose r_1, a-b \choose c+d, {n \choose 0}+{n \choose 1}`                                                                  |                                                              $ n \choose n-r$,$ n^2 \choose r_1$,$ a-b \choose c+d$,$ {n \choose 0}+{n \choose 1} $                                                               |
|   小型二项式系数   |                                                                        `\tbinom{n}{r}=\tbinom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r}`                                                                        |                                                                        $ \tbinom{n}{r}=\tbinom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r} $                                                                        |
|   大型二项式系数   |                                                                        `\binom{n}{r}=\dbinom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r}`                                                                         |                                                                        $ \binom{n}{r}=\dbinom{n}{n-r}=\mathrm{C}_n^r=\mathrm{C}_n^{n-r} $                                                                         |
|        矩阵        |                                                                                  `\begin{matrix} x & y \\ z & v \end{matrix}`                                                                                   |                                                                                  $ \begin{matrix} x & y \\ z & v \end{matrix} $                                                                                   |
|                    |                                                                                 `\begin{vmatrix} x & y \\ z & v \end{vmatrix}`                                                                                  |                                                                                 $ \begin{vmatrix} x & y \\ z & v \end{vmatrix} $                                                                                  |
|                    |                                                                                 `\begin{Vmatrix} x & y \\ z & v \end{Vmatrix}`                                                                                  |                                                                                 $ \begin{Vmatrix} x & y \\ z & v \end{Vmatrix} $                                                                                  |
|                    |                                                   `\begin{bmatrix} 0      & \cdots & 0      \\ \vdots & \ddots & \vdots \\ 0      & \cdots & 0 \end{bmatrix}`                                                   |                                                   $ \begin{bmatrix} 0      & \cdots & 0      \\ \vdots & \ddots & \vdots \\ 0      & \cdots & 0 \end{bmatrix} $                                                   |
|                    |                                                                                 `\begin{Bmatrix} x & y \\ z & v \end{Bmatrix}`                                                                                  |                                                                                 $ \begin{Bmatrix} x & y \\ z & v \end{Bmatrix} $                                                                                  |
|                    |                                                                                 `\begin{pmatrix} x & y \\ z & v \end{pmatrix}`                                                                                  |                                                                                 $ \begin{pmatrix} x & y \\ z & v \end{pmatrix} $                                                                                  |
|                    |                                                                        `\bigl( \begin{smallmatrix} a&b\\ c&d \end{smallmatrix} \bigr) `                                                                         |                                                                        $ \bigl( \begin{smallmatrix} a&b\\ c&d \end{smallmatrix} \bigr)  $                                                                         |
|      条件定义      |                                                   `f(n) = \begin{cases}  n/2,  & \mbox{if }n\mbox{ is even} \\ 3n+1, & \mbox{if }n\mbox{ is odd} \end{cases}`                                                   |                                                   $ f(n) = \begin{cases}  n/2,  & \mbox{if }n\mbox{ is even} \\ 3n+1, & \mbox{if }n\mbox{ is odd} \end{cases} $                                                   |
|  多行等式、同余式  |                                                                       `\begin{align} f(x) & = (m+n)^2 \\ & = m^2+2mn+n^2 \\ \end{align} `                                                                       |                                                                       $ \begin{align} f(x) & = (m+n)^2 \\ & = m^2+2mn+n^2 \\ \end{align}  $                                                                       |
|                    | `\begin{align} 3^{6n+3}+4^{6n+3}  & \equiv (3^3)^{2n+1}+(4^3)^{2n+1}\\   & \equiv 27^{2n+1}+64^{2n+1}\\   & \equiv 27^{2n+1}+(-27)^{2n+1}\\  & \equiv 27^{2n+1}-27^{2n+1}\\ & \equiv 0 \pmod{91}\\ \end{align}` | $ \begin{align} 3^{6n+3}+4^{6n+3}  & \equiv (3^3)^{2n+1}+(4^3)^{2n+1}\\   & \equiv 27^{2n+1}+64^{2n+1}\\   & \equiv 27^{2n+1}+(-27)^{2n+1}\\  & \equiv 27^{2n+1}-27^{2n+1}\\ & \equiv 0 \pmod{91}\\ \end{align} $ |
|                    |                                                         `\begin{alignat}{3} f(x) & = (m-n)^2 \\ f(x) & = (-m+n)^2 \\ & = m^2-2mn+n^2 \\ \end{alignat} `                                                         |                                                         $ \begin{alignat}{3} f(x) & = (m-n)^2 \\ f(x) & = (-m+n)^2 \\ & = m^2-2mn+n^2 \\ \end{alignat}  $                                                         |
| 多行等式（左对齐） |                                                                 `\begin{array}{lcl} z        & = & a \\ f(x,y,z) & = & x + y + z  \end{array}`                                                                  |                                                                 $ \begin{array}{lcl} z        & = & a \\ f(x,y,z) & = & x + y + z  \end{array} $                                                                  |
| 多行等式（右对齐） |                                                                `\begin{array}{lcr} z        & = & a \\ f(x,y,z) & = & x + y + z     \end{array}`                                                                |                                                                $ \begin{array}{lcr} z        & = & a \\ f(x,y,z) & = & x + y + z     \end{array} $                                                                |
|     长公式换行     |                                                    `<math>f(x) \,\!</math> <math>= \sum_{n=0}^\infty a_n x^n </math> <math>= a_0+a_1x+a_2x^2+\cdots</math> `                                                    |                                                    $ <math>f(x) \,\!</math> <math>= \sum_{n=0}^\infty a_n x^n </math> <math>= a_0+a_1x+a_2x^2+\cdots</math>  $                                                    |
|       方程组       |                                                                    `\begin{cases} 3x + 5y +  z \\ 7x - 2y + 4z \\ -6x + 3y + 2z \end{cases}`                                                                    |                                                                    $ \begin{cases} 3x + 5y +  z \\ 7x - 2y + 4z \\ -6x + 3y + 2z \end{cases} $                                                                    |
|        数组        |                                                           `\begin{array}{|c|c||c|} a & b & S \\ \hline 0&0&1\\ 0&1&1\\ 1&0&1\\ 1&1&0\\ \end{array} `                                                            |                                                                                                 $ \begin{array}{                                                                                                  | c | c |  | c | } a & b & S \\ \hline 0&0&1\\ 0&1&1\\ 1&0&1\\ 1&1&0\\ \end{array}  $ |

### 字体

|                        希腊字母                         |                                                           |
| :-----------------------------------------------------: | --------------------------------------------------------- |
| `\Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta` | $ \Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta $ |
|     `\Iota \Kappa \Lambda \Mu \Nu \Xi \Omicron \Pi`     | $ \Iota \Kappa \Lambda \Mu \Nu \Xi \Omicron \Pi $         |
|    `\Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega`    | $ \Rho \Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega $       |
| `\alpha \beta \gamma \delta \epsilon \zeta \eta \theta` | $ \alpha \beta \gamma \delta \epsilon \zeta \eta \theta $ |
|     `\iota \kappa \lambda \mu \nu \omicron \xi \pi`     | $ \iota \kappa \lambda \mu \nu \omicron \xi \pi $         |
|    `\rho \sigma \tau \upsilon \phi \chi \psi \omega`    | $ \rho \sigma \tau \upsilon \phi \chi \psi \omega $       |
|         `\varepsilon \digamma \varkappa \varpi`         | $ \varepsilon \digamma \varkappa \varpi $                 |
|          `\varrho \varsigma \vartheta \varphi`          | $ \varrho \varsigma \vartheta \varphi $                   |

|          希伯来符号           |                                 |
| :---------------------------: | ------------------------------- |
| `\aleph \beth \gimel \daleth` | $ \aleph \beth \gimel \daleth $ |

|      黑板报粗体      |                        |
| :------------------: | ---------------------- |
| `\mathbb{ABCDEFGHI}` | $ \mathbb{ABCDEFGHI} $ |
| `\mathbb{JKLMNOPQR}` | $ \mathbb{JKLMNOPQR} $ |
| `\mathbb{STUVWXYZ}`  | $ \mathbb{STUVWXYZ} $  |

|           粗体           |                            |
| :----------------------: | -------------------------- |
|   `\mathbf{ABCDEFGHI}`   | $ \mathbf{ABCDEFGHI} $     |
|   `\mathbf{JKLMNOPQR}`   | $ \mathbf{JKLMNOPQR} $     |
|   `\mathbf{STUVWXYZ}`    | $ \mathbf{STUVWXYZ} $      |
| `\mathbf{abcdefghijklm}` | $ \mathbf{abcdefghijklm} $ |
| `\mathbf{nopqrstuvwxyz}` | $ \mathbf{nopqrstuvwxyz} $ |
|  `\mathbf{0123456789}`   | $ \mathbf{0123456789} $    |

|                         粗体希腊字母                          |                                                                 |
| :-----------------------------------------------------------: | --------------------------------------------------------------- |
| `\boldsymbol{\Alpha\Beta\Gamma\Delta\Epsilon\Zeta\Eta\Theta}` | $ \boldsymbol{\Alpha\Beta\Gamma\Delta\Epsilon\Zeta\Eta\Theta} $ |
|       `\boldsymbol{\Iota\Kappa\Lambda\Mu\Nu\Xi\Pi\Rho}`       | $ \boldsymbol{\Iota\Kappa\Lambda\Mu\Nu\Xi\Pi\Rho} $             |
|      `\boldsymbol{\Sigma\Tau\Upsilon\Phi\Chi\Psi\Omega}`      | $ \boldsymbol{\Sigma\Tau\Upsilon\Phi\Chi\Psi\Omega} $           |
| `\boldsymbol{\alpha\beta\gamma\delta\epsilon\zeta\eta\theta}` | $ \boldsymbol{\alpha\beta\gamma\delta\epsilon\zeta\eta\theta} $ |
|       `\boldsymbol{\iota\kappa\lambda\mu\nu\xi\pi\rho}`       | $ \boldsymbol{\iota\kappa\lambda\mu\nu\xi\pi\rho} $             |
|      `\boldsymbol{\sigma\tau\upsilon\phi\chi\psi\omega}`      | $ \boldsymbol{\sigma\tau\upsilon\phi\chi\psi\omega} $           |
|       `\boldsymbol{\varepsilon\digamma\varkappa\varpi}`       | $ \boldsymbol{\varepsilon\digamma\varkappa\varpi} $             |
|        `\boldsymbol{\varrho\varsigma\vartheta\varphi}`        | $ \boldsymbol{\varrho\varsigma\vartheta\varphi} $               |

| 斜体（拉丁字母默认）  |                         |
| :-------------------: | ----------------------- |
| `\mathit{0123456789}` | $ \mathit{0123456789} $ |

|               斜体希腊字母（小写字母默认）                |                                                             |
| :-------------------------------------------------------: | ----------------------------------------------------------- |
| `\mathit{\Alpha\Beta\Gamma\Delta\Epsilon\Zeta\Eta\Theta}` | $ \mathit{\Alpha\Beta\Gamma\Delta\Epsilon\Zeta\Eta\Theta} $ |
|       `\mathit{\Iota\Kappa\Lambda\Mu\Nu\Xi\Pi\Rho}`       | $ \mathit{\Iota\Kappa\Lambda\Mu\Nu\Xi\Pi\Rho} $             |
|      `\mathit{\Sigma\Tau\Upsilon\Phi\Chi\Psi\Omega}`      | $ \mathit{\Sigma\Tau\Upsilon\Phi\Chi\Psi\Omega} $           |

|          罗马体          |                            |
| :----------------------: | -------------------------- |
|   `\mathrm{ABCDEFGHI}`   | $ \mathrm{ABCDEFGHI} $     |
|   `\mathrm{JKLMNOPQR}`   | $ \mathrm{JKLMNOPQR} $     |
|   `\mathrm{STUVWXYZ}`    | $ \mathrm{STUVWXYZ} $      |
| `\mathrm{abcdefghijklm}` | $ \mathrm{abcdefghijklm} $ |
| `\mathrm{nopqrstuvwxyz}` | $ \mathrm{nopqrstuvwxyz} $ |
|  `\mathrm{0123456789}`   | $ \mathrm{0123456789} $    |

|         无衬线体         |                            |
| :----------------------: | -------------------------- |
|   `\mathsf{ABCDEFGHI}`   | $ \mathsf{ABCDEFGHI} $     |
|   `\mathsf{JKLMNOPQR}`   | $ \mathsf{JKLMNOPQR} $     |
|   `\mathsf{STUVWXYZ}`    | $ \mathsf{STUVWXYZ} $      |
| `\mathsf{abcdefghijklm}` | $ \mathsf{abcdefghijklm} $ |
| `\mathsf{nopqrstuvwxyz}` | $ \mathsf{nopqrstuvwxyz} $ |
|  `\mathsf{0123456789}`   | $ \mathsf{0123456789} $    |

|                    无衬线体希腊字母（仅大写）                    |                                                                    |
| :--------------------------------------------------------------: | ------------------------------------------------------------------ |
| `\mathsf{\Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta}` | $ \mathsf{\Alpha \Beta \Gamma \Delta \Epsilon \Zeta \Eta \Theta} $ |
|       `\mathsf{\Iota \Kappa \Lambda \Mu \Nu \Xi \Pi \Rho}`       | $ \mathsf{\Iota \Kappa \Lambda \Mu \Nu \Xi \Pi \Rho} $             |
|      `\mathsf{\Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega}`       | $ \mathsf{\Sigma \Tau \Upsilon \Phi \Chi \Psi \Omega} $            |

|      手写体/花体      |                         |
| :-------------------: | ----------------------- |
| `\mathcal{ABCDEFGHI}` | $ \mathcal{ABCDEFGHI} $ |
| `\mathcal{JKLMNOPQR}` | $ \mathcal{JKLMNOPQR} $ |
| `\mathcal{STUVWXYZ}`  | $ \mathcal{STUVWXYZ} $  |

|         Fraktur体          |                              |
| :------------------------: | ---------------------------- |
|   `\mathfrak{ABCDEFGHI}`   | $ \mathfrak{ABCDEFGHI} $     |
|   `\mathfrak{JKLMNOPQR}`   | $ \mathfrak{JKLMNOPQR} $     |
|   `\mathfrak{STUVWXYZ}`    | $ \mathfrak{STUVWXYZ} $      |
| `\mathfrak{abcdefghijklm}` | $ \mathfrak{abcdefghijklm} $ |
| `\mathfrak{nopqrstuvwxyz}` | $ \mathfrak{nopqrstuvwxyz} $ |
|  `\mathfrak{0123456789}`   | $ \mathfrak{0123456789} $    |

|              小型手写体              |                                        |
| :----------------------------------: | -------------------------------------- |
| `{\scriptstyle\text{abcdefghijklm}}` | $ {\scriptstyle\text{abcdefghijklm}} $ |

### 混合字体

|                  特征                   |             语法              |            渲染效果             |
| :-------------------------------------: | :---------------------------: | :-----------------------------: |
|          斜体字符（忽略空格）           |            `x y z`            |            $ x y z $            |
|               非斜体字符                |        `\text{x y z}`         |        $ \text{x y z} $         |
|             混合斜体（差）              | `\text{if} n \text{is even}`  | $ \text{if} n \text{is even} $  |
|             混合斜体（好）              | `\text{if }n\text{ is even}`  | $ \text{if }n\text{ is even} $  |
| 混合斜体（ 替代品：~ 或者"\ "强制空格） | `\text{if}~n\ \text{is even}` | $ \text{if}~n\ \text{is even} $ |

### 括号

|  功能  |            语法            |             显示             |
| :----: | :------------------------: | :--------------------------: |
| 短括号 |      ( \frac{1}{2} )       |      $( \frac{1}{2} )$       |
| 长括号 | \left( \frac{1}{2} \right) | $\left( \frac{1}{2} \right)$ |

### 不同括号

|      功能      |                            语法                            |                             显示                             |
| :------------: | :--------------------------------------------------------: | :----------------------------------------------------------: |
| 圆括号，小括号 |             \left**(** \frac{a}{b} \right**)**             |               $  \left( \frac{a}{b} \right) $                |
| 方括号，中括号 |             \left**[** \frac{a}{b} \right**]**             |               $  \left[ \frac{a}{b} \right] $                |
| 花括号，大括号 |            \left**\{** \frac{a}{b} \right**\}**            |              $  \left\{ \frac{a}{b} \right\} $               |
|     角括号     |      \left **\langle** \frac{a}{b} \right **\rangle**      |        $  \left \langle \frac{a}{b} \right \rangle $         |
| 单竖线，绝对值 |           \left **\|** \frac{a}{b} \right **\|**           |              $  \left\| \frac{a}{b} \right\| $               |
|  双竖线，范数  |           \left **\|** \frac{a}{b} \right **\|**           |             $  \left \| \frac{a}{b} \right \| $              |
|    高斯符号    |      \left **\lbrack** \frac{a}{b} \right **\rbrack**      |        $  \left \lbrack \frac{a}{b} \right \rbrack $         |
|    取底符号    |      \left **\lfloor** \frac{a}{b} \right **\rfloor**      |        $  \left \lfloor \frac{a}{b} \right \rfloor $         |
|    取顶符号    |       \left **\lceil** \frac{c}{d} \right **\rceil**       |         $  \left \lceil \frac{c}{d} \right \rceil $          |
|  斜线与反斜线  |       \left **/** \frac{a}{b} \right **\backslash**        |          $  \left / \frac{a}{b} \right \backslash $          |
|    上下箭头    |    \left **\uparrow** \frac{a}{b} \right **\downarrow**    |      $  \left \uparrow \frac{a}{b} \right \downarrow $       |
|                |    \left **\Uparrow** \frac{a}{b} \right **\Downarrow**    |      $  \left \Uparrow \frac{a}{b} \right \Downarrow $       |
|                | \left **\updownarrow** \frac{a}{b} \right **\Updownarrow** |    $ \left \updownarrow \frac{a}{b} \right \Updownarrow $    |
|    混合括号    |   \left [ 0,1 \right )<br />\left \langle \psi \right \|   | $\left [ 0,1 \right )$ <br />$ \left \langle \psi \right \|  $ |
|    单左括号    |             \left \{ \frac{a}{b} **\right .**              |              $  \left \{ \frac{a}{b} \right . $              |
|    单右括号    |             **\left .** \frac{a}{b} \right \}              |              $  \left . \frac{a}{b} \right \} $              |

> - 可以使用 `\big, \Big, \bigg, \Bigg` 控制括号的大小，比如代码
>
> **\Bigg** ( **\bigg** [ **\Big** \{ **\big** \langle \left | \| \frac{a}{b} \| \right | **\big** \rangle **\Big** \} **\bigg** ] **\Bigg** )
>$$
> \Bigg ( \bigg [ \Big \{ \big \langle \left | \| \frac{a}{b} \| \right | \big \rangle \Big \} \bigg ] \Bigg )
> $$

### 空格

|    功能     |        语法         |         显示          | 宽度  |
| :---------: | :-----------------: | :-------------------: | :---: |
| 2个quad空格 | `\alpha\qquad\beta` | $ \alpha\qquad\beta $ |  2m   |
|  quad空格   | `\alpha\quad\beta`  | $ \alpha\quad\beta $  |   m   |
|   大空格    |   `\alpha\ \beta`   |   $ \alpha\ \beta $   |  m/3  |
|  中等空格   |   `\alpha\;\beta`   |   $ \alpha\;\beta $   | 2m/7  |
|   小空格    |   `\alpha\,\beta`   |   $ \alpha\,\beta $   |  m/6  |
|  没有空格   |    `\alpha\beta`    |    $ \alpha\beta $    |   0   |
|    紧贴     |   `\alpha\!\beta`   |   $ \alpha\!\beta $   | -m/6  |

### 颜色

语法

- 字体颜色︰`{\color{色调}表达式}`
- 背景颜色︰`{\pagecolor{色调}表达式}`

**支持色调表**

|                                            |                                            |                                      |                                                                 |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------ | --------------------------------------------------------------- |
| $ {\color{Apricot}Apricot} $               | $ {\color{Aquamarine}Aquamarine} $         | $ {\color{Bittersweet}Bittersweet} $ | $ {\color{Black}Black} $                                        |
| $ {\color{Blue}Blue} $                     | $ {\color{BlueGreen}BlueGreen} $           | $ {\color{BlueViolet}BlueViolet} $   | $ {\color{BrickRed}BrickRed} $                                  |
| $ {\color{Brown}Brown} $                   | $ {\color{BurntOrange}BurntOrange} $       | $ {\color{CadetBlue}CadetBlue} $     | $ {\color{CarnationPink}CarnationPink} $                        |
| $ {\color{Cerulean}Cerulean} $             | $ {\color{CornflowerBlue}CornflowerBlue} $ | $ {\color{Cyan}Cyan} $               | $ {\color{Dandelion}Dandelion} $                                |
| $ {\color{DarkOrchid}DarkOrchid} $         | $ {\color{Emerald}Emerald} $               | $ {\color{ForestGreen}ForestGreen} $ | $ {\color{Fuchsia}Fuchsia} $                                    |
| $ {\color{Goldenrod}Goldenrod} $           | $ {\color{Gray}Gray} $                     | $ {\color{Green}Green} $             | $ {\color{GreenYellow}GreenYellow} $                            |
| $ {\color{JungleGreen}JungleGreen} $       | $ {\color{Lavender}Lavender} $             | $ {\color{LimeGreen}LimeGreen} $     | $ {\color{Magenta}Magenta} $                                    |
| $ {\color{Mahogany}Mahogany} $             | $ {\color{Maroon}Maroon} $                 | $ {\color{Melon}Melon} $             | $ {\color{MidnightBlue}MidnightBlue} $                          |
| $ {\color{Mulberry}Mulberry} $             | $ {\color{NavyBlue}NavyBlue} $             | $ {\color{OliveGreen}OliveGreen} $   | $ {\color{Orange}Orange} $                                      |
| $ {\color{OrangeRed}OrangeRed} $           | $ {\color{Orchid}Orchid} $                 | $ {\color{Peach}Peach} $             | $ {\color{Periwinkle}Periwinkle} $                              |
| $ {\color{PineGreen}PineGreen} $           | $ {\color{Plum}Plum} $                     | $ {\color{ProcessBlue}ProcessBlue} $ | $ {\color{Purple}Purple} $                                      |
| $ {\color{RawSienna}RawSienna} $           | $ {\color{Red}Red} $                       | $ {\color{RedOrange}RedOrange} $     | $ {\color{RedViolet}RedViolet} $                                |
| $ {\color{Rhodamine}Rhodamine} $           | $ {\color{RoyalBlue}RoyalBlue} $           | $ {\color{RoyalPurple}RoyalPurple} $ | $ {\color{RubineRed}RubineRed} $                                |
| $ {\color{Salmon}Salmon} $                 | $ {\color{SeaGreen}SeaGreen} $             | $ {\color{Sepia}Sepia} $             | $ {\color{SkyBlue}SkyBlue} $                                    |
| $ {\color{SpringGreen}SpringGreen} $       | $ {\color{Tan}Tan} $                       | $ {\color{TealBlue}TealBlue} $       | $ {\color{Thistle}Thistle} $                                    |
| $ {\color{Turquoise}Turquoise} $           | $ {\color{Violet}Violet} $                 | $ {\color{VioletRed}VioletRed} $     | <span style="background:black">$ {\color{White}White} $ </span> |
| $ {\color{WildStrawberry}WildStrawberry} $ | $ {\color{Yellow}Yellow} $                 | $ {\color{YellowGreen}YellowGreen} $ | $ {\color{YellowOrange}YellowOrange} $                          |

> 例子：
> - `{\color{Blue}x^2}+{\color{Brown}2x} - {\color{OliveGreen}1}`
>   $$
>   {\color{Blue}x^2}+{\color{Brown}2x} - {\color{OliveGreen}1}
>   $$
>   
>
> - `x_{\color{Maroon}1,2}=\frac{-b\pm\sqrt{{\color{Maroon}b^2-4ac}}}{2a}`
>   $$
>   x_{\color{Maroon}1,2}=\frac{-b\pm\sqrt{ {\color{Maroon}b^2-4ac}}}{2a}
>   $$
