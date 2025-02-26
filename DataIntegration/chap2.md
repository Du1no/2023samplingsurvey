## 以下内容刘奕彤编写
### 2.4.3 比较数据建模(Ⅰ)

首先考虑一种比较数据建模的方法，它可以与FS范式下的概率记录联系起来。在保持普遍性的同时，让$g_a^*=h$作为$a \in A$的完整比较数据，同时$g_b^*=j$作为$b \in B$的完整比较数据，对于h,j=1,…,K 。正如Stoerts et al.（2015）等人，我们假定比较数据的潜在失真在实体之间是独立的，因此
$f(G^*|ω)= \prod\limits_{(ab) \in M}f(g_a^*,g_b^*|ω_ab=1) \prod\limits_{a \in U_B}f(g_a^*|a \in U_A) \prod\limits_{b \in U_B}f(g_b^*|b \in U_B)$

请注意，原则上，数据链接者可以提供这些概率作为比较数据，而不用披露关键变量。
当只有比较数据$G=\{g_{ab};a \in A_L,b \in B_L\}$ \\可用时，也就是实践中最有可能出现的情况，此时，可以从整合出$g_a^*$和$g_b^*$在完整的比较数据模型中的$g_a^*$和$g_b^*$进行积分，从而得到:

$f(G|\omega )= \prod\limits_{(ab):\omega_ab=1}f(g_ab|\omega_ab=1)$(2.3)

为了建立相关的概率模型，考虑Copas和Hilton（1990）提出的命中-失误失真模型模型，该模型由Copas和Hilton（1990）提出。设想一个二进制试验导致概率为$\alpha$的失误，随后观察到的值h是以概率$p_h$随机分布的，其中$p_h$是真实值h的频率。让$K=n_A +n_B-m$是A和B中实体的数量，其中$m=|M|$。假设所有实体的完整比较数据是不同的，因此以便$p_h=1/K$。对于一个简单的比较数据模型，让为协议指标。我们有:

$\mu_{ab}=f(g_{ab}=1|\omega_{ab}=1)=(1-\alpha)^2+2\alpha(1-\alpha)/K+\alpha^2/K$

$\mu_{ab}^c=f(g_{ab}=0|\omega_{ab}=1)=1-\mu_{ab}=(1-(1-\alpha)^2)(1-1/K)$

这可能被称为可交换协议（EA）模式。次要的分析师只需要提供K（或m）的估计值。

似乎很直观的是，在适当的条件下，EA模型可以产生ELE模型。适当的条件下，EA模型可以产生ELE模型。例如，假设一对一完全匹配，其中综合数据的分析h,j = 1,……,n 和$U_A = U_B =∅ $。在 EA 模型下，让$ \mu_ab=\mu(\alpha)$，其中$ g_{ab}$是协议指标。假设记录连接进行如下进程：如果它们是唯一一致的，则链接(ab)；如果没有唯一一致的记录，则随机链接记录中随机链接，但要遵守一对一的链接约束。这将导致ELE模型，其参数为$\lambda(\alpha,\phi)=q_{ii}=f(P_{ii}=1|\omega_{ii}=1)$, 其中$\omega=I_{n \times n}$的定义。

| $\alpha$ | n=3


| n=10 | n=50        | n=300       | n=1000      |             |             |
| ---- | ----------- | ----------- | ----------- | ----------- | ----------- |
| 0.02 | 0.974/0.987 | 0.965/0.981 | 0.961/0.975 | 0.961/0.964 | 0.960/0.962 |
| 0.05 | 0.935/0.966 | 0.912/0.950 | 0.904/0.925 | 0.903/0.910 | 0.903/0.907 |
| 0.10 | 0.873/0.937 | 0.829/0.895 | 0.814/0.846 | 0.811/0.827 | 0.810/0.824 |
| 0.20 | 0.760/0.878 | 0.676/0.790 | 0.647/0.712 | 0.641/0.691 | 0.640/0.688 |

虽然$\mu(\alpha)$有一个封闭的表达式，但$\lambda(\alpha,\phi)$只能通过G的蒙特卡洛模拟和随后的联系程序获得$\phi$。表2.2提供了$\mu$和$\lambda$给定的$\alpha$和n之间的比率，其中每个都是基于5000次模拟的结果。显然，在所有情况下$\mu /\lambda<1$。在一端，观察在任何固定的情况下，$\mu /\lambda→1$为$n\longrightarrow\infty$，因为在失误之后达成一致的机会趋于零，同时也趋于零。错过的机会趋向于零，而通过随机连接匹配的机会也是如此。在另一端，对于较小的n和较大的 ，$\mu /\lambda$进一步远离1，其中在这里，一对一联系限制的效果直观上是最强的。

表2.3

对于比较模型下的线性回归的一个非常简单的说明模型（2.3）下的线性回归，假设n=3的一对一完全匹配。矩阵$Q_G$为$\beta_G$由（2.2）取决于观察到的G。表2.3给出了两个例子。
$\alpha=0.02$时，观察到$G_1$的概率$f（G_1|\omega）$是0.923$G_1$，鉴于此
$\beta_G$的效率几乎与已知的$\omega$一样，因为$Q_G \approx I$ 。当$\alpha =0.1$观察到$G_1$的概率下降到0.666。回归的有效性低于$G=G_2$，从相应的$Q_G$可以看出。差异根植于$f(G|\omega)=\mu^{d}(1-\mu)^{n-d}$ 其中是观察到的$M(\mu)$的吻合度。让$d_0(G)$为给定G下最大可能的d，当$d_0(G_1)=3$且$d_0(G_2)=2$事，我们有：

$\sum_{\omega\in\Omega}f(G|\omega)=\sum_{d=0}^{d_{0}(G)}m_{d}f_{d}$

其中$f_d=f(G|\omega)$对于任何具有相同d的$\omega$来说是相同的，$m_d$是这样的数量$\omega's$. 似然比为$f_{d+1}/fd=\mu/(1-\mu)$.由$G_1$引起的协议分区是$m_d=(2,3,1)$，对于d=(0,1,3)，并且$\omega=G_1$的可能性是$f_3$,是次高的$f_1$的$\mu^2/(1-\mu)^2$倍。而鉴于$G_2$，我们有$m_d=(2,2,2)$，因为$d=(0,1,2)$，其中有两个$\omega's$最高的可能性$f_2$，是次高$f_1$的$\mu/(1-\mu)$倍。观察到$G=G_2$的不确定性显然大于$G=G_1$。

### 2.4.3 比较数据建模(Ⅱ)

在实践中，多通道的确定性联系是很常见的。让$L_k = A_k\times B_k$包含
k=1,…,K的第k次传递的$n_k$个链接。这些是在第k次传递中彼此完全一致的记录。没有链接的的记录留待以后的检验。让$A_0$包含A和$B_0$中的记录。联系的结果是分区:

$A\times B=\bigcup_{k=0}^{K}\bigcup_{j=0}^{K}A_{k}\times B_{j}$

让$g_{ab} = (k, j)$表示记录对(ab)属于分区的这些域的集合构成了比较数据G。

对于任何$（ab）\in  L_k$，让$\pi_{k}=\,f\bigl(\omega_{a b}\,=\,1\vert g_{a b}\,=\,(k,k)\bigr)$，这样，$1-\pi_{k}$   是$L_k$中的FLR（如表2.1）。我们有

$\mu_{a b}=f{\big(}g_{a b}=(k,k)|\omega_{a b}=1{\big)}=\pi_{k}f{\big(}g_{a b}=(k,k){\big)}/f(\omega_{a b}=1)$

人们可以通过$\pi_k n_k/m$来估计$\mu_{ab}$。理想情况下，我们希望数据提供者
能够提供$\mu_{a b}=\,f\bigl(g_{a b}=(k,j)\bigr)\bigl\vert\omega_{a b}=\,1\,\bigr)$对所有其他的组合

(k, j)也是如此。然而，这在实践中可能是很苛刻的。作为一个可能的
简化，让$L=\bigcup_{k=1}^{K}L_{k}$包含所有的链接对，并让

$\mu_{a b}=f\Bigl((a b)\ll L|\omega_{a b}=1\Bigr)=1-\sum_{k=1}^{K}f\Bigl(g_{a b}=(k,k)|\omega_{a b}=1\Bigr)$

其中假定$g_{ab}$在连接对之外的均匀分布。

当然，上述比较模型是对现实的极大简化。
因为匹配不可能均匀地分布在
$R = (A\times B) / L$。事实上，在所有未链接的记录对中，我们可以期待
预计$m_{R}=m-\sum_{k=1}^{K}\pi_{k}n_{k}$的匹配。我们可以探索$\mu_{ab}$的界限.例如，让$R_k$成为R的子集，其中涉及$a \in A_k$或$b \in B_k$，在这里我们最多可以期待$2n_{k} 1-\pi_{k})$匹配。因此，

$ f{\bigl(}(a b)\in R_{k}{\vert}\omega_{a b}=1{\bigr)}\leq2(1-\pi_{k})n_{k}/mf$，这就提供了一个$\mu_{ab}$在$R_k$上的上限.此外，让$R_0=A_0 \times B_0$，其中可以预期至少有

$m_{R}-2\sum_{k=1}^{K}(1-\pi_{k})n_{k}$k的匹配，因此$\mu_{ab}$在$R_0$上的下限是

$R_{0}|\omega_{a b}=1\rangle\geq1-\sum_{k=1}^{K}(2-\pi_{k})n_{k}/m$

让我们考虑C-PR的情况来说明。让$n_A$是人口普查数据集的大小，$n_B$是病人登记册的大小。让$n_L$是链接的数量（表2.1），m为匹配实体的数量。为了便于理解，假设m=51，nA=53，nB=55，都是以百万计。

* 对于第k个确定性通道，其中k=1,…9，FLR $1 -\pi_k$给出如表2.1我们设定  $\mu_{ab} = \pi_k n_k/m$ 为$（ab）\in  L_k$。

- 除了表2.1之外，我们没有其他关于两个概率性，分别用$L_10$和$L_11$表示。因此我们把它们就像从确定的联系中产生的一样。
- 我们还计算了$R_k$中的上界概率$\mu_{ab}$，和$R_0$中的下限概率 ˜$\mu_{ab}$。

表2.4

当涉及到大型人口时，可扩展性是一个重要的问题，比如在C-PR案例中。考虑一下评估的一般任务：

$E(t_{\omega}|G)=\sum_{\Omega}t_{\omega}f(\omega|G)=\sum_{\Omega}t_{\omega}f(G|\omega)/\sum_{\Omega}f(G|\omega)$

此时$t_\omega$ 是$\omega$的一个函数，正如在2.2中作为$Q_G$的$t_\omega=\omega^T$

完整列举$\omega$在大多数情况下是不可行的。让我们从$\omega$
中去一个样本$ s=\{\omega_{1},...,\omega_{n_{\circ}}\}\subset\Omega$.如果对$\omega's$进行随机抽样，那么H´ajek类型的估计是$E(t_\omega|G)$是$\bar{t}_{H}:=\sum\omega{\in}s\,t_{\omega}f(G|_{c o})/{\sum}\omega{\in}s\,f(G|_{c o})$而如果$\omega\sim f(\omega|G)$,蒙特卡洛估计是$\bar{t}=\sum_{\omega\in s}t_{\omega}/n_{s}$ 。Metropolis-Hastings算法提供了一种解决后者的一般方法：在每一步中从当前的中提出一个新的$\omega's$，其中的提议是对称的，接受率为$min|\{1,\;f(\omega^{\prime}|G)/f(\omega|G)\}.$

在上面的比较数据模型下，我们可以直接分析C-PR联系数据的接受率。让$\omega=\omega_L$ 为与链接矩阵完全一致的匹配矩阵，其中当且仅当$(ab) \in L $时$\omega_{ab}=1$。在以下子矩阵中得到了一般性的描述$\{a,a^{\prime},a^{\prime\prime}\}\times\{b,b^{\prime},b^{\prime\prime}\}$:

$[\omega_{L}]=\left[\begin{array}{c c c}{{1}}&{{0}}&{{0}}\\ {{0}}&{{1}}&{{0}}\\ {{0}}&{{0}}&{{0}}\end{array}\right]$

$[\omega_{1}]=\left[\begin{array}{c c c}{{1}}&{{0}}&{{0}}\\ {{0}}&{{1}}&{{0}}\\ {{0}}&{{0}}&{{1}}\end{array}\right]$

$[\omega_{2}]=\left[\begin{array}{c c c}{{0}}&{{0}}&{{1}}\\ {{0}}&{{1}}&{{0}}\\ {{0}}&{{0}}&{{0}}\end{array}\right]$

$[\omega_{3}]=\left[\begin{array}{c c c}{{0}}&{{1}}&{{0}}\\ {{1}}&{{0}}&{{0}}\\ {{0}}&{{0}}&{{0}}\end{array}\right]$

其中$1\leq k\neq k^{\prime}\leq11$ $(ab) \in L_K$

每一矩阵中的第一行是子向量$(\omega_{a b},\omega_{a b^{\prime}},\alpha_{a b^{\prime\prime}})$，第二行和第三行也是如此.

* $\omega_L$和$\omega_1$之间的唯一区别是，$\omega_1$包含一个额外的匹配 (a'',b'')。根据表2.4,我们有$f(\omega_{1}|G)/f(\omega_{L}|G)=\mu_{a b;0}=0.0100,$，或者至少是0.0055.
* 根据$\omega_2$，$R_k$中的一对实际上是一个匹配，而不是$L_k$中的一对。有$f(\omega_{2}|G)/f(\omega_{L}|G)=f{\big(}(a b^{\prime\prime})\in R_{k}|\omega_{a b^{\prime}}=1{\big)}/\mu_{a b;k}\leq{\tilde{\mu}}_{a b;k}/\mu_{a b;k}$，这对于表2.4中的所有1＜k＜ 11接近于零。
* 对于$\omega_3$，$L_k$中的(ab)和$L_{k'}$中的(a',b')是错误的链接，而$R_k$中的(ab')和(a'b)匹配未能被链接。而$R_k$中的(ab')和$R_{k'}$中的(a'b)不能被链接。我们有$f(\omega_{3}|G)/f(\omega_{L}|G)\ \leq\tilde{\mu}_{a b;k}\tilde{\mu}_{a b;k^{\prime}}/\mu_{a b;k}\mu_{a b;k^{\prime}}$这对所有$1\leq k\mp k^{\prime}\leq1^{\circ}$来说几乎是零。

因此，Metropolis-Hastings算法在数值上是不够有效的。考虑到$m>n_L$，匹配矩阵有$\omega_L$ 作为链接记录的子矩阵，再加上$m-n_L$在$A_0 \times B_0$之间的额外匹配,都有相同的可能性。这种矩阵的数量是$\left((n_{A}-n_{L})!/(n_{A}-m)!\right)\Bigl((n_{B}-n_{L})!/(n_{B}-m)!\Bigr)/(m-n_{L})!$

在结果空间如此之大的情况下，任何对$f(\omega|G)$的再抽样方法都是非常不切实际的。







