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
   > 当论域中的所有元素可以一一列出时 $∃xP(x) ≡ P(x_1)∨P(x_2)∨…∨P(x_n)$
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
>
> ~~标注：嵌套量词中的量词要从左到右顺序进行读取。一般这样能得到正确语句。~~
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

<div align="center">
 <p align="center"><span>推理规则</span></p>
 <table>
  <tr>
    <th>推理规则</th>
    <th>永真式</th>
    <th>名称</th>
  </tr>
  <tr>
    <td>p<br>p→q<br>∴q</td>
    <td>(p∧(p→q))→q</td>
    <td>假言推理</td>
  </tr>
  <tr>
    <td>┐q<br>p→q<br>∴┐p</td>
    <td>(┐p∧(p→q)→┐p)</td>
    <td>取拒式</td>
  </tr>
  <tr>
    <td>p→q<br>q→r<br>∴p→r</td>
    <td>((p→q)∧(q→r))→(p→r)</td>
    <td>假言三段论</td>
  </tr>
  <tr>
    <td>p∨q<br>┐q<br>∴q</td>
    <td>((p∨q)∧┐q)→q</td>
    <td>析取三段式</td>
  </tr>
  <tr>
    <td>p<br>∴(p∨q)</td>
    <td>p→(p∨q)(p⇒(p∨q))</td>
    <td>附加律</td>
  </tr>
  <tr>
    <td>p∧q<br>∴p</td>
    <td>(p∧q)→p</td>
    <td>化简律</td>
  </tr>
  <tr>
    <td>p<br>q<br>∴p∧q</td>
    <td>((p)∧(q))→(p∧q)</td>
    <td>合取律</td>
  </tr>
  <tr>
    <td>p∨q<br>┐p∨r<br>∴q∧r</td>
    <td>((p∨q)∧(┐p∨r))→(q∧r)</td>
    <td>消解律</td>
  </tr>
</table>
</div>

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
$$((p∨q)∧(┑p∨r))→(q∨r)$$
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

> 证明:(p∧q)∨r和r→s蕴含结论p∨s

### 谬误
- [ ] 肯定结论谬误（fallacy of affirming the conclusion）：命题[(p→q)∧q]→p不是重言式。
- [ ] 否定假设谬误（fallacy of denying the hypothesis）：命题[(p→q)∧┐p]→┐q不是重言式。
> 例：下面的论证是否有效？
>
> 若你做过本书的每一道练习，则你学习过离散数学。
>
> 你学习过离散数学。因此你做过本书的每一道练习。
>
> p:你做过本书的每一道练习
>
> q: 你学习过离散数学

### 带量词命题的推理规则

<div align="center">
 <table>
  <tr>
    <th>推理规则</th>
    <th>名称</th>
  </tr>
  <tr>
    <td>∀xP(x)<br>∴P(c)</td>
    <td>全称实例</td>
  </tr>
  <tr>
    <td>P(x), 任意c<br>∴∀xP(x)</td>
    <td>全称引入</td>
  </tr>
  <tr>
    <td>∃xP(x)<br>∴P(c), 对某个元素c</td>
    <td>存在实例</td>
  </tr>
  <tr>
    <td>P(c), 对某个元素c<br>∴∃xP(x)</td>
    <td>存在引入</td>
  </tr>
</table>
</div>

> 例1:
> > 证明前提“在这个班上的某个学生没有读过书”和“班上的每个人都通过了第一门考试”蕴含结论“通过考试的某个人没有读过书”。
> > 
> > C(x):x在这个班中
> >
> > B(x):x读过书了
> >
> >  P(x):x通过了第一门考试
> >
> > 论域：所有学生

- 数学论证中常常既使用命题推理规则，又使用量词推理规则。
	- [x] 全称例示和假言推理结合:∀x(P(x)→Q(x))∨P(c) → Q(c)

> 例2:
> > P(x)：x是大学生；Q(x)：x是青年；c：参加大运会的运动员
> > 所有大学生都是青年:∀x(P(x)→Q(x)) ；
> >
> > 参加大运会的运动员是大学生:P(c)；
> >
> > 所以，参加大运会的运动员是青年:Q(c)。

- 全称生成规则在定理证明中，有时候不明确指出。
	- [x] 若a，b是正实数，则a>b推出 $a^2>b^2$ ；

### 使用推理规则的步骤
> 例题：用推理规则证明:如果∀x(P(x)∨Q(x))和∀x(┑Q(x)∨S(x)),∀x(R(x)→┑S(x))和∃x┑P(x)为真，则∃x┑R(x)为真

