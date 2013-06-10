A Bootstrap Study of Mutual Fund
=================================
Preface-Opinions from the first section
---------------------------------
1.Perform a study on mutual fund to see whether the prolonged superior performance of some funds is purely luck.

2.Genuine stock-picking skills or persisting luck(or can luck persist?how to exam?).

3.The question of this paper:With mutual fund alphas that deviate significantly from normality,how many funds from a large group would we expect to exhibit high alphas simply due to luck,and how does this figure compare to the number we actually observe?

4.The key of their study is the bootstrap analysis that allows them to precisely separate luck from skill in the complicated nonnormal cross section of ranked mutual fund alphas.(?)

5.net-of-cost vs pre-cost.

6.Study of persistence is similar to Cahart(1997).

7.Identifying funds with significant skills and somewhat decreasing returns-to scale in managers' talents.

Bootstrapping Procedure
-------------------------------------------------
### A1.Individual Munual Funds Alphas

Bootstrap can improve the nonnormalize thing

### A2.Cross Section of Mutual Fund Alphas

A lot of factors(such as heterogeneity and individual distribution) leads to the bootstrap a best method.

### B.Implementation

two models

两个线性模型

$$r_{i,t}=\alpha_{i}+\beta_{i}*RMRF{t}+s_{i}*SMB_{T}+h_{i}*HML_{t}+p_{i}*PR1YR_{t}+\epsilon_{i,t}$$

$$r_{i,t}=\alpha_{i}+\beta_{i}*RMRF{t}+s_{i}*SMB_{T}+h_{i}*HML_{t}+p_{i}*PR1YR_{t}+\sum_{j=1}^{K}B_{i,j}[z_{j,t-1}*RMRF_{t}]+\epsilon_{i,t}$$

### B1.baseline bootstrap procedure:residual sampling

首先：对数据OLS估计

固定i对OLS的残差panel重抽样，生成pseudo-time series

再替换model中的残差，同时set alpha=0，重新生成收益率数据

上述步骤重复1000遍，看新的收益率数据分布

把生成的与实际的相比：如果二者差很远，就认为是skill ，rather than luck.

DATA和一些基本统计描述
-----------------------
Empirical Resaults
-----------------------
### Normality of Individual Fund Alphas

以较高概率拒绝正态假设

### Bootstrap Analysis of Significant of Alpha Outliers

1、outperform（例如最高10%的基金）的基金的alpha和t统计量（以估计方差标准化后的统计量）都很高
2、bootsrap后的p值就对应的升高了，呈现出了t分布的特征

### Bootstrap test of Subperiods
### Bootstrap test of investment objective subgroups
growth-oriented fund outperform income-oriented fund

Sensitivity Analysis-robust
-------------------------
### time series dependence
通过对不同长度的残差的在抽样来弱化不独立的 ，结果是所有t统计量（Bootstrap与非Bootstrap）和之前的结论一样

### Residual and Factor Resampling
这里，除了残差项，连回归的factors都会被重抽样，显然，这会与之前结果相同

### Cross-sectional Bootstrap
与之前不同（之前是重抽individual），现在是固定T，把所有截面的残差冲抽样考虑，结论与之前一样

### portfolios of fund
通过构架不同分位数的基金组合，对组合的表现进行检测，同样，结论没变化

### Length of Data Records
因为short-live fund较long-live fund有更多的极端值,作者用long-live fund试，结论不变

### Persisted omitted facto in fund residual
作者指一些未被考虑到residual里的重要变量会被归因为manager talent

作者认为他选的短期fund不存在这种factor，另对residual用了AR(1)（没看懂ar（1）目的）

### bootstrap test for stockholding-based alphas
matching each stock with a value-weighted portfolio of the same stock

i.e.
$$CS_{t}=\sum_{j=1}^{N}w_{j,t-1}(R_{j,t}-R_{t}^{b_{j},t-1})$$
其中，$w_{j,t-1}$是股票j在t-1时刻的权重，$R_{j,t}$是股票j在时区t的回报，$R_{t}^{b_{j},t-1}$是t时刻投资组合的回报

同样的道理，作者对每一个股票都计算了CS，然后又通过重抽样的方法检验t统计量，结果同上
Performance Persistence
--------------------------------
Carhart(1997)

在本文里，作者用滞后的residual的“错位”相加检验“持续性”
Conclusion
--------------------------------
no luck,management skill