## 以下内容侯宇欣编写
# 2.5关于链接子集的分析
## 2.5.1非信息性平衡选择
&ensp;&ensp; 出现上述可伸缩性问题是因为我们的目标是利用存在于单独数据集之间的所有匹配实体。然而，由于错过了比赛，ω的可能性可能在一个非常大的空间上是平坦的。因此，在C-PR案例中，似乎很自然地问，是否有可能将分析限制在5000万条链接记录，甚至是它的一个子集。再次使用线性回归作为点情况，我们研究下面有效链接子集分析的条件。  
&ensp;&ensp;首先，假设A和B之间有一个匹配。令$\left(A_{1}, A_{2}\right)$是A和$\left(B_{1}, B_{2}\right)$是B的一个双分区，其中$\left(A_{1}, B_{1}\right)$形成一个完整的匹配空间（CMS），这意味着记录$A_{1}$没有一个与记录$b < B_{1}$匹配。此外，$\left(A_{2}, B_{2}\right)$形成一个CMS，提供$\left(A_{1}, B_{1}\right)$形成一个CMS。设$X_{1}$和$X_{2}$分别为$a_{1}$与和$a_{2}$相关的回归设计矩阵。设$y_{1}$和$y_{1}$分别为与$b_{1}$和$b_{2}$相关的因变量的向量。对于给定的$\left(X_{1}, X_{2}\right)$，分别用y_{M 1}=\omega_{1} y_{1}和$y_{M 2}=\omega_{2} y_{2}$表示因变量的真实向量。A和B之间的真正匹配矩阵是块对角线矩阵，其中$\omega_{1}$和$\omega_{2}$是对角线上的块。设$g_{1}$和$g_{1}$分别为比较数据。我们说，如果$\left(A_{1}, B_{1}\right)$形成一个CMS，并且比较数据G1是非信息的，那么$\left(A_{1}, B_{1}\right)$形成一个$\left(A, B\right)$的非信息完全选择（NICS）。NICS $\left(A_{2}, B_{2}\right)$也是如此。  
引理1  &ensp;设$\left(A_{1}, A_{2}\right)$是A和$\left(B_{1}, B_{2}\right)$与B的双分法，其中$\left(A_{1}, B_{1}\right)$和$\left(A_{2}, B_{2}\right)$构成$\left(A, B\right)$的NICS。让$\hat{\beta}_{G}$、$\hat{\beta}_{G 1}$和$\hat{\beta}_{G 2}$分别由基于$\left(X, y\right)$、$\left(X_{1}, y_{1}\right)$和$\left(X_{1}, y_{2}\right)$的（2.2）给出。让$T_{1}=X_{1}^{T} Q_{1}^{T} Q_{1} X_{1}$和$T_{2}=X_{2}^{T} Q_{2}^{T} Q_{2} X_{2}$使用。让$r=T_{1}^{-1} T_{2}$和$\phi=(I+r)^{-1} r $。我们有  

$$
\hat{\beta}_{G}=(I-\phi) \hat{\beta}_{G 1}+(I-\phi) r \hat{\beta}_{G 2}=\hat{\beta}_{G 1}+\left[(I-\phi) r \hat{\beta}_{G 2}-\phi \hat{\beta}_{G 2}\right] \\
$$
证明：通过NICS，我们得到了$T=(Q X)^{T}(Q X)=T_{1}+T_{2}$, 当$Q_{1}=E\left(\omega_{T} \mid G\right)$ 为 $y_{M}=\omega_{y}$,$Q_{1}=E\left(\omega_{1}^{T} \mid G\right)$ for yM1 = ω1y1 和 $Q_{2}=E\left(\omega_{2}^{T} \mid G\right)for yM2 = ω2y2.同样地，我们也有$(Q X)^{T} y=X_{1}^{T} Q_{1}^{T} y_{1}+X_{2}^{T} Q_{2}^{T} y_{2}$。使用$T_{1}^{-1}-(I+r)^{-1} r T_{1}^{-1}=(I-\phi) T_{1}^{-1}$，我们得到  

$$
\hat{\beta}_{G}=(I-\phi) T_{1}^{-1}\left(X_{1}^{T} Q_{1}^{T} y_{1}+T_{2} T_{2}^{-1} X_{2}^{T} Q_{2}^{T} y_{2}\right)=(I-\phi) \hat{\beta}_{G 1}+(I-\phi) r \hat{\beta}_{G 2} \\
$$
请注意，虽然$\hat{\beta}_{G}$不仅仅是$\hat{\beta}_{G 1}$和$\hat{\beta}_{G 2}$的凸组合，但我们确实有$(I-\phi)+(I-\phi) r=I$，因为  