> 证明如下：
> 1. ∃x┑P(x)(前提引入)
> 2. ┑P(c)(存在实例，由(1))
> 3. ∀x(P(x)∨Q(x))(前提引入)
> 4. P(c)∨Q(c)(全称实例，由(3))
> 5. Q(c)(析取三段式，由(2)(4))
> 6. ∀x(┑Q(x)∨S(x))(前提引入)
> 7. ┑Q(c)∨S(c)(全称实例，由(6))
> 8. S(c)(析取三段式，由(5)(7))
> 9. ∀x(R(x)→┑S(x))(前提引入)
> 10. R(c)→┑S(c)(全称实例，由(9))
> 11. ┑R(c)(取拒式，由(8)(10))
> 12. ∃x┑R(x)(存在引入，由(11))

## 1.7 证明导论

### 证明定理的方法
- [x] 直接证明（direct proof）
- [x] 间接证明（proof by contraposition）
- [x] 空证明（vacuous proof）
- [x] 平凡证明（trivial proof）
- [x] 归谬证明（proof by contradiction）
- [x] 分情形证
- [x] 等价性证明（proof of equivalence）
### 直接证明
- [x] 直接证明：通过证明若p为真则q也必然为真，来证明蕴含式p→q为真；

> 例：整数n是偶数，如果存在一个整数k是的n=2k；整数n是奇数，如果存在一个整数k是的n=2k+1。

> 例：给出定理“若n是奇数，则n2是奇数”的直接证明

### 间接证明（反证法）
- [x] 间接证明：通过证明逆否命题┐q→┐p ，来证明蕴含式p→q；
 
> 例：给出定理“若3n+2是奇数，则n是奇数”的间接证明

### 空证明和平凡证明
- [x] 空证明：通过证明p为假，来证明蕴含式p→q为真；
	- [ ] 主要用于证明一些定理的特殊情况 
 
> 例：证明命题P(0)为真，其中P(n)是命题函数“ $若n>1，则n^2>n$ ”

- [x] 平凡证明：通过证明q为真，来证明蕴含式p→q为真；
	- [ ] 主要用于证明定理的特殊情形以及数学归纳法中
 
> 例：设P(n)是命题“若a和b是满足的a≥b的正整数，则 $a^n ≥b^n$ ”。证明P(0)为真。

### 归谬证明(类似反证法，但是一般在没有给出条件时证明结论的时候使用)
- [x] 归谬证明：假定可以找到矛盾式q（比如q=r∧┐r）使得┐p→q为真，即┐p→F为真，则命题┐p必然为假，所以p必然为真。
 
> 例：通过给出归谬证明来证明 $\sqrt{2}$ 是无理数。
> > 实数r是有理数，若存在整数p和q(q≠0,p,q互质)使得r=p/q。不是有理数的实数称为无理数。
> > 
> > 假设 $\sqrt{2}$ 为有理数则存在 $\sqrt{2}=\frac{p}{q}$ ,所以有 $2q^2=p^2$ ，此时说明p和q不互质，矛盾。

> 例：证明如果n是整数且 $n^3+5$ 为奇数，则n为偶数，用归谬法证明
> > 假设n和 $n^3+5$ 为奇数，则可知 $n^3$ 为奇数，所以5为偶数，显然矛盾。

> ***~~从这里不难看出，归谬法和反证法的本质区别为，反证法是假设结论错误，推条件矛盾，而归谬法是假设结论错误，且条件正确，推出与某个公理相悖的矛盾。~~***

### 等价性证明
- [x] 等价性证明：为了证明形如p↔q的命题，可以使用重言式 $(p↔q)↔[(p→q)∧(q→p)]$ ，若需证明多个命题等价，则可使用重言式 $$[p_1↔p_2↔...↔p_n]↔[(p_1↔p_2)∧(p_2↔p_3)∧...∧(p_n↔p_1)]$$

> 证明下列三个命题等价：
> > $p_1$ :n是偶数， $p_2$ : n-1是奇数， $p_3$ : $n^2$ 是偶数

### 反例
- [x] 反例：一般用于证明形如∀xP(x)的语句为假。

> 例：证明语句“灭国正整数都是三个整数的平方和”为假
> > 解：如果能找到一个反例，使能证明此语句为假，要寻找反例，我们试着写出可满足语句条件的连续的正整数。可以发现7得不到这样的拆分，所以为假。

