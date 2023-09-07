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

<div id="cer" align="center">
 
::: markdown-cer
|p|┐p|
|----|----|
|T|F|
|F|T|
:::

</div>

- 运算符（operator）可以从已有命题构造新命题。有时可称为联接词（connective）。
- 非运算符： ┐
- 原子命题（ Atomic Proposition ）：不含逻辑运算符的命题，不可拆分<span id="yuanzimingti"></span>
- 复合命题（Compositional Proposition） ：用逻辑运算符组合命题构造出的新命题

- - -
### 合取（conjunction）
> 令p和q为命题。用p∧q表示这样一个命题：当p和q均为真命题时它为真，否则为假。命题p∧q称为p和q的合取。
注:***理解为集合运算交运算，有一个为假就为假*** 。

|p|q|p∧q|
|----|----|----|
|T|T|T|
|F|T|F|
|T|F|F|
|F|F|F|

- - -
### 析取（disjunction）
> 令p和q为命题。用p∨q表示这样一个命题：当p和q均为假命题时它为假，否则为真。命题p∨q称为p和q的析取。
***注意:理解为同或或者集合中的并运算，有一个为真就为真***

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

## 1.3 命题等价

- 永真式（tautology，重言式）：无论其中出现的原子命题的真值是什么，复合命题的真值永远是真；
- 矛盾（contradiction）：真值永远为假的复合题；
- 可能式（contingency）：既不是永真式，又不是矛盾的命题。
例:`p∨┐p` 为永真式，`p∧┐p` 为矛盾。

|p|┐p|p∨┐p|p∧┐p|
|----|----|----|----|
|T|F|T|F|
|F|T|T|F|

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
> - [x] 判定两个命题是否等价：使用真值表（其实这个在推不出来，并且在原子命题数少时非常好用）
> > - [ ] 涉及n个原子命题的复合命题，需要2n行
> > - [ ] 当n较大时，真值表方法行不通
> - [x] 判定两个命题是否等价：使用已建立的等价关系来构造其他等价关系
> > - [ ] 复合命题中的一个命题可以用与它逻辑等价的命题替换，而不改变复合命题的真值（***注:此时的命题替换与重言式中的命题置换不一样***）
> - [x] 德摩根定律： ┐(p∨q) ≡ ┐p∧┐q

#### 重要的等价关系（很重要）
> ***注:以下表中的等价关系是可以直接用不用推导的，其他的需要自行推导***

> ***从下面的表格不难看出来，五种基本运算符（合取，析取，否定，蕴含，双蕴含）之间是可以互相表示的，且每一种运算符最少要用2种其他的运算符表示。***

### 逻辑等价的性质，和数学中等号性质类似

#### 性质
1. 自反性： p⇔p
2. 对称性： 若p⇔q，则q⇔p
3. 传递性：若p⇔q， q⇔r，则p⇔r

#### 判定两个命题是否等价（考点）
- 使用已建立的等价关系来构造其他等价关系
> 证明┐(p∨(┐p∧q) ≡ ┐p∧┐q

> 证明 (p∧q)→(p∨q)为永真式
>
> ***思路:即证明等价为T***

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
> - [x] 每一行包含了每一个数
> - [x] 每一列包含了每一个数
> - [x] 每一个九宫格包含了每一个数
> - [x] 没有一个单元包含多余一个数

## 1.4 谓词和量词

### 谓词

#### 定义
- 简单认为是用于判断性质的语句或者符号，比如“是”，“>”等。

#### 命题函数
– 含变量的语句，在变量值未知时，语句既不为真，也不
为假：“x>3”，“x=y+3”，“x+y=z”
– 命题函数（propositional function）：谓词（predicate）和变量的组合
- P(x1, x2, …, xn)表示命题函数P在n元组（n-tupie）(x1, x2, …, xn)的值，P也称为谓词，用来描述个体的属性以及个体之间的关系；
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
- 命题∀xP(x)表示为“对所有x，P(x)”或“对每个x，
P(x)”。
> 当论域中的所有元素可以一一列出时

> ∀xP(x) ≡ P(x1)∧P(x2)∧…∧P(xn)

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
– P(x)的存在量化是命题“论域中存在一个元素x使P(x)为真”，记为∃xP(x)。其中∃称为存在量词。（存在一个但也可以不止一个）
– 命题∃xP(x)表示为“有一个x使得P(x)”或“对某个x，P(x)”。
> 当论域中的所有元素可以一一列出时
> 
> ∃xP(x) ≡ P(x1)∨P(x2)∨….∨P(xn)
> 
> 使用量词时，论域是很重要的

#### 举例
> P(x)：x>3
>
> 论域：实数集合
> 
> ∃xP(x)=T