$$
\left.(I-\phi) r-\phi=\left[I-\phi-(I+r)^{-1}\right)\right] r=\left[I-(I+r)^{-1}(r+I)\right] r=0 \\
$$
因此，引理1表明，基于一个链接子集的回归是有效的，只要它是所有记录的某些NICS-分区的一部分。当然，除非FLR为零，否则我们不能确定用$\left(A_{L}, B_{L}\right)$表示的链接记录是否形成了$\left(A, B\right)$的NICS。但是，也可以考虑将记录链接作为识别一个可能的NICS的一种手段。设$\pi_{L}$为$\left(A_{L}, B_{L}\right)$形成NICS的概率。然后我们有$E\left(\hat{\beta}_{G L} \mid G, X\right)=\beta$，其中$\hat{\beta}_{G_L}$、由（2.2）给出，如果$\left(A_{L}, B_{L}\right)$形成一个NICS。此外，当$\left(A_{L}, B_{L}\right)$不形成NICS时，设ω(L)为真匹配矩阵$\omega_{n_{A}} \times n_{B}$的$n_{A} \times n_{L}$子矩阵，由对应于BL的ω列组成。提供$\omega_{(L)}^{T} \mathbf{1}=\mathbf{1}$，也就是说，所有的记录匹配即使他们不是所有，真正的回归设计矩阵的$X_{M L}=\omega_{(L)}^{T} X $.引理2下面显示$\hat{\beta}_{G}$的偏见是有限的概率$\left(A_{L}, B_{L}\right)$不形成CMS，即$1-\pi_{L}$ 。  
引理2  让$\hat{\beta}_{G L}=T_{L}^{-1}\left(X_{L} Q_{L}^{T} y_{L}\right)$，其中$T_{L}=X_{L}^{T} Q_{L}^{T} Q_{L} X_{L}$和QL计算为$\left(A_{L}, B_{L}\right)$形成一个NICS。设$f\left(\Omega_{L} \mid G\right)$为$\left(A_{L}, B_{L}\right)$形成NICS的概率。假设$\omega_{(L)}^{T} \mathbf{1}=\mathbf{1}$，其中$\omega_{(L)}$是$B_{L}$的真正匹配子矩阵，我们有  

$$
E\left(\hat{\beta}_{G L} \mid G, X\right)=\pi_{L} \beta+\left(1-\pi_{L}\right) T_{L}^{-1} X_{L}^{T} Q_{L}^{T} E\left(\omega_{(L)}^{T} \mid G\right) X \beta \\
$$
&ensp;&ensp;请注意，在$B_{L}$中不是所有的记录都在A中有匹配的情况下，如果不对BL中不匹配的y值做一些额外的假设，就不能给出$\hat{\beta}_{G L}$的期望。然而，很明显，在创建链接集$\left(A_{L}, B_{L}\right)$时，它有助于增加$\left(A_{L}, B_{L}\right)$形成CMS的概率。虽然很难评估大型数据集的概率πL，但限制FLR似乎有助于该课程，因为如果FLR为零，对于任何链接集，我们都必须有$\pi_{L}=1$。  
&ensp;&ensp;上述结果涉及调整后的$\hat{\beta}_{G L}$（2.2）。对于大的人口数据集，如果能够使用面值估计器，将会以一种更直接的方式更加实用。   

$$
\hat{\beta}_{L}=\left(X_{L}^{T} X_{L}\right)^{-1}\left(X_{L}^{T} y_{L}\right)
$$
基于引理1和引理2背后的推理，我们现在开发了一个基于大数据集的βˆL的渐近结果。  
&ensp;&ensp;设$\left(A_{ML}, A_{cL}\right)$为AL和设$\left(B_{ML}, B_{cL}\right)$与BL的双分区，其中$A_{ML}$包含正确链接到$B_{ML}$的$n_{M}$记录，其中$n_{M} \leq n_{L} $和$A_{cL}$的$n_{c} = n_{L}−n{M}$记录。让设$\left(X_{ML}, X_{cL}\right)$与设$\left(A_{ML}, A_{cL}\right)$和设$\left(y_{ML}, y_{cL}\right)$与$\left(B_{ML}, B_{cL}\right)$关联。让$T_{M L}=X_{M L}^{T} X_{M L}$，$T_{c L}=X_{c L}^{T} X_{c L}, r_{L}=T_{M L}^{-1} T_{c L} $和$\phi_{L}=\left(I+r_{L}\right)^{-1} r_{L}$。即使不知道哪些记录在$A_{ML}$和$B_{ML}$中，我们也有  

$$
\hat{\beta}_{L}=\left(X_{M L}^{T} X_{M L}+X_{c L}^{T} X_{c L}\right)^{-1}\left(X_{M L}^{T} y_{M L}+X_{c L}^{T} y_{c L}\right) \\
=\left(I-\phi_{L}\right) T_{M L}^{-1} X_{M L}^{T} y_{M L}+\left(I-\phi_{L}\right) r_{L} T_{c L}^{-1} X_{c L}^{T} y_{c L} \\
$$
假设ycL存在XMcL，其中$E\left(y_{c L} \mid X_{M c L}\right)=X_{M c L} \beta$，尽管BcL中的记录是错误链接的。考虑到大数据集和低FLR，我们提出了以下条件。渐近地，如nL→∞，设$\left(A_{L}, B_{L}\right)$被认为形成一个非信息平衡选择（NIBS）  

$
\text { (B1) } n_{M} / n_{L} \stackrel{P}{\rightarrow} \pi_{M}, \text { where } \pi_{M} \in(0,1] \\
$

$
\text { (B2) } n_{M}^{-1} X_{M L}^{T} X_{M L} \stackrel{P}{\rightarrow} \mu_{x} \mu_{x}^{T}+\Sigma_{x} \text { and } n_{c}^{-1} X_{c L}^{T} X_{c L} \stackrel{P}{\rightarrow} \mu_{x} \mu_{x}^{T}+\Sigma_{x} \\
$