- [x] 无论存在多少个使P(x)为真的特例， ∀xP(x)的语句仍可能为假

### 证明中的错误(略)

## 1.8 证明方法和策略
### 分情形证明
- [x] 分情形证明：为了证明蕴含式 $(p_1∨p_2∨… ∨p_n) →q$ ，使用以下重言式来作为推理规则 $$[(p_1∨p_2∨...∨p_n)→q]↔[(p_1→q)∧(p_2→q)∧...∧(p_n→q)]$$

> 一般证明分段或分情况讨论时使用

#### 分情形帮助证明
- [x] 分情形证明：当没有明显方式可以开始证明，而分情形后，每种情形的额外信息可以帮助证明时。
	> 绝对值：负数，非负数
	> 被n整除：nk,nk+1,…,nk+n-1

> 例：证明：如果n是不能被2或3整除的整数，则 $n^2-1$ 能被24整除。
> > 分为n=6k+1,6k+5的情况证明(最好将所有情形列举出来再筛选，此处为省略情况)
>
> 证明： $x^2+3y^2=8$ 没有整数解x和y。
> > 定x和y的取值范围，进行穷举就可以

#### 证明中的错误(略)
> ***注意：在分情形证明时，一定要将所有情形列举出来！***

### 定理和量词 
#### 存在性证明
- [x] 存在性证明：形如∃xP(x)的命题的证明。
	> 构造性的存在性证明：通过找出一个使得P(a)为真的元素a来证明

> 例：证明存在某个正整数，可以用两种不同的方法将其表示为正整数的立方和。
> > $1729=10^3+9^3=12^3+1^3$

> 非构造性的存在性证明：通过其它方法来证明，也就是不用找出具体的实例，只用证明存在就可以

> 例：证明存在无理数x和y使得 $x^y$ 是有理数
> > 证明，假设 $\sqrt{2}^{\sqrt{2}}$ 分两种情况，为有理数和为无理数，若为有理数则得证，如果为无理数，则考虑 $(\sqrt{2}^{\sqrt{2}})^{\sqrt{2}}$ 可知 $\sqrt{2}$ 和 $\sqrt{2}^{\sqrt{2}}$ 均为无理数，但是 $(\sqrt{2}^{\sqrt{2}})^{\sqrt{2}}$ 为有理数2，得证。

#### 唯一性证明
- [x] 唯一性证明：证明具有特定性质的元素唯一存在。即证明∃x(P(x)∧∀y(y≠x→┐P(y)))。
> 例：证明每个整数都有一个唯一的加逆性。也就是证明，如果P是整数，那么存在一个唯一的整数q使得p+q=0

### 证明策略
- [x] 蕴含式的证明：先尝试直接证明，再尝试间接证明，然后尝试归缪证明。
- [x] 前推：从一个起点开始，利用公理和已知定理，用导向结论的一系列步骤来构造证明。
- [x] 后推：为了证明命题q，就寻找能证明具有性质p→q的命题p。
	- [ ] 寻找能证明使得q→r的r不会有帮助
 	- [ ] ***一定不能从结果证明结果，即不能先假定结论为真，再推结论为真。*** 

> 例:给定两个正实数a和b，其算术均值是(a+b)/2，几何均值是 $\sqrt{ab}$ ，证明算术均值总是大于几何均值。
> > 用均值不等式逆推

### 修改现存证明
> 证明：存在无穷多个形如4k+3的素数，其中k是非负整数。
> > 相似问题证明：假设只存在有穷多个素数 $p_1,p_2,···,p_n$ ，并且构造出数 $p_1,p_2,···,p_n+!$。这个数要么是素数，要么具有与素数 $p_1,p_2,···,p_n$ 中每个都不同的素因子，于是证明了无穷多个素数。

> 本问题的证明：假设只存在有穷多个形如4k+3的素数，即 $q_1,q_2, ···,q_n$ ，构造 $Q=4q_1q_2...q_n-1$ 即可，不能构造 $$Q=4q_1q_2...q_n+3$ 虽然它们形式上都为4k+3形式，但是后者属于是可能被3整除，所以不可行。构造后 $Q=4q_1q_2...q_n-1$ 可能有4k+1形式的素因子，但是不能全是4k+1类的素因子，但是其不能被已经罗列的4k+3形式的素因子整除，故得证。

