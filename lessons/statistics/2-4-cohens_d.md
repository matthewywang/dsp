[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Yes, first babies are lighter than later babies.  <br>
Cohen's d = -0.08867 (weight of first babies vs later babies).  <br>
This is larger and in the opposite direction compared to Cohen's d for pregnancy length, which was 0.02888.

`<addr>` *Code (Cohen's d preg length - first babies vs later babies)*  <br>
    CohenES_prglngth = thinkstats2.CohenEffectSize(firsts.prglngth, others.prglngth)   <br>
    CohenES_prglngth

*Code (Cohen's d weight - first babies vs later babies)*     
    first_wgt = firsts['totalwgt_lb']     <br>
    others_wgt = others['totalwgt_lb']     <br>
    thinkstats2.CohenEffectSize(first_wgt, others_wgt)