$
\text { (B3) } n_{c}^{-1} X_{c L}^{T} X_{M c L} \stackrel{P}{\rightarrow} \mu_{x} \mu_{x}^{T} \\
$


例如，如果XML、XcL和XMcL是X的随机子集。  
定理1  提供了（B1）-（B3），渐近为$n_{L} \rightarrow \infty$，我们有  

$$
E\left(\hat{\beta}_{L}\right) \stackrel{P}{\rightarrow}\beta-\left(1-\pi_{M}\right)(I-\psi) \beta \\
$$

$$
n_{L} V\left(\hat{\beta}_{L}\right) \stackrel{P}{\rightarrow} \sigma^{2} \Delta_{x}^{-1} \\
$$

$
\text { where } \psi=\left(\mu_{x} \mu_{x}^{T}+\Sigma_{x}\right)^{-1} \mu_{x} \mu_{x}^{T} \text { and } \Delta_{x}=\mu_{x} \mu_{x}^{T}+\Sigma_{x} \\
$

证明：从（B1）和（B2）中，我们有$r_{L}\stackrel{P}{\rightarrow} I\left(1-\pi_{M}\right) / \pi_{M} $和$I-\phi_{L} \stackrel{P}{\rightarrow} \pi_{M} I$。对于（2.4）的第一项，我们可以得出这个结论  

$$
\left(I-\phi_{L}\right) T_{M L}^{-1} X_{M L} y_{M L} \stackrel{P}{\rightarrow} \pi_{M} \beta=\beta-\left(1-\pi_{M}\right) \beta \\
$$
对于（2.4）的第二项，从（B3）得出，$T_{c L}^{-1} X_{c L}^{T} X_{M c L} \stackrel{P}{\rightarrow} \psi$，即$\left(I-\phi_{L}\right) r_{L} T_{c L}^{-1} X_{c L}^{T} y_{c L} \stackrel{P}{\rightarrow}\left(1-\pi_{M}\right) \psi \beta$。结合这两项，可以得到第一个结果。对于ˆβL的方差，我们可以观察到  

$$
V\left(\hat{\beta}_{L}\right)=\left(I-\phi_{L}\right) V\left(\hat{\beta}_{M L}\right)\left(I-\phi_{L}\right)^{T}+\left(I-\phi_{L}\right) r_{L} T_{c L}^{-1} V\left(X_{c L}^{T} y_{c L}\right) T_{c L}^{-1} r_{L}^{T}\left(I-\phi_{L}\right)^{T} \\
$$

$
\text { 当 } \hat{\beta}_{M L}=T_{M L}^{-1} X_{M L}^{T} y_{M L} \text {. } \\
$
请注意，V（βˆL）并没有用$\left(X_{M L}, X_{c L}, X_{M c L}\right) $来指定，因为这些都没有被观察到。因此，使用作为a的NIBS链路子集的渐近偏差以FLR 1−πM为界，并给出了β的渐近偏差调整估计量为  

$$
\hat{\beta}_{A}=\left(I-\left(1-\pi_{M}\right)(I-\hat{\psi})\right)^{-1} \hat{\beta}_{L} \\ 
$$
估计量（2.5）计算简单，只需要由（2.4）的面值βˆL和XL的估计均值和协方差矩阵。  
## 2.5.2 C-PR数据的说明
上述结果为C-PR数据提供了一种实用的方法（表2.1），即只制作具有几乎为零的错误链接概率的链接，并基于产生的链接子集调整分析，即所有本来可以创建的链接。当这个链接子集中的所有记录都是真匹配时，它们必然会形成一个CMS，而调整问题将成为缺失的数据之一。开发调整这种链接子集的一般方法超出了这里的范围。下面我们将考虑一些广泛的替代方案，以及数据提供商和二级分析师的隐含成本和收益。  
&ensp;&ensp;考虑线性回归$y_{i}=x_{i}^{T} \beta+\epsilon_{i} $，其中yi和xi分别驻留在两个数据集中，而$\beta_{p \times 1}$是回归系数的向量。假设$\quad \operatorname{Cov}\left(\epsilon_{i}, \epsilon_{j}\right)=\sigma^{2}$，如果$i=j$，0，如果$i \neq j $。为了我们这里的目的，假设xi是标准化的，其中$\mu_{x}=E\left(x_{i}\right)=0$和$\Sigma_{x}=V\left(x_{i}\right)$，因此定理1中的$\psi=0 $和$V(\hat{\beta})=O\left(1 / n_{L}\right) $提供了NIBS链接子集。  
&ensp;&ensp;从表2.1中可以看出，超过97%的链接记录的FLR低于0.01，其中的例外情况是确定性传递8和两个概率传递。请注意，这两个概率传递对数据提供者来说是最昂贵的，同时与最大的flr相关联。  
&ensp;&ensp;考虑L1，由从第一个确定性通道开始的3000万条链路组成，其中的FLR低至0.00011。二级分析人员可以(i)假设NICS并获得基于L1（2.2）给出的βˆGL1，或（ii）假设NIBS并根据定理1（2.5）获得$\hat{\beta}_{A 1}=\hat{\beta}_{L 1} / \pi_{1}$，其中ψ = 0和βˆL1是基于L1和$1-\pi_{1}=0.00011$的面值OLS（2.4）。显然，对于检测到的FLR，NICS假设并非如此，因此选项(i)并不完全合理，正如第2.4.4节所讨论的，为L1计算$\mathrm{Q}_{1}=E\left(\omega_{1}^{\mathrm{T}} \mid G\right)$是不切实际的。相比之下，选项（ii）是简单的，并且避开了与条件分布$f(\omega \mid G)$相关的计算。假设NIBS假设，$\hat{\beta}_{L 1} $和βˆA1的合理性似乎是直观的低FLR。  
&ensp;&ensp;类似的推理也分别适用于所有其他链接子集L2，...，L11。现在考虑结合子集估计数$\hat{\beta}_{A k}=\hat{\beta}_{L k} / \pi_{k}$。让$S \subseteq${1,2，...，11}是一个索引集。一种基于s中的链路子集的组合估计器  

$$
\hat{\beta}_{A s}=\sum_{k \in s} w_{k} \hat{\beta}_{A k} \quad \text{和 }V\left(\hat{\beta}_{A s}\right)=\sum_{k \in s} w_{k}^{2} V\left(\hat{\beta}_{A k}\right) \\
$$
其中，$1 / w_{k}=v_{k} W$、$W=\sum_{k \in s} 1 / v_{k }$和vk是可选择的常数。vk的一个自然选择是$v_{k}=V\left(\hat{\beta}_{A k}\right)$，前提是NIBS假设适用于$k \in S$的每个子集Lk。另一种可能性是简单的$v_{k}=1 / n_{k} $，所以工作=nk/ns，$n_{s}=\sum_{k \in s} n_{k}$。如果NIBS假设在所有子集中都成立，那么这比$v_{k}=V\left(\hat{\beta}_{A k}\right) $的效率要低一些。但是，如果NIBS假设对于子集$L_{s}=\bigcup_{k \in s} L_{k}$的合并成立，但在每个子集中不是单独存在，那么它仍然是可信的。   

$$
\begin{table}[!htbp]
\centering
\caption{人口普查和患者登记链接子集回归的说明}
\label{tab:pagenum}
\begin{tabular}{llll}
\toprule
& 链接子集 &组合FLR & 标准错误顺序\\
\midrule
{1} &1 &1\\
{1,2,3,4,5,6,7,9} &1 &1\\
{1,2,3,4,5,6,7,8,9,10,11} &1 &1\\
\bottomrule
\end{tabular}
\end{table}
$$

$$
表2.5
\space \space 人口普查和患者登记链接子集回归的说明 \\
\begin{array}
{cll}
\hline
	链接子集  & 组合FLR  & 标准错误顺序 \\
\hline
	\{1\} &1.1 \times 10^{-4}  &1.80 \times 10^{-4} \\
	\{1,2,3,4,5,6,7,9\} &16.1 \times 10^{-4} &1.43 \times 10^{-4} \\
	\{1,2,3,4,5,6,7,8,9,10,11\} &25.2 \times 10^{-4} &1.41\times 10^{-4} \\
\hline
\end{array}
$$