### 棋盘拼接游戏（Tiled）
- 标准棋盘（standard checkerboard）：8×8的标准国际象棋棋盘，黑白格拼接
- 拼板（board）：任意大小的矩形棋盘或删除一个或多个方格后的棋盘
- 骨牌（domino）：1×2的方格
> 拼接标准棋盘？
> > 应该可以，可以考虑骨牌每次都会盖上黑白两个格子，所以只要黑白格子数目一致就可以

> 拼接去掉一个角的棋盘？
> > 不可以，同上，去掉后黑白格子数目不一致。

> 拼接去掉对称两个角的棋盘？
> > 同上，不可以。

> 直三联骨牌拼接去掉一个角的棋盘？
> > 棋盘改成三种颜色，三种颜色交替拼接。
> > 
> > 考虑不同颜色棋盘格的个数,直三联骨牌每次要盖住3种颜色，考虑每种颜色格子个数即可。

> 但是类似的问题不一定都能用骨牌能占用每种颜色，且每种颜色格子数目相同来推出可以用该种骨牌将棋盘铺满。
>
> ~~***严格来讲，是否能铺满，取决于是否在铺满棋盘时是否存在一种每行每列颜色不重复(这里说的每行每列是指，有n种颜色的格子，在相邻n行或n列内不出现相同颜色的格子)的排序方式，使得每个骨牌在排序时，都占用对应不同颜色的格子，且不同颜色的格子数量在棋盘内相同***~~

### 猜想与证明
- [x] 定理：当a>2或者当a=2且n是合数时，整数 $a^n-1$是合数。
> 例：希望找到一个函数，对所有正整数n来说，函数f(n)都是素数。 $$f(n)=n^2-n+41$$
> 对所有不超过40的正整数n来说f(n)是素数。
> > 可以证明：对于每个整系数多项式f(n)，都存在正整数y，使得f(y)是合数。

- [x] 费马大定理：若n为大于2的整数，则 $x^n+y^n=z^n$ 没有正整数解。
> 3x+1猜想（Collatz猜想）：若变换T把偶数x转换为x/2，把奇数x转换为3x+1，则对于所有正整数x，当反复应用变换T，最终会得到整数1。
> > 已验证到 $5.6×10^{13}$

# 第二章 基本结构：集合、函数、序列、求和与矩阵
## 2.1  集合
### 定义
- [x] 集合（set）：一组无序的对象。
- [x] 元素（element）：集合中的对象也称为该集合的元素，或成员（member）。
	> 集合的表示方法：花括号之间列出所有元素
	> 英语字母中所有元音字母的集合： V={a,e,i,o,u}
 	> 小于10的正奇数集合： O={1,3,5,7,9} 
- 集合中的元素表面上可以看起来毫不相干： {a,2,Fred,New Jerseg}
- 通常用大写字母表示集合：自然数集合N，整数集合Z，正整数集合 $Z^+$ ，有理数集合Q，实数集合R
- 集合的表示方法：花括号中列出集合的部分元素，其余用省略号表示： {1,2,3…,99}

### 集合的基本定义和性质
- [x] 两个集合 ***相等（equal）*** **当且仅当它们有相同的元素。**
	> 元素的顺序不起作用：集合{1,3,5}和集合{3,5,1}相等；
	> 同一个元素被列出来不止一次也没关系： {1,3,3,3,5,5,5,5}和{1,3,5}是同一个集合。
- [x] 集合的描述方式：使用集合构造符号（谓词公式）
	> O={x|x是小于10的奇数}，O={x|P(x)}
 	> R={x|x是实数}
- [x] 集合的描述方式：文式图（Venn diagram）
	> 全集（universal set）：我们所考虑的所有对象的集合U，在文式图中用长方形代替
	> 用圆或其他几何图形表示集合，用点表示特定元素

 <p align="center">
	 <img src="./img/文氏图.png" alt="集合的文氏图示意图">
	 <p align="center"><span>示例：元音字母集合的文氏图示意图</span></p>
 </p>

 ### 集合成员的关系
- [x] a是集合A的一个元素：a∈A。
- [x] a不是集合A的一个元素：a∉A 。
- [x] 空集（empty set, null set）：不含任何元素的特殊集合，用∅表示
	> $\lbrace x|x>x^2, x∈Z^+\rbrace$ 是一个空集
 	> ∅和{∅}不一样，是两个集合
- [x] 单元集（singleton set）：只含有一个元素的集合
- [x] 集合A是集合B的子集（subset）当且仅当A的每个元素也是B的元素，用A⊆B表示A是B的子集。
	> A⊆B当且仅当量化语句∀x(x∈A→x∈B)为真。
