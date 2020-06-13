[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

PMF of Actual Data (Number of Kids in Household)
```python
import thinkstats2
resp = nsfg.ReadFemResp()
pmf_kdhh_actual = thinkstats2.Pmf(resp.numkdhh, label='actual')
```

PMF of Bias Data (Number of Kids in Household)
```python
pmf_kdhh_bias = pmf_kdhh_actual.Copy(label='bias')
for x,y in pmf_kdhh_actual.Items():
    pmf_kdhh_bias[x] = pmf_kdhh_actual[x]*x
pmf_kdhh_bias.Normalize()
pmf_kdhh_bias.Total()
```

Plot both PMFs
```python
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf_kdhh_actual, pmf_kdhh_bias]) 
thinkplot.Show(xlabel='number of kids in household', ylabel='PMF');
```
![Image of KidsHH Plot](https://github.com/matthewywang/dsp/blob/master/lessons/statistics/Actual_vs_Bias_Data_KidsHH.png)

Mean - Actual Data vs Bias Data
```python
pmf_kdhh_actual.Mean()
```
1.0242
```python
pmf_kdhh_bias.Mean()
```
2.4037

