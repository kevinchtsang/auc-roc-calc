## AUC-ROC Online Calculator for a Single Point

Although it is best to estimate the receiver operating characteristic (ROC) curve using multiple coordinates of sensitivity and specificity, this is not always possible. Here, we will use the esimation given by Zhang and Mueller [[1]](https://link.springer.com/article/10.1007/s11336-003-1119-8).

### Summary of method
The lower and upper bounds of the AUC (Area under ROC curve) given a single point (x = 1-specificity, y = sensitivity) can be estimated geometrically. The lower bound is the area of the quadrilateral defined between (0,0), point p, (1,1), and (1,0) which is  

<!-- 0.5*(sensitivity + specificity) -->

<img src="https://render.githubusercontent.com/render/math?math=A_{min}=\frac{(sensitivity%2Bspecificity)}{2}">

There are three cases of ROC curves, in the most general case, the curve has five (three non-axis) line segments; in the other two cases, one of the line segments degenerates to a point. Depending on where is the point of data, there is a different upper bound (see below). The AUC can be approximated as the mean of the maximum area and minimum area.

Let *F* denote (false alarm rate) false positive rate = 1 - specificity; *H* denote (hit rate) true positive rate = sensitivity

<!-- A_max -->
<img src="https://render.githubusercontent.com/render/math?math=A_{max}=1 - 2F ( 1 - H)"> if <img src="https://render.githubusercontent.com/render/math?math=F \leq 0.5 <H ">

<img src="https://render.githubusercontent.com/render/math?math=A_{max}=1 - \frac{F}{1 - H}"> if <img src="https://render.githubusercontent.com/render/math?math=F \leq H<0.5">

<img src="https://render.githubusercontent.com/render/math?math=A_{max}=1 - \frac{1 - H}{2(1 - F)}"> if <img src="https://render.githubusercontent.com/render/math?math=0.5<F \leq H ">

### Calculator