- [x] 定理：对于任意集合S，(i) ∅⊆S和(ii) S⊆S。
	> 证明：(i)写为逻辑表达式∀x(x∈∅→x∈S),由于x∈∅为F，所以该式一定为重言式
 	>
 	> (ii) 写为逻辑表达式∀x(x∈S→x∈S)，该式子也一定为重言式
 	
- [x] 真子集（proper subset）：A是B的子集，但A≠B。
	> 证明两个集合相等的一个有效的方法就是证明它们互为另一个的子集，即如果A⊆B且B⊆A，则A=B；
	> 
 	> 集合可以以其他集合作为它的成员；
	> > {∅,{a},{b},{a,b}}
	> > {x|x是集合{a,b}的子集}
 
<p align="center">
	 <img src="./img/真子集文氏图.png" alt="真子集的文氏图示意图">
	 <p align="center"><span>真子集的文氏图示意图</span></p>
 </p>

- [x] 有限集合（finite set）：集合S中恰有n个不同的元素，其中n是一个非负整数，称为S的基数（cardinality），用|S|表示。
- [x] 无限集合（infinite set）：不是有限的集合，如正整数集合。

### 幂集合
- [x] 已知集合S，S的幂集合（Power Set）是集合S所有子集的集合，用P(S)表示。
	> 如果一个集合有n个元素，那么它的幂集合有 $2^n$ 个元素；
 
> 例：P({0,1,2})={∅,{0},{1},{2},{0,1},{0,2},{1,2},{0,1,2}}
>
> P(∅)={∅}
>
> P({∅})={∅,{∅}}

### 笛卡儿积
- [x] 有序n元组（ordered n-tuple） $(a_1,a_2,…,a_n)$ 是以 $a_1$ 为第1个元素， $a_2$ 为第2个元素，…， $a_n$ 为第n个元素的有序组。
	> 只有当两个有序n元组每一对对应的元素都相等时，他们才相等；
	>
 	> 有序2元组特称为有序偶；
- [x] 令A和B为集合。A和B的笛卡尔积（Cartesian product）用A×B表示，是所有有序偶(a,b)的集合，其中a∈A而b∈B。
$$A×B=\lbrace (a,b)| a∈A ∧ b∈B\rbrace$$
- [x] 笛卡儿积A×B的子集R称为从集合A到集合B的关系。
> 例：
> A={1,2}
>
> B={a,b,c}
>
> A×B={(1,a),(1,b),(1,c),(2,a),(2,b),(2,c)}
>
> B×A={(a,1),(b,1),(c,1),(a,2),(b,2),(c,2)}
> > ***可以看出来一般情况下：A×B ≠ B×A***
> >
> > ***注：集合的笛卡尔积也为集合，只是集合的元素为有序组，而非整个集合都是有序组，集合内的元素是可以换位置的，但是元素内部(有序组内部)的更小的元素是不能改变位置的。***

- [x] 集合 $A_1,A_2,…,A_n$ 的笛卡儿积用 $A_1×A_2×…×A_n$ 表示，这是有序n元组 $(a_1,a_2,…,a_n)$ 的集合，其中对于i=1,2,…,n， $a_i∈A_i$。
$$A_1×A_2×…×A_n =\lbrace(a_1,a_2,…,a_n) | a_i∈A_i, i=1,2,…,n\rbrace$$

> 例：什么是笛卡尔积A×B×C，其中A={0,1}，B={1,2}，C={0,1,2}？
> > A×B×C={(0,1,0),(0,1,1),(0,1,2),(0,2,0),(0,2,1),(0,2,2),(1,1,0),(1,1,1),(1,1,2),(1,2,0),(1,2,1),(1,2,2)}

### 使用带量词的集合符号
- [x] 用集合来表示量词的论域
	> 全称量化：∀x∈SP(x)
	> 存在量化：∃x∈SP(x)

> 例：语句 $∀x∈R(x^2 \geq)$ 和 $∃x∈Z(x^2=1)$ 的含义是什么？
> > 解释：语句 $∀x∈R(x^2 \geq)$ 声称对任意实数x， $x^2 \geq 0$ 。这个语句可以表述为“任意实数的平方是非负的”，该语句为真
> >
> >  $∃x∈Z(x^2=1)$ 声称存在一个整数x使得 $x^2=1$ 。这个语句可以表述为“有某个整数，其的平方是1”，该语句为真