&ensp;&ensp;表2.5显示了s的三个备选设置的一些汇总统计数据。组合的FLR由$1-\sum_{k \in s} n_{k} \pi_{k} / n_{s}$给出，标准误差（SE）的阶数为$O\left(1 / \sqrt{n_{s}}\right) $。第一种替代方案只使用$L_{1}$，提供了NIBS假设。第二种选择是使用flr低于0.01的8个子集。合并的FLR是单独的$L_{1}$的15倍，而SE有可能降低约20%。如果NIBS假设合理地支持相关子集的并集，则该替代方案可能近似有效。它确实需要为数据提供者做额外的工作。所有链接的记录都用于最终的选择。联合FLR比以前的替代方案高出约50%，而SE的潜在降低是最小的，可能不值得增加偏倚风险。如前所述，与直接确定性传递相比，这两个概率记录链接过程更需要资源。   
&ensp;&ensp;简而言之，基于具有接近零flr的链接子集的分析在所需的资源、二级分析人员和数据提供者的资源方面具有实际优势。似乎对潜在的连锁误差偏差的必要调整可能不那么复杂，并且由于比较数据模型的错误说明，可能具有较低的风险。  
## 2.6 结语
我们考虑了三种广泛的方法，关于辅助用户如何对不能没有错误地链接的数据集进行分析，提供相关记录之间的非分解比较数据。  
&ensp;&ensp;关于在尊重链接数据结构的模型下的MLE，目前仍然是一个有待解决的问题。对于一个旨在在单独的数据集中使用所有匹配的实体的分析，有两个关键的方法挑战。首先，可能需要更准确的比较数据模型，例如，以适应关键变量的异构失真误差，特别是对于小到中等大小的数据集。接下来，与条件分布$f(\omega \mid G)$相关的计算目前似乎无法伸缩。  
&ensp;&ensp;对于大种群数据集的分析，链接子集分析可以提供一个实用的替代方法。以上得到的结果，提供了渐近的NIBS链接子集，需要扩展，以处理不统一的或潜在的信息选择的链接子集。  
&ensp;&ensp;重要的是要观察数据提供者的关键角色，从我们的调查，准备数据集和传播适当的链接比较数据，为了二级分析师有可能进行有效的统计分析，并占的不确定性，因为不知道真正的匹配实体。  
### 参考文献
[1] Chambers, R.C. (2009). Regression Analysis of Probability Linked Data.Statisphere, Vol. 4: http://ro.uow.edu.au/eispapers/762/  
[2] Chambers, R.C. and Kim, G. (2015). Secondary Analysis of LinkedData. In Methodological Developments in Data Linkage (eds. K. Harron,H. Goldstein and C. Dibben), Chapter 5.  
[3] Chipperfield, J.O., Bishop, G.R. and Campell, P. (2011). Maximum likelihood estimation for contingency tables and logistic regression with incorrectly linked data. Survey Methodology, 37, 13–24.  
[4] Chipperfield, J.O. and Chambers, R.C. (2015). Using bootstrap to account for linkage errors when analysing probabilistically linked categorical data. Journal of Official Statistics, 31, 397–414.  
[5] Christen, P. (2012). A survey of indexing techniques for scalable record linkage and deduplication. ISEE Transactions on Knowledge and Data Engineering, 24.  
[6] Copas, J.B. and Hilton, F.J. (1990). Record linkage: Statistical models from matching computer records. Journal of the Royal Statistical Society,Ser. A, 153, 287–320.  
[7] DeGroot, M.H. and Goel, P.K. (1980). Estimation of the correlation coefficient from a broken random sample. The Annals of Statistics, 8, 264–278.  
[8] Fellegi, I.P. and Sunter, A.B. (1969). A theory for record linkage. Journal of the American Statistical Association, 64, 1183–1210.  
[9] Gilbert, R., Lafferty, R., Hagger-Johnson, G., Harron, K., Zhang,L-C., Smith, P., ... Goldstein, H. (2017). GUILD: GUidance for Information about Linking Data sets. Journal of Public Health, DOI:10.1093/pubmed/fdx037  
[10] Goldstein, H., Harron, K. and Wade, A. (2012). The analysis of recordlinked data using multiple imputation with data value priors. Statistics in Medicine, 31, 3481–3493.  
[11] Gutman, R., Afendulis, C.C. and Zaslavsky, A.M. (2013). A Bayesian procedure for file linking to analyze end-of-life medical costs. Journal of the American Statistical Association, 108, 34–47.  
[12] Gutman, R., Sammartino, C.J., Green, T.C. and Montague, B.T. (2015).Error adjustments for file linking methods using encrypted unique client identifier (eUCI) with application to recently released prisoners who are HIV+. Statistics in Medicine, 35, 115–129.  
[13] Herzog, T.N., Scheuren, F.J. and Winkler, W.E. (2007). Data Quality and Record Linkage Techniques. Springer.  
[14] Hof, M.H.P. and Zwinderman, A.H. (2012). Methods for analysing data from probabilistic linkage strategies based on partially identifying variables. Statistics in Medicine,31, 4231–4242.  
[15] Hof, M.H.P. and Zwinderman, A.H. (2015). A mixture model for the analysis of data derived from record linkage. Statistics in Medicine, 34,74–92.  
[16] Kim, G. and Chambers, R.C. (2012a). Regression analysis under incomplete linkage. Computational Statistics and Data Analysis, 56, 2756–2770.  
[17] Kim, G. and Chambers, R.C. (2012b). Regression analysis under probabilistic multi-linkage. Statistica Neerlandica, 66, 64–79.  
[18] Lahiri, P. and Larsen, M.D. (2005). Regression analysis with linked data. Journal of the American Statistical Association, 100, 222–230.  
[19] Orchard, T. and Woodbury, M.A. (1972). A missing information principle: theory and applications. Proc. Sixth Berkeley Symp. on Math. Statist. and Prob., Vol. 1, 697–715.   
[20] Owen, A., Jones, P. and Ralphs, M. (2015). Large-scale Linkage for Total Populations in Official Statistics. In Methodological Developments in Data Linkage (eds. K. Harron, H. Goldstein and C. Dibben), Chapter 8.  
[21] Sadinle, M. (2014). Detecting duplicates in a homicide registry using a Bayesian partitioning approach. Annals of Applied Statistics, 8, 2404–2434.  
[22] Scheuren, F. and Winkler, W. E. (1993). Regression analysis of data files that are computer matched. Survey Methodology, 19, 39–58.  
[23] Scheuren, F. and Winkler, W. E. (1997). Regression analysis of data files that are computer matched – Part II. Survey Methodology, 23, 157–165.  
[24] Stoerts, R., Hall, R. and Fienberg, S. (2016). A Bayesian approach tographical record linkage and de-duplication. Journal of the American Statistical Association, 111, 1660–1672.  
[25] Tancredi, A. and Liseo, B. (2013). A hierarchical Bayesian approachto record linkage and population size problems. The Annals of Applied Statistics, 5, 1553–1585.  
[26] Zhang, G. and Campbell, P. (2012). Data Survey:Developing the Statistical Longitudinal Census Dataset and identifying its potential uses.Australian Economic Review, 45, 125–133.  
