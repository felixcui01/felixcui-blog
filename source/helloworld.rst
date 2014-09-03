数学基础：
========
http://blog.csdn.net/pi9nc/article/details/8689982#comments
http://dec3.jlu.edu.cn/webcourse/t000022/teach/chapter3/3_2.htm


优化理论： 
=========
* 梯度下降GD：
    - 算法步骤


    - 迭代公式：  
*随机梯度下降SGD : <<机器学习>> 4.4.3节
    - 特点：Batch Gradient Descent使用了全量数据，环顾四周，找下降的方向走；Stochastic Gradient Descent则是使用当前点的数据，仅根据当前点就判断出来下降方向；前者有充足的信息来确定方向，但是使用全量数据计算量比较大，后者仅根据当前点确定迭代方向，速度快但是准确性低，有可能会进入局部最优值。
    - 迭代公式： 

*牛顿法： 

*拟牛顿法：
    - L-BFGS

* 参考：
    http://blog.csdn.net/itplus/article/details/21896453
    http://www.52nlp.cn/unconstrained-optimization-one


机器学习三要素
===========
* 模型： 
    模型空间，具体的参数待学习；
    决策函数或条件概率分布模型；
* 策略：
    经验风险最小化；
    结构风险（加入正则化项）最小化（经验风险和模型复杂度同时小）；
* 算法： 
    使用最优化算法求模型参数；

分类
======

感知机
----------
场合： 二分类
模型：        w.z+b>=0时为1，<0时为-1；
学习策略： 极小化经验损失函数（误分类的点到超平面的距离之和）
    
学习算法： 随机梯度下降，拉格朗日对偶算法
http://blog.csdn.net/stan1989/article/details/8565499

逻辑回归
------------
* 场合：二类或多类
* 模型：可以看成是概率模型，也可看做非概率模型 

      选择概率大的那个分类
* 学习策略：极大似然估计，或极小化logisti损失


* 学习算法：梯度下降，拟牛顿法
* 参考：
http://blog.csdn.net/zouxy09/article/details/20319673
http://www.cnblogs.com/zhangchaoyang/articles/2640700.html
http://www.cnblogs.com/biyeymyhjob/archive/2012/07/18/2595410.html
http://52opencourse.com/125/coursera%E5%85%AC%E5%BC%80%E8%AF%BE%E7%AC%94%E8%AE%B0-%E6%96%AF%E5%9D%A6%E7%A6%8F%E5%A4%A7%E5%AD%A6%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%E7%AC%AC%E5%85%AD%E8%AF%BE-%E9%80%BB%E8%BE%91%E5%9B%9E%E5%BD%92-logistic-regression
<机器学习导论> 10.7

SVM
----------
* 场合：二类或多类
* 模型：
       w.z+b>0时为1，<0时为-1；
    线性可分:  硬间隔（几何间隔）最大化
    线性不可分： 软间隔最大化 
    非线性：核函数包括多项式核函数，高斯核函数，字符串核函数等；
* 学习策略：极小化合页损失（hinge loss)，最大化分类间隔 => 拉格朗日对偶
* 学习算法： 凸二次规划，SMO
* 参考
http://blog.csdn.net/v_july_v/article/details/7624837
http://www.cnblogs.com/LeftNotEasy/archive/2011/05/02/basic-of-svm.html
http://www.cnblogs.com/wangbogong/p/3148668.html
http://www.svms.org/
libsvm： http://jacoxu.com/?p=118

决策树
-----------
模型： 基于特征对实例进行分类的树形结构；包括三种算法ID3， C4.5， CART；
学习算法： 特征选择，剪枝；    
http://blog.csdn.net/v_july_v/article/details/7577684
http://www.docin.com/p-511267944.html
http://www.cnblogs.com/LeftNotEasy/archive/2011/03/07/random-forest-and-gbdt.htm

贝叶斯
--------------
朴素贝叶斯
模型： 
学习策略： 0-1损失函数时的 期望风险最小化
学习方法：最大似然估计，贝叶斯估计
参考：
http://www.ruanyifeng.com/blog/2013/12/naive_bayes_classifier.html
http://mindhacks.cn/2008/09/21/the-magical-bayesian-method/
http://sobuhu.com/ml/2012/11/11/navie-bayes-classify.html

 贝叶斯网络
http://www.cnblogs.com/leoo2sk/archive/2010/09/18/bayes-network.html
http://txt.wenku.baidu.com/view/3d4e12cf83d049649b6658af.html
http://wenku.baidu.com/view/c5c381232f60ddccda38a096.html


KNN
-------- 
重点是各种距离的选择
http://blog.csdn.net/luowen3405/article/details/6275254
相似度：http://blog.csdn.net/pi9nc/article/details/9068359
            马氏距离分类：http://blog.sina.com.cn/s/blog_4e24d9c501011p8y.html
模型： 多数表决
学习策略： 经验风险最小，多数表决
搜索算法： kd树，加速搜索最近邻

Adaboost
-------------
* adative boost，组合多个弱分类器，构成一个强分类器
* 模型： am，子分类器的系数
* 学习策略： 极小化损失函数
* 学习算法： 前向分步算法
* 提升树：以分类树或回归树为基本分类器的提升方法


参数估计
------------
贝叶斯估计和极大似然估计
http://www.open-open.com/doc/view/9e9eee699d1249c1be13ebd1dac11a15

EM算法
    含有隐含变量的概率模型参数的极大似然估计算法，包括两步，求Expection和Maximization
    http://blog.csdn.net/zouxy09/article/details/8537620


多分类问题
--------------
利用二分类构建多分类；
http://blog.sina.com.cn/s/blog_5eef0840010147pa.html


其他
----------
隐马尔科夫模型
http://blog.csdn.net/eaglex/article/details/6376826
http://blog.csdn.net/v_july_v/article/details/7577684

费希尔判别
http://wenku.baidu.com/link?url=QXNoYtXnNG9LeQrz_XHxGTpp92Z1BxiPY18dD5ayFSW-2a12d5ET0EodIpdYU4xNjSXX24llL-66uBkMWaJrSAApZfytNMwX7JW3y_Iazh7
http://wenku.baidu.com/link?url=djVOU5HwMM3OkdE9v2E1ghdl3z23Fn9_Q2980pJ66eE3u3g0FRgoyK0LBfCuoZb1uVWIq0AUVKLtDhokyzNxEQoU50Dr_8CVIaqFmivwRP7

受限玻尔兹曼机
http://www.cnblogs.com/kemaswill/p/3203605.html

转导推理
http://www.cnblogs.com/siegfang/p/3424003.html


回归
============
线性回归
-------------
* 一般回归
    - 模型： 
    - 学习策略：最小化公式
    - 两种学习方法：
        + 梯度下降：
        + 矩阵公式： 
    - 过拟合问题
        + 

* ridge回归
    - L2正则化，解决过拟合问题
    - ridge（岭）回归得到的系数是稠密的，即系数都为非零值，因此做预测时，所有的特征都会用到，模型的可解释性不强
    
* lasso回归
    - L1正则化，解决过拟合问题
    - Lasso得到的系数是稀疏的，因此相对于岭回归，Lasso还有特征选择的作用
    - Ridge 和LASSO的算法的不同点在于如果惩罚参数增加，Ridge 估计参数减小但是仍然会保持在非零(Non-Zero)，而在LASSO中，惩罚参数增加会将估计参数压缩到零。

* 局部加权线性回归 
    - 解决线性回归欠拟合的问题    
    - 学习策略：       
                         
    - 回归解： 
    - 特点： 需要利用全量数据，每次进行预测或者分类时都进行计算；针对每一个x，训练训练对应的theta；
        
* 参考
http://blog.sina.com.cn/s/blog_68c81f3901019hhp.html
http://www.cnblogs.com/LeftNotEasy/archive/2010/12/19/mathmatic_in_machine_learning_2_regression_and_bias_variance_trade_off.html
http://blog.csdn.net/allenalex/article/details/16370245
http://blog.sina.com.cn/s/blog_6a1b8c6b0101id09.html
http://www.cnblogs.com/hseagle/p/3908276.html (spark 线性回归分析)

回归树
----------
http://www.tuicool.com/articles/JvMJve
http://blog.csdn.net/zhangchaoyangsun/article/details/8461786 cart回归


降维
====================
PCA 
-----------
（Principal Component Analysis）
重要特征提取
http://www.cnblogs.com/jerrylead/archive/2011/04/18/2020209.html 有计算详细步骤
http://blog.csdn.net/u010545732/article/details/18886933

SVD
---------
（Singular Value Decomposition）

推荐系统中通常将高维映射到低维后，计算相似度；
http://www.cnblogs.com/LeftNotEasy/archive/2011/01/19/svd-and-applications.html
http://blog.csdn.net/abcjennifer/article/details/8131087
http://blog.sina.com.cn/s/blog_642c9bdd01010bu5.html


正则化
========
L1范数： 模型特征选择
L2范数： 接近过拟合
http://blog.csdn.net/zouxy09/article/details/24971995


分类器评价指标
==============
ROC
    http://alexkong.net/2013/06/introduction-to-auc-and-roc/
http://www.tuicool.com/articles/uyaUZr


TODO
=========
各种方法的使用场景？ 
优缺点？
具体实践，spark如何用？


参考文档：
========
正则化和归一化 http://www.51weixue.com/thread-110-1-1.html
比较好的总结
http://www.cnblogs.com/tornadomeet/p/3395593.html
http://blog.csdn.net/v_july_v/article/category/1061301
http://www.cnblogs.com/zhangchaoyang/archive/2012/08/28/2660929.html
http://blog.csdn.net/lantian0802/article/details/38333479

ml-ng笔记： http://www.holehouse.org/mlclass/