### 真值集合
- [x] 给定谓词P和论域D，定义P的真值集合为：D中元素x使P(x)为真的元素组成的集合，即{x∈D|P(x)=T}。
	> 全称量化∀x∈U P(x)为真当且仅当P(x)的真值集合是集合U；
 	> 
	> 存在量化∃x∈U P(x)为真当且仅当P(x)的真值集合非空；
> 例：谓词P(x)、Q(x)、R(x)的真值集合都是什么？其中论域是整数集合，P(x)：|x|=1，Q(x)： $x^2$ =2，R(x)：|x|=x。

## 2.2 集合运算
### 并集
- [x] 令A和B为集合。A和B的并集（union）用A∪B表示，这是在A或B中或同时在A和B中的元素组成的集合。
      $$A \cup B=\lbrace x|x∈A ∨ x∈B\rbrace$$

<p align="center">
	 <img src="./img/并集文氏图.png" alt="并集文氏图">
	 <p align="center"><span>并集文氏图</span></p>
</p>

> 例：{1,3,5}∪{1,2,3} = {1,2,3,5}

### 交集
- [x] 令A和B为集合。A和B的交集(intersection)用A∩B表示，这是既在A中又在B中的元素组成的集合。
      $$A \cap B=\lbrace x|x∈A ∧ x∈B\rbrace$$
- [x] 如果两个集合的交集为空集，就说它们不相交(disjoint)

<p align="center">
	 <img src="./img/交集文氏图.png" alt="交集文氏图">
	 <p align="center"><span>交集文氏图</span></p>
</p>

> 例：{1,3,5}∩{1,2,3} = {1,3}
>
> {1,5}∩{2,3} = ∅

#### 容斥原理
- [x] 容斥原理（principle of inclusion-exclusion）：计算集合并集的基数
$$|A \cup B|=|A|+|B|-|A \cap B|$$

<p align="center">
	 <img src="./img/容斥原理文氏图.png" alt="容斥原理文氏图">
	 <p align="center"><span>容斥原理文氏图</span></p>
</p>

### 差集
- [x] 令A和B为集合。A和B的差集（difference）用A-B表示，这是只属于A而不属于B的所有元素组成的集合。A和B的差集也称为B对于A的补集。
$$A-B=\lbrace x|x∈A ∧ x∉B\rbrace$$

<p align="center">
	 <img src="./img/差集文氏图.png" alt="差集文氏图">
	 <p align="center"><span>差集文氏图</span></p>
</p>

> 例：A= {1,3,5},B={1,2,3} ，A∩B= {1,3} ，A-B = {5}，B-A = {2}
### 补集
令U为全集。集合A的补集（complement）用 $\bar A$ 表示，这是A对于U的补集，即U-A。
$$\overline{A}=\lbrace x|x∉A\rbrace$$

<p align="center">
	 <img src="./img/补集文氏图.png" alt="补集文氏图">
	 <p align="center"><span>补集文氏图</span></p>
</p>

### 集合恒等式
- [x] 如下表所示(U为全集)

|恒等式|名称|
|----|----|
| $A\cap U=A$ <br> $A\cup \varnothing=A$ |恒等律|
| $A\cup U=U$ <br> $A\cup \varnothing=\varnothing$ |支配率|
| $A\cap A=A$ <br> $A\cup A=A$ |幂等律|
| $\overline{(\bar{A})}=A$ |补律|
| $A\cap B=B \cap A$ <br> $A\cup B=B\cup A$ |交换律|
| $A \cup (B\cup C)=(A \cup B)\cup C$ <br> $A \cap (B\cap C)=(A \cap B)\cap C$ |结合律|
| $A \cap (B \cup C)=(A \cap B)\cup (A \cap C)$ <br> $A \cup (B \cap C)=(A \cup B)\cap (A \cup C)$ |分配律|
| $\overline{A \cap B}=\bar{A} \cup \bar{B}$ <br> $\overline{A \cup B}=\bar{A} \cap \bar{B}$ |德·摩根律|
| $A\cup (A \cap B)=A$ <br> $A\cap (A \cup B)=A$ |吸收律|
| $A \cup \bar{A}=U$ <br> $A \cap \bar{A}=\varnothing$ |互补律|
| $A-B=A\cap \bar{B}$ ||

