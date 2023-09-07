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
- S={A|A∉A}}也就是说S是由满足条件A∉A的那些A组成的一个新的集合。
- 我们要问:S是不是它自己的一个元素? 即S∈S,还是S∉S。
- 既不是S∈S,也不是S∉S, 这个悖论就是著名的罗素悖论。

- - -
### 命题（Proposition）
命题：是一个或真或假的陈述语句，但不能既真又假。
> 以下不是命题:（可判断真假的才是命题）
x+1＝2（含有变量无法判断真假），几点了？
仔细读这个。

- 命题变元：命题的字母表示，p, q, r, s, …
- 命题的真值（true value）：真命题的真值用“T”表示，假命题的真值用“F”来表示
- 命题逻辑（propositional logic）或命题演算（propositional calculus）：涉及命题的逻辑领域。

- - -
### 命题的否定
> 命题的否定（negation）：令p为一命题，则语句“不是p所说的情形”是另一个命题，称为p的否定，用“┐p”表示。命题“┐p”读为“非p”。

- - -
### 真值表和运算符
> 真值表（truth table）给出了命题真值之间的关系。
 
|p|┐p|
|----|----|
|T|F|
|F|T|

- 运算符（operator）可以从已有命题构造新命题。有时可称为联接词（connective）。
- 非运算符： ┐
- 原子命题（ Atomic Proposition ）：不含逻辑运算符的命题，不可拆分
- 复合命题（Compositional Proposition） ：用逻辑运算符组合命题构造出的新命题

- - -
### 合取（conjunction）
> 令p和q为命题。用p∧q表示这样一个命题：当p和q均为真命题时它为真，否则为假。命题p∧q称为p和q的合取。
注:***理解为集合运算并运算*** 。

|p|q|p∧q|
|----|----|----|
|T|T|T|
|F|T|F|
|T|F|F|
|F|F|F|

- - -
### 析取（disjunction）
> 令p和q为命题。用p∨q表示这样一个命题：当p和q均为假命题时它为假，否则为真。命题p∨q称为p和q的析取。
***注意:理解为同或或者集合中的或运算***

|p|q|p∨q|
|----|----|----|
|T|T|T|
|F|T|T|
|T|F|T|
|F|F|F|

- - -
### 异或（exclusive or）
> 令p和q为命题。p和q的异或，用p⊕q表示，是这样一个命题：当p和q中恰有一个为真时它为真，否则为假。

|p|q|p⊕q|
|----|----|----|
|T|T|F|
|F|T|T|
|T|F|T|
|F|F|F|

- - -
### 蕴含（implication）
> 令p和q为命题。蕴含p→q是这样一个命题：当p为真而q为假时它为假，否则为真。p称为假设（或前提，前项），q称为结论（或推论）。一个蕴含有时也称为条件语句（conditional statement）
> >  ***注意：只有在p为真而q为假时， p→q才为假。如果p为假，则不管q的真值是什么， p→q都为真。***

|p|q|p→q|
|----|----|----|
|T|T|T|
|F|T|F|
|T|F|T|
|F|F|T|

> 计算机语言“if then”和蕴含的区别“if 2+2=4 then x:=x+1”不是蕴含，因为包含未知参数，所以两个语句都不是命题，从而不是蕴含。

#### 蕴含的逆、倒置和反
- 蕴含： p→q
- 逆蕴含（converse implication）： q→p
- 倒置蕴含（contrapositive implication）: ┐q→ ┐p
- 反蕴含（inverse implication）： ┐p→ ┐q
> 倒置蕴含和蕴含有相同的真值
> 逆蕴含和反蕴含有相同的真值，但与蕴含的真值不同
- 等价（equivalent）：两个复合命题总是具有相同的真值时，我们称这两个命题等价

- - -
### 双蕴含（bi-imiplication）
> 令p和q为命题。双蕴含p↔q是这样一个命题：当p和q具有相同真值时它为真，否则为假。一个双蕴含有时也称为双条件语句（biconditional statement），可理解为p为q的充要条件。
> > ***可理解为异或的反取***

|p|q|p↔q|
|----|----|----|
|T|T|T|
|F|T|F|
|T|F|F|
|F|F|T|

#### 双蕴含的含义
- 双蕴含p↔q恰在p→q和q→p均为真时为真。我们常用术语“p当且仅当q”来表示这一双蕴含。
- p↔q与(p→q) ∧(q→p)有完全相同的真值。
> “当且仅当”结构在自然语言中很少使用，我们一般用相对简单的结构来表示。比如说，“你吃完饭才可以吃甜点”。双蕴含的部分含义是隐含的，这就造成了在有些情况下，自然语言的不精确性。而在数学上，双蕴含和单蕴含是有明确区分的。~~可能双蕴含在自然语言中是只有才，单蕴含是如果就~~
- 自然语言和逻辑的区别
> 逻辑：p↔q= q↔p
> 自然语言：不一定。如p：吃完饭；q：可以吃甜点

- - -
### 逻辑运算符的优先级

|运算符|优先等级|
|----|----|
|┐|1|
|∧|2|
|∨|3|
|→|4|
|↔|5|

***注:在容易混淆的情况下，尽量使用括号 。***
- - -
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
- - -
### 命题逻辑的应用-翻译语言的句子
- 由于语言的二义性，需要把句子译成逻辑表达式以消除
歧义，有时需要在句子含义基础上做一些合理的假设
 > 例1:“只有你主修计算机科学或不是新生，才可以从
校园网访问因特网”
 a：你从校园网访问因特网；
 c：你主修计算机科学；
f：你是一个新生；
 a↔(c ∨ ┐f)
> 例2:“除非你已满16周岁，否则只要你身高不足4英
尺就不能乘公园滑行铁道游乐车”
 q：你能乘公园滑行铁道游乐车；
 r：你身高不足4英尺；
s：你已满16周岁；
 (r ∧ ┐s)→┐q
 
- - -
### 系统规范说明（~~感觉不重要~~）

- 在说明硬件系统和软件系统时，把自然语言语句翻译成逻辑表达式是很重要的一部分。这些说明可以作为系统开发的基础。
- 系统规范说明不应该存在冲突，因此，表示这些规范说明的命题表达式应该是一致的。
- 也就是说，对表达式中的各个变量，必然有一个真值赋
值使所有表达式为真。（自洽的）

### bool搜索和逻辑电路（略）

## 命题等价

- 永真式（tautology，重言式）：无论其中出现的原子命题的真值是什么，复合命题的真值永远是真；
- 矛盾（contradiction）：真值永远为假的复合题；
- 可能式（contingency）：既不是永真式，又不是矛盾的命题。
例:
