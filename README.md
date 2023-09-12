# 课前须知
> 评分细则:
跟信息论的相同，上课本前7章，期末60，作业32，迟交2分，满分4分，做了按时交最少3.5分，点名8分。

> [课程主页](https://faculty.ustc.edu.cn/flowice/zh_CN/zdylm/679091/list/index.htm):
https://faculty.ustc.edu.cn/flowice/zh_CN/zdylm/679091/list/index.htm

# 第一章 基础:逻辑与证明

## 1.1命题逻辑

### 罗素悖论
- 将集合分成两类,一类是集合A本身是A的一个元素, 即A∈A,另一类是集合A本身不是A的一个元素, 即A∉A。
- 现构造一个集合S:
- S={A|A∉A}也就是说S是由满足条件A∉A的那些A组成的一个新的集合。
- 我们要问:S是不是它自己的一个元素? 即S∈S,还是S∉S。
- 既不是S∈S,也不是S∉S, 这个悖论就是著名的罗素悖论。

### 命题（Proposition）
命题：是一个或真或假的陈述语句，但不能既真又假。
> 以下不是命题:（可判断真假的才是命题）
x+1＝2（含有变量无法判断真假），几点了？
仔细读这个。

- 命题变元：命题的字母表示，p, q, r, s, …
- 命题的真值（true value）：真命题的真值用“T”表示，假命题的真值用“F”来表示
- 命题逻辑（propositional logic）或命题演算（propositional calculus）：涉及命题的逻辑领域。

### 命题的否定
> 命题的否定（negation）：令p为一命题，则语句“不是p所说的情形”是另一个命题，称为p的否定，用“┐p”表示。命题“┐p”读为“非p”。

### 真值表和运算符
> 真值表（truth table）给出了命题真值之间的关系。

<div align="center">
 <table>
   <thead>
     <tr>
       <th>p</th>
       <th>¬p</th>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td>T</td>
       <td>F</td>
     </tr>
     <tr>
       <td>F</td>
       <td>T</td>
     </tr>
   </tbody>
 </table>
</div>

- 运算符（operator）可以从已有命题构造新命题。有时可称为联接词（connective）。
- 非运算符： ┐
- 原子命题（ Atomic Proposition ）：不含逻辑运算符的命题，不可拆分<span id="yuanzimingti"></span>
- 复合命题（Compositional Proposition） ：用逻辑运算符组合命题构造出的新命题

### 合取（conjunction）
> 令p和q为命题。用p∧q表示这样一个命题：当p和q均为真命题时它为真，否则为假。命题p∧q称为p和q的合取。
注:***理解为集合运算交运算，有一个为假就为假*** 。

<div align="center">
 <table>
  <thead>
    <tr>
      <th>p</th>
      <th>q</th>
      <th>p∧q</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>T</td>
      <td>T</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>T</td>
      <td>F</td>
    </tr>
    <tr>
      <td>T</td>
      <td>F</td>
      <td>F</td>
    </tr>
    <tr>
      <td>F</td>
      <td>F</td>
      <td>F</td>
    </tr>
  </tbody>
</table>
</div>

### 析取（disjunction）
> 令p和q为命题。用p∨q表示这样一个命题：当p和q均为假命题时它为假，否则为真。命题p∨q称为p和q的析取。
***注意:理解为同或或者集合中的并运算，有一个为真就为真***

<div align="center">
 <table>
  <thead>
    <tr>
      <th>p</th>
      <th>q</th>
      <th>p∨q</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>T</td>
      <td>T</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>T</td>
      <td>T</td>
    </tr>
    <tr>
      <td>T</td>
      <td>F</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>F</td>
      <td>F</td>
    </tr>
  </tbody>
</table>
</div>

### 异或（exclusive or）
> 令p和q为命题。p和q的异或，用p⊕q表示，是这样一个命题：当p和q中恰有一个为真时它为真，否则为假。

<div align="center">
 <table>
  <thead>
    <tr>
      <th>p</th>
      <th>q</th>
      <th>p⊕q</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>T</td>
      <td>T</td>
      <td>F</td>
    </tr>
    <tr>
      <td>F</td>
      <td>T</td>
      <td>T</td>
    </tr>
    <tr>
      <td>T</td>
      <td>F</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>F</td>
      <td>F</td>
    </tr>
  </tbody>
</table>
</div>

### 蕴含（implication）
> 令p和q为命题。蕴含p→q是这样一个命题：当p为真而q为假时它为假，否则为真。p称为假设（或前提，前项），q称为结论（或推论）。一个蕴含有时也称为条件语句（conditional statement）
> >  ***注意：只有在p为真而q为假时， p→q才为假。如果p为假，则不管q的真值是什么， p→q都为真。***

<div align="center">
 <table>
  <thead>
    <tr>
      <th>p</th>
      <th>q</th>
      <th>p→q</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>T</td>
      <td>T</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>T</td>
      <td>F</td>
    </tr>
    <tr>
      <td>T</td>
      <td>F</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>F</td>
      <td>T</td>
    </tr>
  </tbody>
</table>
</div>

> 计算机语言“if then”和蕴含的区别“if 2+2=4 then x:=x+1”不是蕴含，因为包含未知参数，所以两个语句都不是命题，从而不是蕴含。

#### 蕴含的逆、倒置和反
- 蕴含： p→q
- 逆蕴含（converse implication）： q→p
- 倒置蕴含（contrapositive implication）: ┐q→ ┐p
- 反蕴含（inverse implication）： ┐p→ ┐q
  > 倒置蕴含和蕴含有相同的真值
  > 
  > 逆蕴含和反蕴含有相同的真值，但与蕴含的真值不同
- 等价（equivalent）：两个复合命题总是具有相同的真值时，我们称这两个命题等价

### 双蕴含（bi-imiplication）
> 令p和q为命题。双蕴含p↔q是这样一个命题：当p和q具有相同真值时它为真，否则为假。一个双蕴含有时也称为双条件语句（biconditional statement），可理解为p为q的充要条件。
> > ***可理解为异或的反取***

<div align="center">
 <table>
  <thead>
    <tr>
      <th>p</th>
      <th>q</th>
      <th>p↔q</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>T</td>
      <td>T</td>
      <td>T</td>
    </tr>
    <tr>
      <td>F</td>
      <td>T</td>
      <td>F</td>
    </tr>
    <tr>
      <td>T</td>
      <td>F</td>
      <td>F</td>
    </tr>
    <tr>
      <td>F</td>
      <td>F</td>
      <td>T</td>
    </tr>
  </tbody>
</table>
</div>

#### 双蕴含的含义
- 双蕴含p↔q恰在p→q和q→p均为真时为真。我们常用术语“p当且仅当q”来表示这一双蕴含。
- p↔q与(p→q) ∧(q→p)有完全相同的真值。
  > “当且仅当”结构在自然语言中很少使用，我们一般用相对简单的结构来表示。比如说，“你吃完饭才可以吃甜点”。双蕴含的部分含义是隐含的，这就造成了在有些情况下，自然语言的不精确性。而在数学上，双蕴含和单蕴含是有明确区分的。~~可能双蕴含在自然语言中是只有才，单蕴含是如果就~~
- 自然语言和逻辑的区别
  > 逻辑：p↔q= q↔p
  > 自然语言：不一定。如p：吃完饭；q：可以吃甜点

### 逻辑运算符的优先级

<div align="center">
 <table>
  <thead>
    <tr>
      <th>运算符</th>
      <th>优先等级</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>┐</td>
      <td>1</td>
    </tr>
    <tr>
      <td>∧</td>
      <td>2</td>
    </tr>
    <tr>
      <td>∨</td>
      <td>3</td>
    </tr>
    <tr>
      <td>→</td>
      <td>4</td>
    </tr>
    <tr>
      <td>↔</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>

***注:在容易混淆的情况下，尽量使用括号 。***

## 1.2命题逻辑的应用

### 逻辑运算和位运算
> - 计算机用字位（bit）来表示信息，每个字位有两个可能的值：0或1（0为F，1为T）；
> - 用字位来表示真值
> - 布尔变量（Boolean variable）
> - 字位运算（bit operation）：对应逻辑联接词
> - 位串（bit string）：0个或多个字位的序列，位串的长度就是它所含字位的个数；
> - 长度相同的两个位串的按位（bitwise）运算：运算结果的每个字位均由北运算的两个位串地对应字位经运算得到
> > 对于按位运算:
> > XOR为异或运算，两者有一个为1时，该位所得值为1，其他时候为0
> > OR为同或运算，两者全为0时，该位所得值为0，其他时候为1
> > AND为和运算，两者全为1时，该为值为1，其他时候为0
> > > ***需要注意的是按位运算的规则与二进制算法不太一样，按照上述异或，同或和合取时候的真值表来理解更好***

### 命题逻辑的应用-翻译语言的句子
- 由于语言的二义性，需要把句子译成逻辑表达式以消除
歧义，有时需要在句子含义基础上做一些合理的假设
  > 例1:“只有你主修计算机科学或不是新生，才可以从校园网访问因特网”
  > 
  >  a：你从校园网访问因特网；
  > 
  >  c：你主修计算机科学；
  >
  > f：你是一个新生；
  > 
  > a↔(c ∨ ┐f)
  > 
  > 例2:“除非你已满16周岁，否则只要你身高不足4英尺就不能乘公园滑行铁道游乐车”
  > 
  > q：你能乘公园滑行铁道游乐车；
  > 
  > r：你身高不足4英尺；
  >
  > s：你已满16周岁；
  > 
  > (r ∧ ┐s)→┐q

### 系统规范说明（~~感觉不重要~~）

- 在说明硬件系统和软件系统时，把自然语言语句翻译成逻辑表达式是很重要的一部分。这些说明可以作为系统开发的基础。
- 系统规范说明不应该存在冲突，因此，表示这些规范说明的命题表达式应该是一致的。
- 也就是说，对表达式中的各个变量，必然有一个真值赋值使所有表达式为真。（自洽的）

### bool搜索和逻辑电路（略）

## 1.3 命题等价

- 永真式（tautology，重言式）：无论其中出现的原子命题的真值是什么，复合命题的真值永远是真；
- 矛盾（contradiction）：真值永远为假的复合题；
- 可能式（contingency）：既不是永真式，又不是矛盾的命题。
例:`p∨┐p` 为永真式，`p∧┐p` 为矛盾。

<div align="center">
 <table>
  <thead>
    <tr>
      <th>p</th>
      <th>┐p</th>
      <th>p∨┐p</th>
      <th>p∧┐p</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>T</td>
      <td>F</td>
      <td>T</td>
      <td>F</td>
    </tr>
    <tr>
      <td>F</td>
      <td>T</td>
      <td>T</td>
      <td>F</td>
    </tr>
  </tbody>
</table>
</div>

### 重言式的性质

- 任何两个重言式的合取、析取、蕴含或双蕴含，仍然是一个重言式。（两个为真命题上述运算也全为真，**矛盾没有该性质**）
   > - [x] 由简单的重言式可构造出复杂的重言式
   > - [x] 由重言式使用公认的规则可以产生许多有用等价式和蕴含式
- 一个重言式，对同一[原子命题](#yuanzimingti)都用任何原子命题/复合命题置换，其结果仍为一重言式。（可以理解为用一个符合命题或者一个单独命题替换掉原有重言式中的某个单独子命题，但是不能替换原有重言式中的某个复合命题）
  > - [x] 置换时被替换的是原子命题，而不能是整个复合命题；
  > - [x] 置换时必须对同一原子命题处处替换以同一公式；
  > > - 例如：可用(r∨s)来替换(p∨¬p)∨q中的p，结果仍是重言式；
  > > - 但若用(r∨s)替换(p∨¬p)；则不能保持重言式；用(r∨s)只替换一处p得到的(r∨s)∨¬p∨q也不是重言式
- 对于矛盾式也有类似的性质

###  逻辑等价（logical equivalences)

#### 定义
- 如果p↔q是永真式，命题p和q称为是逻辑等价的，用记号p≡q来表示，有时也用p⇔q来表示；
  > - [x] p⇔q与p↔q是两个概念（前者表示两个命题之间的关系，后者是一个命题，有对应真值）；
  > - [x] 判定两个命题是否等价：使用真值表（其实这个在推不出来，并且在原子命题数少时非常好用，比如证明p∨(q∧r) ≡ (p∨q)∧(p∨r)时可以用）
  > > - [ ] 涉及n个原子命题的复合命题，需要2n行
  > > - [ ] 当n较大时，真值表方法行不通
  > - [x] 判定两个命题是否等价：使用已建立的等价关系来构造其他等价关系
  > > - [ ] 复合命题中的一个命题可以用与它逻辑等价的命题替换，而不改变复合命题的真值（***注:此时的命题替换与重言式中的命题置换不一样***）
  > - [x] 德摩根定律： ┐(p∨q) ≡ ┐p∧┐q

<div align="center">
  <table>
   <thead>
     <tr>
       <th>p</th>
       <th>q</th>
       <th>p∨q</th>
       <th>┐(p∨q)</th>
       <th>┐p</th>
       <th>┐q</th>
       <th>┐p∧┐q</th>
     </tr>
   </thead>
   <tbody>
     <tr>
       <td>T</td>
       <td>T</td>
       <td>T</td>
       <td>F</td>
       <td>F</td>
       <td>F</td>
       <td>F</td>
     </tr>
     <tr>
       <td>T</td>
       <td>F</td>
       <td>T</td>
       <td>F</td>
       <td>F</td>
       <td>T</td>
       <td>F</td>
     </tr>
     <tr>
       <td>F</td>
       <td>T</td>
       <td>T</td>
       <td>F</td>
       <td>T</td>
       <td>F</td>
       <td>F</td>
     </tr>
     <tr>
       <td>F</td>
       <td>F</td>
       <td>F</td>
       <td>T</td>
       <td>T</td>
       <td>T</td>
       <td>T</td>
     </tr>
   </tbody>
 </table>
</div>

#### 重要的等价关系（很重要）
> ***注:以下表中的等价关系是可以直接用不用推导的，其他的需要自行推导***

> ***从下面的表格不难看出来，五种基本运算符（合取，析取，否定，蕴含，双蕴含）之间是可以互相表示的，且每一种运算符最少要用2种其他的运算符表示。***

##### 等价表
<div align="center">
  <h6><strong>逻辑等价式</strong></h6>
  <table>
  <thead>
    <tr>
      <th>等价式</th>
      <th>名称</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>p∧T≡p<br>p∨F≡p</td>
      <td>恒等律</td>
    </tr>
    <tr>
      <td>p∨T≡T<br>p∧F≡F</td>
      <td>支配律</td>
    </tr>
    <tr>
      <td>p∨p≡p<br>p∧p≡p</td>
      <td>幂等律</td>
    </tr>
    <tr>
      <td>┐(┐p)≡p</td>
      <td>双重否定律</td>
    </tr>
    <tr>
      <td>p∨q≡q∨p<br>p∧q≡q∧p</td>
      <td>交换律</td>
    </tr>
    <tr>
      <td>(p∨q)∨r≡p∨(q∨r)<br>(p∧q)∧r≡p∧(q∧r)</td>
      <td>结合律</td>
    </tr>
    <tr>
      <td>p∨(q∧r)≡(p∨q)∧(p∨r)<br>p∧(q∨r)≡(p∧q)∨(p∧r)</td>
      <td>分配律</td>
    </tr>
    <tr>
      <td>┐(p∧q)≡┑p∨┑q<br>┐(p∨q)≡┑p∧┑q</td>
      <td>德·摩根律</td>
    </tr>
    <tr>
      <td>p∨(p∧q)≡p<br>p∧(p∨q)≡p</td>
      <td>吸收律</td>
    </tr>
    <tr>
      <td>p∨┑p≡T<br>p∧┑p≡F</td>
      <td>否定律</td>
    </tr>
  </tbody>
</table>
 <h6><strong>条件命题的逻辑等价式</strong></h6>
 <table>
  <thead>
    <tr>
      <th>逻辑等价式</th>
      <th>常用程度</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>p→q≡┑p∨q</td>
      <td>✔</td>
    </tr>
    <tr>
      <td>p→q≡┑q→┑p</td>
      <td>✔✔✔</td>
    </tr>
    <tr>
      <td>p∨q≡┑p→q</td>
      <td>✔</td>
    </tr>
    <tr>
      <td>p∧q≡┑(p→┑q)</td>
      <td>✔</td>
    </tr>
    <tr>
      <td>┑(p→q)≡p∧┑q</td>
      <td>✔</td>
    </tr>
    <tr>
      <td>┑(p→q)≡p∧┑q</td>
      <td>✔</td>
    </tr>
    <tr>
      <td>(p→q)∧(p→r)≡p→(q∧r)</td>
      <td>✔✔</td>
    </tr>
    <tr>
      <td>(p→r)∧(q→r)≡(p∨q)→r</td>
      <td>✔✔</td>
    </tr>
    <tr>
      <td>(p→q)∨(p→r)≡p→(q∨r)</td>
      <td>✔✔</td>
    </tr>
    <tr>
      <td>(p→r)∨(q→r)≡(p∧q)→r</td>
      <td>✔✔</td>
    </tr>
  </tbody>
</table>
<h6><strong>双条件命题的逻辑等价式</strong></h6>
 <table>
  <thead>
    <tr>
      <th>逻辑等价式</th>
      <th>常用程度</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>p↔q≡(p→q)∧(q→p)</td>
      <td>✔✔✔</td>
    </tr>
    <tr>
      <td>p↔q≡┑p↔┑q</td>
      <td>✔✔</td>
    </tr>
    <tr>
      <td>p↔q≡(p∧q)∨(┑q∧┑p)</td>
      <td>✔✔</td>
    </tr>
    <tr>
      <td>┑(p↔q)≡p↔┑q</td>
      <td>✔✔</td>
    </tr>
  </tbody>
</table>
</div>

#####  德·摩根律的扩展

$$┑(p_1 ∨ p_2 ∨...∨p_n)≡(┑p_1 ∧┑ p_2 ∧...∧┑p_n)$$

$$┑(p_1 ∧ p_2 ∧...∧p_n)≡(┑p_1 ∨┑ p_2 ∨...∨┑p_n)$$

$$\begin{equation}
\begin{aligned}
\lnot(\bigvee^n_{i=1} p_i) &\equiv \bigwedge^n_{i=1} \lnot p_i 
\end{aligned}
\end{equation}$$

$$\begin{equation}
\begin{aligned}
\lnot(\bigwedge^n_{i=1} p_i) &\equiv \bigvee^n_{i=1} \lnot p_i
\end{aligned}
\end{equation}$$

<!--\begin{equation}：这是LaTeX中用于创建数学公式块的命令。它使公式以单独的行内显示，并附带一个自动编号。

\begin{aligned}：这是LaTeX中用于创建多行数学公式的环境。在这个环境中，可以使用&来对齐公式中的不同部分，并且可以使用\\来分隔不同的行。

\lnot：这是LaTeX中用于表示逻辑非（not）的符号。

\bigvee：这是LaTeX中用于表示逻辑或（logical OR）的符号，其中\big用于显示大的逻辑运算符。

\bigwedge：这是LaTeX中用于表示逻辑与（logical AND）的符号，同样，\big用于显示大的逻辑运算符。

\equiv：这是LaTeX中用于表示逻辑等价（logical equivalence）的符号，表示左侧和右侧的表达式是等价的。-->

### 逻辑等价的性质，和数学中等号性质类似

#### 性质
1. 自反性： p⇔p
2. 对称性： 若p⇔q，则q⇔p
3. 传递性：若p⇔q， q⇔r，则p⇔r

#### 判定两个命题是否等价（考点）
- 使用已建立的等价关系来构造其他等价关系
  > 证明┐(p∨(┐p∧q) ≡ ┐p∧┐q
  >
  > 证明过程:
  > ┐(p∨(┐p∧q)⇔┐p∧┐(┐p∧q)⇔┐p∧(p∨┐q)⇔(┐p∧p)∨(┐p∧┐q)⇔F∨(┐p∧┐q)⇔┐p∧┐q

  > 证明 (p∧q)→(p∨q)为永真式
  >
  > ***思路:即证明等价为T***
  > 
  > 证明过程:
  > 
  > (p∧q)→(p∨q)⇔┐(p∧q)∨(p∨q)⇔(┐p∨┐q)∨(p∨q)⇔(p∨┐p)∨(q∨┐q)⇔T∨T⇔T

### 命题的可满足性
- 一个复合命题称为可满足的：如果存在一个对其变元的
真值赋值使其为真（永真式+可能式）
  > 判断可满足性
  > - [x] 真值表
  > - [x] 是否逻辑等价于矛盾式
  > - [x] 逻辑推理

#### 数独求解
- [ ] 命题p(i,j,n)：当数n位于第i行第j列的单元时为真
- [ ] 数独的解需满足（以下所有的合取）：
  > - [x] 已知数对应单元的p(i,j,n)为真，如p(1,7,4)
  > - [x] 每一行包含了每一个数 $\bigwedge\limits^9_{i=1}  \bigwedge\limits^9_{n=1}  \bigvee\limits^9_{j=1} p(i,j,n)$
  > - [x] 每一列包含了每一个数 $\bigwedge\limits^9_{j=1}  \bigwedge\limits^9_{n=1}  \bigvee\limits^9_{i=1} p(i,j,n)$
  > - [x] 每一个九宫格包含了每一个数 $\bigwedge\limits^2_{r=0}  \bigwedge\limits^2_{s=1} \bigwedge\limits^9_{n=1} \bigvee\limits^9_{i=1} \bigvee\limits^9_{j=1} p(3r+i,3s+j,n)$
  > - [x] 没有一个单元包含多余一个数 $p(i,j,n)→\lnot p(3r+i,3s+j,n)$

## 1.4 谓词和量词

### 谓词

#### 定义

- 简单认为是用于判断性质的语句或者符号，比如“是”，“>”等。

#### 命题函数

- 含变量的语句，在变量值未知时，语句既不为真，也不为假：“x>3”，“x=y+3”，“x+y=z”
- 命题函数（propositional function）：谓词（predicate）和变量的组合，一般用大写英文表示，与命题（小写字母）区分开，当命题函数中的未知参数赋值以后就是命题，可以判断其真值。
- $P(x_1, x_2, …, x_n)$ 表示命题函数P在n元组（n-tupie） $(x_1, x_2, …, x_n)$ 的值，P也称为谓词，用来描述个体的属性以及个体之间的关系；
  > P(x)：x>3
  >
  > Q(x,y)：x=y+3
  >
  > R(x,y,z)：x+y=z

### 量词
#### 定义
- 量化（quatification）：从命题函数产生命题
  > - 全称量化∀ （universal quatification）：Any首字母的倒写
  > - 存在量化∃ （existential quatification）：Exist首字母的反写
- 谓词演算（predicate calculus）：与谓词和量词相关的逻辑领域
- 论域（domain of discourse）：命题函数中变量的定义域

### 全称量化

#### 定义

- P(x)的全称量化是命题“P(x)对x在其论域的所有值为真”，记为∀xP(x)。其中∀称为全称量词。
- 命题∀xP(x)表示为“对所有x，P(x)”或“对每个x，P(x)”。
   > 当论域中的所有元素可以一一列出时 $∀xP(x) ≡ P(x_1)∧P(x_2)∧…∧P(x_n)$
   
   > 使用量词时，论域是很重要的
   
   > 反例（counterexample）：论域中使P(x)为假的x的取值

#### 举例
> P(x)：x+1>x 
> 
> 论域：实数集合
> 
> ∀xP(x)=T
> 
> P(x)：x2>0
> 
> 论域：整数
> 
> 反例：x=0

### 存在量化

#### 定义

- P(x)的存在量化是命题“论域中存在一个元素x使P(x)为真”，记为∃xP(x)。其中∃称为存在量词。（存在一个但也可以不止一个）
- 命题∃xP(x)表示为“有一个x使得P(x)”或“对某个x，P(x)”。
   > 当论域中的所有元素可以一一列出时 $∃xP(x) ≡ P(x_1)∨P(x_2)∨….∨P(x_n)$
   > 
   > 使用量词时，论域是很重要的

#### 举例
> P(x)：x>3
>
> 论域：实数集合
> 
> ∃xP(x)=T

### 量词总结
<div align="center">
 <table>
  <thead>
    <tr>
      <th>语句</th>
      <th>何时为真?</th>
      <th>何时为假?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>∀xP(x)</td>
      <td>对每一个x，P(x)都为真</td>
      <td>有一个x，使P(x)都为假</td>
    </tr>
    <tr>
      <td>∃xP(x)</td>
      <td>有一个x，使P(x)都为真</td>
      <td>对每一个x，P(x)都为假</td>
    </tr>
  </tbody>
</table>
</div>

- 唯一性量词（∃!或 $∃_1$ ）：存在唯一的x使P(x)为真
  > ∃!xP(x)
- 量词的优先级：高于合取/析取等逻辑运算符
  > ∃xP(x)∧Q(x)=(∃xP(x))∧Q(x)

### 绑定变量

- 当量词作用于变量x或给这一变量赋值时，我们说此变量的这一次出现为 ___绑定（bound）___ 的；
- 没有被量词绑定或设置为与某一特定值相等的变量出现为 ___自由（free）___ 的；
  > - [x] 出现在命题函数中的所有变量必须通过绑定，才能把此命题函数转变成命题
- 逻辑表达式中应用量词的部分称为这个量词的 ___作用域（scope）___。
  > - [x] 判定一个变量是否自由：在指定这个变量的公式中，变量在所有量词的作用域之外
  > > 例子：∃xQ(x,y) ∃x(P(x)∧Q(x))∨∀xR(x)(此时前后两个x变量的作用域不一样)
  > - [x] ___只要作用域不重叠，相同的字母可以用于表示被不同量词绑定的变量___

### 量词的否定

- 全称量词的否定
  > 例子
  > 
  > P(x)：x学过一门微积分课
  > 
  > 论域：全班学生
  > 
  > ∀xP(x)：班上每个学生都学过一门微积分课
  > 
  > ┐(∀xP(x))：并非班上每个学生都学过一门微积分课
  > 
  > ∃x┐P(x)：班上有个学生没有学过微积分课
  > 
  > ┐(∀xP(x))≡ ∃x┐P(x)

<div align="center" id="not">
 <h6><strong>量词的否定</strong></h6>
 <table>
  <thead>
    <tr>
      <th>否定</th>
      <th>等价语句</th>
      <th>何时为真?</th>
      <th>何时为假?</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>┑∃xP(x)</td>
      <td>∀x┑P(x)</td>
      <td>对每个x，P(x)都为假</td>
      <td>有x，使P(x)都为真</td>
    </tr>
    <tr>
      <td>┑∀xP(x)</td>
      <td>∃x┑P(x)</td>
      <td>有x，使P(x)都为假</td>
      <td>对每个x，P(x)都为真</td>
    </tr>
  </tbody>
</table>
</div>

### 涉及量词的逻辑等价(重点考察，易错点)
#### 定义
- 涉及谓词和量词的逻辑等价：当且仅当无论用什么谓词代入这些语句，也无论为这些命题函数里的变量指定什么论域(即变量x所有可以存在的论域，而不是仅限某个论域)，它们都有相同的真值。用S≡T表示。
  > 证明：┑∀x(P(x)→Q(x))和∃x(P(x)∧┑Q(x))是逻辑等价的（始终采用同一个论域）
  >
  > 假设┑∀x(P(x)→Q(x))为假。这说明对于论域中的任何元素x，都满足条件P(x)→Q(x)。接下来证明∃x(P(x)∧┑Q(x))为假，即不存在一个元素x使得P(x)∧┑Q(x)为真。
  >
  > 假设反证法，假设∃x(P(x)∧┑Q(x))为真，即存在元素x使得P(x)∧┑Q(x)为真。然后，使用∀x(P(x)→Q(x))为真的前提来构造一个矛盾。
  >
  > 选择一个特定的元素a，P(a)∧┑Q(a)为真，可知P(a)和┑Q(a)为真，Q(a)为假，由于∀x(P(x)→Q(x))为真，从而得到P(a)必须为假才行。
  >
  > 这导致了矛盾，因此假设∃x(P(x)∧┑Q(x))为真是不正确的。因此，根据反证法的证明，∃x(P(x)∧┑Q(x))为假。
  >
  > 这表明∀x(P(x)→Q(x))和∃x(P(x)∧┑Q(x))之间不存在反例，因此它们是逻辑等价的。

#### 常见的量词的逻辑等价

<div align="center">
 <table>
  <thead>
    <tr>
      <th>量词的逻辑等价</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>∀xP(x) ≡ P(x₁)∧P(x₂)∧…∧P(xₙ)</td>
    </tr>
    <tr>
      <td>∃xP(x) ≡ P(x₁)∨P(x₂)∨…∨P(xₙ)</td>
    </tr>
    <tr>
      <td>∀x(P(x)∧q) ⇔ ∀xP(x)∧q</td>
    </tr>
    <tr>
      <td>∀x(P(x)∨q) ⇔ ∀xP(x)∨q</td>
    </tr>
    <tr>
      <td>∃x(P(x)∧q) ⇔ ∃xP(x)∧q</td>
    </tr>
    <tr>
      <td>∃x(P(x)∨q) ⇔ ∃xP(x)∨q</td>
    </tr>
    <tr>
      <td>∀x(P(x)∧Q(x)) ⇔ ∀xP(x)∧∀xQ(x)</td>
    </tr>
    <tr>
      <td>∃x(P(x)∨Q(x)) ⇔ ∃xP(x)∨∃xQ(x)</td>
    </tr>
  </tbody>
</table>
</div>

> - [x] 为了便于记忆，可以这么理解，由于命题q的真值与x取值没有关系，所以P(x)∧(∨)q对于论域中的任意x而言，其实发生变化的只有P(x)的真值，所以将q提取出来没有问题。
>
> - [x] ***但是考虑以下关系∀x(P(x)→q) ⇔ ∀xP(x)→q，这个是有问题的，假设∀xP(x)为假时，后面的量词命题始终为真，但是有可能存在x=a，使得P(x)为真（∀xP(x)为假不代表不存在x使得P(x)为真）。***
>
> - [x] ***假设q为假，此时P(x)→q为假，说明存在x=a使得P(x)→q为假，故∀x(P(x)→q)为假。这个是矛盾的，所以可证明是有问题的*** 
>
> - [x] 同时由于对于∀x(P(x)∧Q(x))而言，本来是同一个论域中的x变量，P(x)和Q(x)的真值会同时变化，假设对于论域某一个x=a而言，P或Q为假，则前部分命题表达式为假，同时由于为同一个论域，所以a仍在域内，故右边命题也为假。
>
> - [x] 同理也可知当前面这个命题表达式为真时，对于论域中的x，P(x)和Q(x)均为真，所以对于同一论域，后面也为真。
> 
> - [x] ***这个时候考虑关系∀x(P(x)∨Q(x)) ⇔ ∀xP(x)∨∀xQ(x),这个则是有问题的，假设前者表达式为真，则说明对于每一个x而言，P(x)或Q(x)为真，但是此时x不能保证P(x)和Q(x)同时为真。***
>
> - [x] ***假设x=a时，P(x)为真，Q(x)为假，而当x=b时，P(x)为假，Q(x)为真，就算只有这两种情况的特例，其他x都使得P(x)和Q(x)同时为真，这个时候前面的命题为真。***
>
> - [x] ***但是∀xP(x)和∀xQ(x)均为假（分别存在b,a使得P(x)和Q(x)为假），则∀xP(x)∨∀xQ(x)为假，所以两个量词命题是不等价的***
>
> - [x] 同时根据上述解释，可以明白∃x(P(x)∨Q(x)) ⇔ ∃xP(x)∨∃xQ(x)，而 ***∃x(P(x)∧Q(x)) ⇔ ∃xP(x)∧∃xQ(x)有问题，也可以举例类似上述的矛盾，假设前者为假，则没有一个x可以让P(x)∧Q(x)同时为真。***
>
> - [x] ***但是可以存在x=a使得P(x)为真，Q(x)为假，x=b使得P(x)为假，Q(x)为真，所以此时可看出来∃xP(x)和∃xQ(x)均为真（分别存在a,b使得P(x)和Q(x)为真），后面表达式为真。***
>
> - [x] ***从上述不难发现，反证法，取特定值法和假设法在证明该问题时，尤其好用。*** 

### 翻译语句为逻辑表达式
- 例：使用谓词和量词表达语句“班上的每个学生都学过积分课”
 > C(x):x学过微积分课
 >
 > 论域：全班同学
 >
 > ∀xC(x):班上每个学生都学过微积分课
 >
 > 或者
 >
 > Q(x,y):学生x学过课程y
 > 
 > S(x):x是班上的学生
 > 
 > 论域为：所有人，所有课程
 > 
 > ∀x(S(x)→Q(x,微积分))
- 例：
  > P(x):x是只蜂鸟
  >
  > Q(x):x是大的
  >
  > R(x):x以蜜为生
  >
  > S(x):x五彩斑斓
  >
  > 论域:所有鸟
  >
  > 所有蜂鸟都五彩斑斓:∀x(P(x)→S(x))
  >
  > 没有大鸟以蜜为生：┑∃x(Q(x)∧R(x))
  >
  > 不以蜜为生的鸟都色彩单调:∀x(┑R(x)→┑S(x))
  >
  > 蜂鸟都是小鸟:∀x(P(x)→┑Q(x))

## 1.5 嵌套量词
### 嵌套量词(Nested Quantifiers)
> 定义:出现在其他量词的作用域中的量词。
> > 例：
> >
> > ∀x∀y(x+y=y+x)
> >
> > ∀x∃y(x+y=0)
> >
> > ∀x∀y∀z(x+(y+z)=(x+y)+z)
> >
> > ∀x∀y((x>0)∧(y<0)→(xy<0))

### 循环量化思考
#### 定义
> 借助嵌套循环来思考多个变量使用量词的情况。

<div align="center">
 <p align="center"><span>两个变量的量化</span></p>
 <table>
  <tr>
    <th>语句</th>
    <th>何时为真?</th>
    <th>何时为假?</th>
  </tr>
  <tr>
    <td>∀x∀yP(x,y)<br>∀y∀xP(x,y)</td>
    <td>对每一对x,y,P(x,y)均为真</td>
    <td>有一对x,y使得P(x,y)为假</td>
  </tr>
  <tr>
    <td>∀x∃yP(x,y)</td>
    <td>对每个x，都有y使得P(x,y)为真</td>
    <td>有x,使得P(x,y)对于每个y总是假</td>
  </tr>
  <tr>
    <td>∃y∀xP(x,y)</td>
    <td>有一个x,使得P(x,y)对于所有y均为真</td>
    <td>对于每个x都有y使得P(x,y)为假</td>
  </tr>
  <tr>
    <td>∃x∃yP(x,y)<br>∃y∃xP(x,y)</td>
    <td>有一对x,y使得P(x,y)为真</td>
    <td>对每一对x,y,P(x,y)均为假</td>
  </tr>
</table>
</div>

#### 举例
> Q(x,y,z):x+y=z
> 
> 论域：所有实数
> 
> ∀x∀y∃zQ(x,y,z)= T
>
> > 对于所有实数x和所有实数y，有实数z，使得x+y=z
> 
> ∃z∀x∀yQ(x,y,z)= F
>
> > 有实数z使得对所有实数x和所有实数y，x+y=z

### 量词的顺序
> 除非所有量词均为全称量词或存在量词，否则量词的顺序是很重要的。

#### 举例
> P(x,y):x+y=y+x
>
> 论域：所有实数
>
> ∀x∀yP(x,y)= T
>
> Q(x,y):x+y=0
>
> 论域：所有实数
>
> ∃y∀xQ(x,y)= F
>
> > 有个实数y能使Q(x,y)对于每一个实数x成立
>
> ∀x∃yQ(x,y)= T
> > 对每个实数x都有一个实数y使Q(x,y)成立

### 翻译涉及嵌套量词的语句
- [x] 写出表达式中的量词和谓词的含义, ***注意：要分清楚全称量词和存在量词***
- [x] 用简单的句子来表达这个含义

#### 举例
> ∃x∀y∀z((F(x,y)∧F(x,z)∧F(y≠z))→┑F(y,x))
>
> F(a,b):a和b是朋友
>
> 论域：学校中所有的学生
>
> *有个学生，他的朋友之间都不是朋友*

>  将语句“每个人都恰有一个最好的朋友”翻译成逻辑表达式
>
> B(x,y):y是x的最好的朋友
>
> 论域：所有人
>
> x恰有一个最好的朋友意味着有一个人y是x的最好的朋友，而且，对每个人z，若果z不是y，那么z不是x的最好的朋友。
>
> ∀x∃y(B(x,y)∧∀z((z≠y)→┑B(x,z)))

> 将语句“有一个妇女已搭乘过世界上每一条航线上的航班”翻译成逻辑表达式
>
> P(w,f)：w搭乘过f
>
> Q(f,a)：f是a上的航班
>
> 论域：所有妇女，所有航班，所有航线
>
> ∃w∀a∃f(P(w,f)∧Q(f,a))

### 将数学语句翻译成逻辑表达式
#### 举例
> 将语句“两个正整数的和是正数”翻译成逻辑表达式。
>
> x：正整数
>
> y：正整数
>
> 论域：全体整数
>
> ∀x∀y((x>0)∧(y>0)→(x+y>0))

> 将语句“每个实数（除了零）都有乘法逆元”翻译成逻辑表达式。
>
> x：实数，x≠0
>
> 论域：实数
>
> ∀x((x≠0))→∃y(xy=1)

### 否定嵌套量词
#### 定义
> 可以通过连续的应用否定单个量词的规则来否定带嵌套量词的语句
[量词的否定表格见上](#not)

#### 举例
> 使用量词表示语句“没有一个妇女已搭乘过世界上每一条航线上的航班”
> P(w,f)：w搭乘过f
>
> Q(f,a)：f是a上的航班
>
> 论域：所有妇女,所有航班,所有航线
>
> $┑∃w∀a∃f(P(w,f)∧Q(f,a))$
> $\equiv ∀w┑∀a∃f(P(w,f)∧Q(f,a))$
> $\equiv ∀w∃a┑∃f(P(w,f)∧Q(f,a))$
> $\equiv ∀w∃a∀┑f(P(w,f)∧Q(f,a))$
> $\equiv ∀w∃a∀f(┑P(w,f)∨┑Q(f,a))$

## 1.6 推理规则
### 相关定义
- 定理（theorem）：可以被证明为真的命题。
- 证明（proof）：用一系列命题来证明一条定理为真，这些命题就形成一项论证，称为证明。
- 公理（axioms）：或称为公设（postulates），是关于数学结构的基本假设。
- 推理规则（rules of inference）：是从其他断言得出结论所用的方法，用来把证明的各个步骤联系起来。
- 引理（lemma）：在其他定理证明中所用的简单定理。
- 推论（corollary）：从已经证明了的定理直接证实的命题。
- 猜想（conjecture）：真值未知的命题。

### 推理规则
#### 假言推理
> 假言推理（modus ponens）：又称分离规则（law of detachment），以重言式(p∧(p→q))→q为基础的推理规则。假言推理是说，若蕴含式及其前提为真，则这个蕴含式的结论为真。
> > 一般推理过程如下
```math
p为真
p→q为真
∴q为真
```
#### 假言推理的例子
> 例1
> > 假定蕴含式“若今天下雪，则将去滑雪”和它的前件“今天正在下雪”都为真。那么，根据假言推理，得出蕴含式的后件“将去滑雪”为真。

> 例2
> > 蕴含式“若 n被3整除，则n²被9整除”为真。所以，若n被3整除，则根据假言推理得出n²被9整除。

#### 一些基本的推理规则

### 假言三段论的例子
> 一般形如以下形式的论证为是假言三段论(hypothetical syllogism)
```math
p→q
q→r
∴p→r
```
#### 示例
> 说出在下列论证里使用哪个推理规则
> > 若今天下雨，则我们今天将不野餐。若我们今天不野餐，则我们明天将野餐。因此，若今天下雨，则我们明天将野餐。
> > 
> > p:今天下雨
> > 
> > q：我们今天将不野餐
> > 
> > r：我们明天将野餐

### 有效论证
- 若每当所有的前提都为真时，结论也为真，则这样的论证称为有效的。
 - [ ] 设 $p_1, p_2, …, p_n$ 和q是命题，当且仅当为 $(p_1∧p_2∧...∧p_n)→q$ 一重言式，称q为 $p_1, p_2, …, p_n$ 的有效结论，记为 $(p_1 ∧ p_2 ∧ … ∧ p_n)⇒q$ ；
 - [ ] 有效论证强调的是推理的有效性，而不在于结论是否正确：当在有效论证中用到一个或多个假命题时，该论证可能得出不正确的结论；
 - [ ] 当存在许多前提时，为了证明一个论证是有效的，就常常需要多个推理规则。
#### 示例
> 例证明：前提“今天下午没有出太阳并且今天比昨天冷”，“只有今天下午出太阳，我们才将去游泳”，“若我们不去游泳，则我们将乘独木舟游览”，以及“若我们乘独木舟游览，则我们将在黄昏时回家”，导致结论“我们将在黄昏时回家”。
> > p:今天下午出太阳
> >
> > q：今天比昨天冷
> >
> > r：我们将去游泳
> >
> > s：我们将乘独木舟游览
> > 
> > t：我们将在黄昏时回家

### 消解
- [ ] 消解（resolution）：基于以下永真式的推理规则，析取q∨r称为 ***消解式*** （resolvent）。
 - [x] 在计算机程序中经常使用的推理规则；
 - [x] 当r=F时，消解规则成为了析取三段论规则

> 例：使用消解证明假设“Jasmine在滑雪或没有下雪”和“下雪了或Bart在打曲棍球”蕴含结论“Jasmine在滑雪或Bart在打曲棍球。”
> > p:下雪了
> >
> > q: Jasmine在滑雪
> >
> > r: Bart在打曲棍球
> >
> > 假设为： ┐p∨q， p∨r ***消解得到： q∨r***

### 谬误
- [ ] 肯定结论谬误（fallacy of affirming the conclusion）：命题[(p→q)∧q]→p不是重言式。
- [ ] 否定假设谬误（fallacy of denying the hypothesis）：命题[(p→q)∧ ┐p]→ ┐q不是重言式。
> 例：下面的论证是否有效？
>
> 若你做过本书的每一道练习，则你学习过离散数学。
>
> 你学习过离散数学。因此你做过本书的每一道练习。
>
> p:你做过本书的每一道练习
>
> q: 你学习过离散数学