### 证明集合恒等式的方法
- [ ] 证明两个集合相等：证明两个集合互为对方的子集。
- [ ] 证明两个集合相等：使用集合构造符和推理。
> 例如：证明 $\overline{A \cap B}=\bar{A} \cup \bar{B}$
> > 证明：对于 $x \in \overline{A \cap B}$ ，有 $x \notin A \cap B$ = $\neg (x \in A ∧ x \in B)$
> >
> > = $\neg (x \in A) ∨ \neg (x \in B)$ = $x \notin A ∨ x \notin B$ = $x \in \bar A ∨ x \in \bar B$ 
> >
> > = $\bar A \cup \bar B$ (该证明加上{x|}即集合构造符即可)
- [ ] 要证明涉及两个以上集合的集合恒等，可以证明恒等式的每一边是另一边的子集。
- [ ] 使用成员表来证明集合恒等式：用1表示元素属于一个集合，0表示元素不属于一个集合。
> 例如：可以用成员表证明 $A \cap (B \cup C)=(A \cap B)\cup (A \cap C)$
- [ ] 使用已经证明的集合恒等式来证明其它集合恒等式。
> 例如：证明 $\overline{A \cup (B \cup C)}=(\bar C \cup \bar B)\cap \bar A$
> > 证明： $\overline{A \cup (B \cup C)}=\bar A \cap \overline{B \cap C}$
> >
> > $=\bar A \cap (\bar B \cup \bar C)$ (再利用交换律即可)

### 扩展的并集和交集
- [x] 一组集合的并集是包含那些至少是这组集合中一个集合成员的元素的集合。
- [x] 一组集合的交集是包含那些属于这组集合中所有集合成员的元素的集合。

<p align="center">
	 <img src="./img/扩展文氏图.png" alt="扩展的并集和交集文氏图">
	 <p align="center"><span>扩展的并集和交集文氏图</span></p>
</p>

> 例：令A={0,2,4,6,8}，B={0,1,2,3,4}，C={0,3,6,9}。A∪B∪C和A∩B∩C 是什么集合？
>
> A∪B∪C包括那些至少属于A，B，C之一的元素，则：A∪B∪C={0,1,2,3,4,6,8,9}
>
> A∩B∩C包含那些属于全部三个集合的元素，则：A∩B∩C={0}

> 例：令 $A_i=\lbrace i,i+1,i+2,...\rbrace$ ，那么有
> $\bigcup\limits_{i=1}^n A_i=\bigcup\limits_{i=1}^n \lbrace i,i+1,i+2,...\rbrace=\lbrace 1,2,3,...\rbrace$
> $\bigcap\limits_{i=1}^n A_i=\bigcap\limits_{i=1}^n \lbrace i,i+1,i+2,...\rbrace=\lbrace n,n+1,n+2,...\rbrace$

### 计算机表示集合的方法
- [x] 假定全集U的元素个数n是有限的，且大小合适；
- [x] 为U的元素任意规定一个顺序，如 $a_1,a_2,…,a_n$ ；
- [x] 用长度为n的位串表示U的子集A：如果 $a_i$属于A，则位串中第i位是1，否则为0；
- [x] 用位串表示集合便于计算集合的补集、并集、交集和差集；
	> 补集：把位串的每个1改为0，0改为1；
 	>
	> 并集和交集：对表示两个集合的位串按位做对应的布尔运算（并集为按位或（bitwise OR），交集为按位与（bitwise AND））；

> 例：U={1,2,3,4,5,6,7,8,9,10},令 $a_i=i$
>
> A={1,3,5,7,9} 1010101010
>
> B={2,4,6,8,10} 0101010101
>
> C={1,2,3,4,5} 1111100000

## 2.3 函数
### 定义
- [x] 令A和B为集合。从A到B的函数（function）f是对元素的一种指派，对A的每个元素恰好指派B的一个元素。
	- [ ] 如果f指派给A中元素a的唯一的B元素是b，就写成f(a)=b；
	- [ ] 如果f是A到B的函数，就写成f:A→B；
 	- [ ] 函数f:A→B有时定义为从A到B的关系；
- [x] 如果f是从A到B的函数，就说A是f的定义域（domain），而B是f的伴域（codomain）。如果f(a)=b，就说b是a的像（image）而a是b的原像（preimage）。A中元素的所有像元素的集合称为f的值域（range）。有时也说f把A映射（mapping）到B。

<p align="center">
	 <img src="./img/函数的例子.png" alt="函数的例子">
	 <p align="center"><span>函数的例子</span></p>
</p>

> 例：令f为从Z到Z的函数，它指派给每个整数的是该整数的平方。于是 $f(x)=x^2$ ，而f的定义域是所有整数的集合，f
的伴域可以从所有整数集合中选择，f的值域是所有非负整数中那些完全平方的集合，即{0,1,4,9……}

