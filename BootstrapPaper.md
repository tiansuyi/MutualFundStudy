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

��������ģ��

$$r_{i,t}=\alpha_{i}+\beta_{i}*RMRF{t}+s_{i}*SMB_{T}+h_{i}*HML_{t}+p_{i}*PR1YR_{t}+\epsilon_{i,t}$$

$$r_{i,t}=\alpha_{i}+\beta_{i}*RMRF{t}+s_{i}*SMB_{T}+h_{i}*HML_{t}+p_{i}*PR1YR_{t}+\sum_{j=1}^{K}B_{i,j}[z_{j,t-1}*RMRF_{t}]+\epsilon_{i,t}$$

### B1.baseline bootstrap procedure:residual sampling

���ȣ�������OLS����

�̶�i��OLS�Ĳв�panel�س���������pseudo-time series

���滻model�еĲвͬʱset alpha=0��������������������

���������ظ�1000�飬���µ����������ݷֲ�

�����ɵ���ʵ�ʵ���ȣ�������߲��Զ������Ϊ��skill ��rather than luck.

DATA��һЩ����ͳ������
-----------------------
Empirical Resaults
-----------------------
### Normality of Individual Fund Alphas

�Խϸ߸��ʾܾ���̬����

### Bootstrap Analysis of Significant of Alpha Outliers

1��outperform���������10%�Ļ��𣩵Ļ����alpha��tͳ�������Թ��Ʒ����׼�����ͳ���������ܸ�
2��bootsrap���pֵ�Ͷ�Ӧ�������ˣ����ֳ���t�ֲ�������

### Bootstrap test of Subperiods
### Bootstrap test of investment objective subgroups
growth-oriented fund outperform income-oriented fund

Sensitivity Analysis-robust
-------------------------
### time series dependence
ͨ���Բ�ͬ���ȵĲв���ڳ����������������� �����������tͳ������Bootstrap���Bootstrap����֮ǰ�Ľ���һ��

### Residual and Factor Resampling
������˲в�����ع��factors���ᱻ�س�������Ȼ�������֮ǰ�����ͬ

###Cross-sectional Bootstrap
��֮ǰ��ͬ��֮ǰ���س�individual���������ǹ̶�T�������н���Ĳв��������ǣ�������֮ǰһ��

