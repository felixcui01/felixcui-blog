

数学基础：
=======
方差

优化理论： 
=========
梯度下降GD：

随机梯度下降SGD : <<机器学习>> 4.4.3节 
牛顿： 
拟牛顿法等：

分类
==========
感知机
场合： 二分类
模型：        w.z+b>=0时为1，<0时为-1；
学习策略： 极小化经验损失函数（误分类的点到超平面的距离之和）
    
学习算法： 随机梯度下降，拉格朗日对偶算法


KNN： 重点是各种距离的选择
http://blog.csdn.net/luowen3405/article/details/6275254
相似度：http://blog.csdn.net/pi9nc/article/details/9068359
            马氏距离分类：http://blog.sina.com.cn/s/blog_4e24d9c501011p8y.html
模型： 多数表决
学习策略： 经验风险最小，多数表决
搜索算法： kd树，加速搜索最近邻


逻辑回归：
场合：二类或多类
模型：可以看成是概率模型，也可看做非概率模型 

      选择概率大的那个分类
学习策略：极大似然估计，或极小化logisti损失


学习算法：梯度下降，拟牛顿法
参考：
http://blog.csdn.net/zouxy09/article/details/20319673
http://www.cnblogs.com/zhangchaoyang/articles/2640700.html
http://www.cnblogs.com/biyeymyhjob/archive/2012/07/18/2595410.html
http://52opencourse.com/125/coursera%E5%85%AC%E5%BC%80%E8%AF%BE%E7%AC%94%E8%AE%B0-%E6%96%AF%E5%9D%A6%E7%A6%8F%E5%A4%A7%E5%AD%A6%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0%E7%AC%AC%E5%85%AD%E8%AF%BE-%E9%80%BB%E8%BE%91%E5%9B%9E%E5%BD%92-logistic-regression
<机器学习导论> 10.7

SVM：
场合：二类或多类
模型：
       w.z+b>0时为1，<0时为-1；
    线性可分:  硬间隔（几何间隔）最大化
    线性不可分： 软间隔最大化 
    非线性：核函数包括多项式核函数，高斯核函数，字符串核函数等；
学习策略：极小化合页损失（hinge loss)，最大化分类间隔 => 拉格朗日对偶
学习算法： 凸二次规划，SMO
http://www.cnblogs.com/LeftNotEasy/archive/2011/05/02/basic-of-svm.html
http://www.cnblogs.com/wangbogong/p/3148668.html
http://www.svms.org/


决策树
http://blog.csdn.net/v_july_v/article/details/7577684
http://www.docin.com/p-511267944.html
http://www.cnblogs.com/LeftNotEasy/archive/2011/03/07/random-forest-and-gbdt.htm

朴素贝叶斯：
http://www.ruanyifeng.com/blog/2013/12/naive_bayes_classifier.html
http://mindhacks.cn/2008/09/21/the-magical-bayesian-method/
http://sobuhu.com/ml/2012/11/11/navie-bayes-classify.html

贝叶斯网络
http://www.cnblogs.com/leoo2sk/archive/2010/09/18/bayes-network.html
http://txt.wenku.baidu.com/view/3d4e12cf83d049649b6658af.html
http://wenku.baidu.com/view/c5c381232f60ddccda38a096.html、

贝叶斯估计和极大似然估计
http://www.open-open.com/doc/view/9e9eee699d1249c1be13ebd1dac11a15
http://blog.csdn.net/zouxy09/article/details/8537620

隐马尔科夫模型
http://blog.csdn.net/eaglex/article/details/6376826
http://blog.csdn.net/v_july_v/article/details/7577684

费希尔判别
http://wenku.baidu.com/link?url=QXNoYtXnNG9LeQrz_XHxGTpp92Z1BxiPY18dD5ayFSW-2a12d5ET0EodIpdYU4xNjSXX24llL-66uBkMWaJrSAApZfytNMwX7JW3y_Iazh7
http://wenku.baidu.com/link?url=djVOU5HwMM3OkdE9v2E1ghdl3z23Fn9_Q2980pJ66eE3u3g0FRgoyK0LBfCuoZb1uVWIq0AUVKLtDhokyzNxEQoU50Dr_8CVIaqFmivwRP7

感知器算法
http://blog.csdn.net/stan1989/article/details/8565499

受限玻尔兹曼机
http://www.cnblogs.com/kemaswill/p/3203605.html

转导推理
http://www.cnblogs.com/siegfang/p/3424003.html

基于规则的分类器
决策树是其中一种


回归
==================
线性回归：
http://blog.sina.com.cn/s/blog_68c81f3901019hhp.html
http://www.cnblogs.com/LeftNotEasy/archive/2010/12/19/mathmatic_in_machine_learning_2_regression_and_bias_variance_trade_off.html

回归树：
http://www.tuicool.com/articles/JvMJve
http://blog.csdn.net/zhangchaoyangsun/article/details/8461786 cart回归

降维
====================
PCA
http://www.cnblogs.com/jerrylead/archive/2011/04/18/2020209.html


TODO
=========
各种方法的使用场景？


附：
正则化和归一化 http://www.51weixue.com/thread-110-1-1.html

机器学习笔记： http://www.cnblogs.com/tornadomeet/p/3395593.html
数据挖掘数理统计知识： http://blog.csdn.net/pi9nc/article/details/8689982#comments
比较好的总结
http://blog.csdn.net/v_july_v/article/category/1061301
http://www.cnblogs.com/zhangchaoyang/archive/2012/08/28/2660929.html