### 函数相加和相乘
- [x] 令 $f_1$ 和 $f_2$ 是从A到R的函数，那么 $f_1+f_2$ 和 $f_1 f_2$ 也是从A到R的函数，其定义为
$$(f_1+f_2)(x)= f_1(x)+ f_2(x)$$
$$(f_1f_2)(x)= f_1(x)f_2(x)$$

> 例：令 $f_1$ 和 $f_2$ 是从R到R的函数，且 $f_1(x)=x^2$ 而 $f_2(x)=x-x^2$ 。函数 $f_1+f_2$ 和 $f_1f_2$ 是什么？
> > 从函数的和与积的定义知：
> >
> > $$(f_1+f_2)(x)=f_1(x)+f_2(x)=x^2+(x-x^2)=x$$
> > $$(f_1f_2)(x)=x^2(x-x^2)=x^3-x^4$$

### 集合的像
- [x] 令f为从集合A到集合B的函数，S为A的一个子集。S的像是由S中元素的像组成的B的子集，用f(S)表示。
$$f(S)=\lbrace f(s)|s∈S\rbrace$$

> 例：令A={a,b,c,d,e}而B={1,2,3,4}，且f(a)=2，f(b)=1，f(c)=4，f(d)=1， f(e)=1。子集S={b,c,d}的像是集合f(S)={1,4}
 
### 一对一函数
- [x] 令函数f称为一对一（one-to-one）的或单射的，当且仅当对于f的定义域中的所有x和y，f(x)=f(y)蕴含着x=y。一对一函数称为单射（injection）。
$$∀x∀y(f(x)=f(y) →x=y)$$
$$∀x∀y(x≠y→f(x)≠f(y))$$
> 例：判断从{a,b,c,d}到{1,2,3,4,5}的函数是否一对一的，f的定义是f(a)=4，f(b)=5，f(c)=1而f(d)=3。

#### 一对一函数的例子
- [x] 判断从整数集合到整数集合的函数f(x)=x2是否为一对一的?
> 函数 $f(x)=x^2$ 不是一对一的，因为，例如f(1)=f(-1)=1，但1 ≠-1。
> > 若定义域限制为 $Z^+$ ，函数f就是一对一的。
- [x] 判断函数f(x)=x+1是否为一对一的。
> 函数f(x)=x+1是一对一的。因在x≠y时x+1≠y+1。

#### 函数为一对一的条件
- [x] 定义域和伴域都是实数集合子集的函数f称为严格递增的（strictly increasing），如果对f定义域中的x和y，只要x<y就有f(x)<f(y)。类似的，f称为严格递减的（strictly decreasing），如果对f定义域中的x和y，只要x<y就有f(x)>f(y)。
	> 严格递增：∀x∀y(x<y→f(x)<f(y))
	> 严格递减：∀x∀y(x<y→f(x)>f(y))
	> 论域为f的定义域
- [x] 只要函数是严格递增的或严格递减的，它必定是一对一的。

### 映上函数
- [x] 从A到B的函数f称为映上的（onto）或满射的（surjective），当且仅当对每个b∈B，有元素a∈A使得f(a)=b。如果函数f是映上的，则称它为映上函数或满射函数（surjection）。
	> 映上函数：∀y∃x(f(x)=y)，其中x的论域是函数的定义域，y的论域是函数的伴域；
	> 函数的值域和伴域相等；
> 例：判断从{a,b,c,d}到{1,2,3}的函数是否映上的，f的定义是f(a)=3，f(b)=2，f(c)=1而f(d)=3。

#### 映上函数的例子
> 例：从整数集到整数集的函数 是映上的吗？
> > 解：f不是映上的，比如说没有x使 。
> 例：从整数集到整数集的函数f(x)=x+1是映上的吗？
> > 解：这个函数是映上的，因为对每个整数y，都有一个整数x使f(x)=y。 f(x)=y的充要条件是x+1=y,而这只要令x=y-1就成立。

### 一一对应函数
- [x] 若函数f既是一对一的，又是映上的，就说它是一一对应（one-to-one correspondence）或双射的（bijection）。
	> 假定f是从集合A到它自身的函数。如果A是有限的，那么f是一对一的当且仅当它是映上的。
	> 当A为无限集时，这一结论不一定成立。 

<p align="center">
	 <img src="./img/一一对应函数例子.jpg" alt="一一对应函数例子">
	 <p align="center"><span>一一对应函数例子</span></p>
</p>
