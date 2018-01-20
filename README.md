## 线性回归
[practice0112](https://github.com/morening/LearnML/blob/master/linear_regression/practice0112.py)

拟合 y = a*x1 + b*x2 + c

训练集 x:[[1, 2], [2, 1], [2, 3], [3, 5], [1, 3], [4, 2], [7, 3], [4, 5], [11, 3], [8, 7]]

训练集 y:[7, 8, 10, 14, 8, 13, 20, 16, 28, 26]

测试集 x:[[1, 4], [2, 2], [2, 5], [5, 3], [1, 5], [4, 1]]

**测试结果**
```
计算轮次：4009，耗时：0.434706，最小误差：0.000001
a = 2.000087
b = 1.000458
c = 2.997658
#测试：
[6.9986617712594938, 7.998290420402709, 9.9992069599056101, 14.00021041830318, 7.9991200410109435, 12.998922527943494, 19.999641554378947, 16.000297337197846, 27.999989229957613, 26.001561552279416]
#计算：
[8.999578310762395, 8.9987486901541605, 12.000123499408513, 15.99946771658961, 10.000036580513846, 11.998464258192042]
```

<img width="50%" height="50%" src="https://github.com/morening/LearnML/blob/master/snapshot/linear_regression/practice0112.png?raw=true" />

最后，感谢[《梯度下降原理及Python实现》](http://blog.csdn.net/programmer_wei/article/details/51941358)的帮助与指导，令我深刻理解梯度下降法的原理和完成python实现。

## 线性回归（矩阵）
[practice0115](https://github.com/morening/LearnML/blob/master/linear_regression/practice0115.py)

设 y = theta0 + theta1*x1 + theta2*x2

**测试结果**
```
#参数拟合：
[[ 2.9999716 ]
 [ 2.00000105]
 [ 1.00000556]]
#轮次：6528
#测试结果：
[[  6.99998377]
 [  7.99997927]
 [  9.99999038]
 [ 14.00000255]
 [  7.99998933]
 [ 12.99998693]
 [ 19.99999565]
 [ 16.00000361]
 [ 27.99999987]
 [ 26.00001894]]
```

## 逻辑回归

### 测试结果（[data1](https://github.com/morening/LearnML/blob/master/data/logistic_regression/data1.txt)）

***一阶拟合***

```
#参数拟合：
[[-280.76963691]
 [   2.64287161]
 [   1.98393109]]
#正确率：92.0%
#测试结果：
[[  1.07319525e-15]
 [  4.42892157e-50]
 [  1.05119846e-18]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  2.14759841e-22]
 [  1.00000000e+00]
 [  9.99948356e-01]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  3.39548891e-10]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  9.09687815e-12]
 [  1.00000000e+00]
 [  9.98353316e-01]
 [  1.86340791e-04]
 [  1.00000000e+00]
 [  9.99999961e-01]
 [  2.00405482e-08]
 [  1.00000000e+00]
 [  1.44882945e-22]
 [  2.64702210e-45]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  9.99999998e-01]
 [  1.00000000e+00]
 [  2.14898366e-08]
 [  3.81937603e-22]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.83418388e-08]
 [  4.19230161e-03]
 [  3.67661156e-15]
 [  5.76301349e-15]
 [  9.93404975e-01]
 [  1.00000000e+00]
 [  3.46954688e-01]
 [  1.33151719e-18]
 [  1.00000000e+00]
 [  3.98874970e-23]
 [  1.00000000e+00]
 [  9.99999975e-01]
 [  1.36908331e-24]
 [  2.17675534e-06]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  5.34702346e-31]
 [  4.93701639e-22]
 [  3.23689090e-14]
 [  1.00000000e+00]
 [  6.61782487e-03]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.19539567e-41]
 [  2.87507466e-24]
 [  1.96864105e-45]
 [  3.86293428e-14]
 [  7.34917872e-11]
 [  9.99999997e-01]
 [  1.23349461e-21]
 [  1.00000000e+00]
 [  9.99999940e-01]
 [  8.62910776e-48]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  9.99999997e-01]
 [  9.51953113e-01]
 [  1.19931816e-16]
 [  9.99999999e-01]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.09424428e-05]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.95134375e-06]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  3.21484293e-10]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  2.47143486e-28]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  1.00000000e+00]
 [  9.76584208e-01]
 [  1.00000000e+00]
 [  3.35954358e-03]
 [  1.00000000e+00]]
```

<img width="50%" height="50%" src="https://github.com/morening/LearnML/blob/master/snapshot/logistic_regression/practice0114_data1.png?raw=true" />

### 测试结果（[data2](https://github.com/morening/LearnML/blob/master/data/logistic_regression/data2.txt)）

***四阶拟合***

```
#拟合阶次：4

#正确率：85.59322033898306%

#拟合轮次：6469

#拟合参数：
[[ 3.20336492]
 [ 3.42216743]
 [-4.82267847]
 [-0.9102518 ]
 [-4.10029314]
 [ 2.05013743]
 [-4.26437115]
 [-0.75903534]
 [-1.05585157]
 [-5.70498231]
 [-1.21458307]
 [-1.40552181]
 [ 0.6064388 ]
 [ 0.50207037]
 [-4.64027097]]

#测试结果
[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 1, 0, 1, 0, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 1]
```

<img width="50%" height="50%" src="https://github.com/morening/LearnML/blob/master/snapshot/logistic_regression/practice0114_data2.png?raw=true" />

## KNN

### 测试结果（[datingTestSet2](https://github.com/morening/LearnML/blob/master/data/knn/datingTestSet2.txt)）

```
# K = 10

# 准确度：90.0%

# 测试结果：

[  4.68930000e+04   3.56297600e+00   4.45386000e-01   1.00000000e+00] 1.0
[  8.17800000e+03   3.23048200e+00   1.33169800e+00   2.00000000e+00] 2.0
[  5.57830000e+04   3.61254800e+00   1.55191100e+00   1.00000000e+00] 1.0
[  1.14800000e+03   0.00000000e+00   3.32365000e-01   2.00000000e+00] 2.0
[  1.00620000e+04   3.93129900e+00   4.87577000e-01   2.00000000e+00] 2.0
[  7.41240000e+04   1.47523420e+01   1.15516000e+00   1.00000000e+00] 1.0
[  6.66030000e+04   1.02618870e+01   1.62808500e+00   1.00000000e+00] 1.0
[  1.18930000e+04   2.78726600e+00   1.57040200e+00   2.00000000e+00] 2.0
[  5.09080000e+04   1.51123190e+01   1.32413200e+00   3.00000000e+00] 1.0
[  3.98910000e+04   5.18455300e+00   2.23382000e-01   3.00000000e+00] 3.0
[  6.59150000e+04   3.86835900e+00   1.28078000e-01   1.00000000e+00] 1.0
[  6.56780000e+04   3.50796500e+00   2.89040000e-02   1.00000000e+00] 1.0
[  6.29960000e+04   1.10192540e+01   4.27554000e-01   1.00000000e+00] 1.0
[  3.68510000e+04   3.81238700e+00   6.55245000e-01   1.00000000e+00] 1.0
[  3.66690000e+04   1.10567840e+01   3.78725000e-01   3.00000000e+00] 3.0
[  3.88760000e+04   8.82688000e+00   1.00232800e+00   3.00000000e+00] 3.0
[  2.68780000e+04   1.11738610e+01   1.47824400e+00   3.00000000e+00] 3.0
[  4.62460000e+04   1.15064650e+01   4.21993000e-01   3.00000000e+00] 3.0
[  1.27610000e+04   7.79813800e+00   1.47917000e-01   3.00000000e+00] 2.0
[  3.52820000e+04   1.01550810e+01   1.37003900e+00   3.00000000e+00] 3.0
[  6.83060000e+04   1.06452750e+01   6.93453000e-01   1.00000000e+00] 1.0
[  3.12620000e+04   9.66320000e+00   1.52154100e+00   3.00000000e+00] 3.0
[  3.47540000e+04   1.07904040e+01   1.31267900e+00   3.00000000e+00] 3.0
[  1.34080000e+04   2.81053400e+00   2.19962000e-01   2.00000000e+00] 2.0
[  3.03650000e+04   9.82599900e+00   1.38850000e+00   3.00000000e+00] 3.0
[  1.07090000e+04   1.42131600e+00   6.77603000e-01   2.00000000e+00] 2.0
[  2.43320000e+04   1.11232190e+01   8.09107000e-01   3.00000000e+00] 3.0
[  4.55170000e+04   1.34022060e+01   6.61524000e-01   3.00000000e+00] 3.0
[  6.17800000e+03   1.21225500e+00   8.36807000e-01   2.00000000e+00] 2.0
[  1.06390000e+04   1.56844600e+00   1.29746900e+00   2.00000000e+00] 2.0
[  2.96130000e+04   3.34347300e+00   1.31226600e+00   1.00000000e+00] 1.0
[  2.23920000e+04   5.40015500e+00   1.93494000e-01   1.00000000e+00] 3.0
[  5.11260000e+04   3.81875400e+00   5.90905000e-01   1.00000000e+00] 1.0
[  5.36440000e+04   7.97384500e+00   3.07364000e-01   3.00000000e+00] 1.0
[  5.14170000e+04   9.07882400e+00   7.34876000e-01   3.00000000e+00] 1.0
[  2.48590000e+04   1.53467000e-01   7.66619000e-01   1.00000000e+00] 1.0
[  6.17320000e+04   8.32516700e+00   2.84790000e-02   1.00000000e+00] 1.0
[  7.11280000e+04   7.09208900e+00   1.21673300e+00   1.00000000e+00] 1.0
[  2.72760000e+04   5.19248500e+00   1.09440900e+00   3.00000000e+00] 3.0
[  3.04530000e+04   1.03407910e+01   1.08772100e+00   3.00000000e+00] 3.0
[  1.86700000e+04   2.07716900e+00   1.01977500e+00   2.00000000e+00] 2.0
[  7.06000000e+04   1.01519660e+01   9.93105000e-01   1.00000000e+00] 1.0
[  1.26830000e+04   4.68260000e-02   8.09614000e-01   2.00000000e+00] 2.0
[  8.15970000e+04   1.12218740e+01   1.39501500e+00   1.00000000e+00] 1.0
[  6.99590000e+04   1.44979630e+01   1.01925400e+00   1.00000000e+00] 1.0
[  8.12400000e+03   3.55450800e+00   5.33462000e-01   2.00000000e+00] 2.0
[  1.88670000e+04   3.52267300e+00   8.67250000e-02   2.00000000e+00] 2.0
[  8.08860000e+04   1.45316550e+01   3.80172000e-01   1.00000000e+00] 1.0
[  5.58950000e+04   3.02752800e+00   8.85457000e-01   1.00000000e+00] 1.0
[  3.15870000e+04   1.84596700e+00   4.88985000e-01   1.00000000e+00] 1.0
[  1.05910000e+04   1.02261640e+01   8.04403000e-01   3.00000000e+00] 3.0
[  7.00960000e+04   1.09659260e+01   1.21232800e+00   1.00000000e+00] 1.0
[  5.31510000e+04   2.12992100e+00   1.47737800e+00   1.00000000e+00] 1.0
[  1.19920000e+04   0.00000000e+00   1.60684900e+00   2.00000000e+00] 2.0
[  3.31140000e+04   9.48900500e+00   8.27814000e-01   3.00000000e+00] 3.0
[  7.41300000e+03   0.00000000e+00   1.02079700e+00   2.00000000e+00] 2.0
[  1.05830000e+04   0.00000000e+00   1.27016700e+00   2.00000000e+00] 2.0
[  5.86680000e+04   6.55667600e+00   5.51830000e-02   1.00000000e+00] 1.0
[  3.50180000e+04   9.95958800e+00   6.00200000e-02   3.00000000e+00] 3.0
[  7.08430000e+04   7.43605600e+00   1.47985600e+00   1.00000000e+00] 1.0
[  1.40110000e+04   4.04888000e-01   4.59517000e-01   2.00000000e+00] 2.0
[  3.50150000e+04   9.95294200e+00   1.65027900e+00   3.00000000e+00] 3.0
[  7.08390000e+04   1.56002520e+01   2.19350000e-02   1.00000000e+00] 1.0
[  3.02400000e+03   2.72384600e+00   3.87455000e-01   2.00000000e+00] 2.0
[  5.52600000e+03   5.13866000e-01   1.32344800e+00   2.00000000e+00] 2.0
[  5.11300000e+03   0.00000000e+00   8.61859000e-01   2.00000000e+00] 2.0
[  2.08510000e+04   7.28060200e+00   1.43847000e+00   2.00000000e+00] 3.0
[  4.09990000e+04   9.16197800e+00   1.11018000e+00   3.00000000e+00] 3.0
[  1.58230000e+04   9.91725000e-01   7.30979000e-01   2.00000000e+00] 2.0
[  3.54320000e+04   7.39838000e+00   6.84218000e-01   3.00000000e+00] 3.0
[  5.37110000e+04   1.21497470e+01   1.38908800e+00   3.00000000e+00] 1.0
[  6.43710000e+04   9.14967800e+00   8.74905000e-01   1.00000000e+00] 1.0
[  9.28900000e+03   9.66657600e+00   1.37033000e+00   2.00000000e+00] 3.0
[  6.06130000e+04   3.62011000e+00   2.87767000e-01   1.00000000e+00] 1.0
[  1.83380000e+04   5.23880000e+00   1.25364600e+00   2.00000000e+00] 2.0
[  2.28450000e+04   1.47157820e+01   1.50375800e+00   3.00000000e+00] 3.0
[  7.46760000e+04   1.44457400e+01   1.21116000e+00   1.00000000e+00] 1.0
[  3.41430000e+04   1.36095280e+01   3.64240000e-01   3.00000000e+00] 3.0
[  1.41530000e+04   3.14158500e+00   4.24280000e-01   2.00000000e+00] 2.0
[  9.32700000e+03   0.00000000e+00   1.20947000e-01   2.00000000e+00] 2.0
[  1.89910000e+04   4.54750000e-01   1.03328000e+00   2.00000000e+00] 2.0
[  9.19300000e+03   5.10310000e-01   1.63950000e-02   2.00000000e+00] 2.0
[  2.28500000e+03   3.86417100e+00   6.16349000e-01   2.00000000e+00] 2.0
[  9.49300000e+03   6.72402100e+00   5.63044000e-01   2.00000000e+00] 2.0
[  2.37100000e+03   4.28937500e+00   1.25630000e-02   2.00000000e+00] 2.0
[  1.39630000e+04   0.00000000e+00   1.43703000e+00   2.00000000e+00] 2.0
[  2.29900000e+03   3.73361700e+00   6.98269000e-01   2.00000000e+00] 2.0
[  5.26200000e+03   2.00258900e+00   1.38018400e+00   2.00000000e+00] 2.0
[  4.65900000e+03   2.50262700e+00   1.84223000e-01   2.00000000e+00] 2.0
[  1.75820000e+04   6.38212900e+00   8.76581000e-01   2.00000000e+00] 3.0
[  2.77500000e+04   8.54674100e+00   1.28706000e-01   3.00000000e+00] 3.0
[  9.86800000e+03   2.69497700e+00   4.32818000e-01   2.00000000e+00] 2.0
[  1.83330000e+04   3.95125600e+00   3.33300000e-01   2.00000000e+00] 2.0
[  3.78000000e+03   9.85618300e+00   3.29181000e-01   2.00000000e+00] 3.0
[  1.81900000e+04   2.06896200e+00   4.29927000e-01   2.00000000e+00] 2.0
[  1.11450000e+04   3.41062700e+00   6.31838000e-01   2.00000000e+00] 2.0
[  6.88460000e+04   9.97471500e+00   6.69787000e-01   1.00000000e+00] 1.0
[  2.65750000e+04   1.06501020e+01   8.66627000e-01   3.00000000e+00] 3.0
[  4.81110000e+04   9.13452800e+00   7.28045000e-01   3.00000000e+00] 3.0
[  4.37570000e+04   7.88260100e+00   1.33244600e+00   3.00000000e+00] 3.0
```

<img width="50%" height="50%" src="https://github.com/morening/LearnML/blob/master/snapshot/knn/practice0118_dating.png?raw=true" />

### 测试结果（[digits](https://github.com/morening/LearnML/blob/master/data/knn/digits/)）

```
# K = 10

# 准确度：97.56871035940803%

# 测试结果：

4_36.txt 4.0
4_22.txt 4.0
3_17.txt 3.0
9_76.txt 9.0
0_52.txt 0.0
0_46.txt 0.0
9_62.txt 9.0
7_67.txt 7.0
7_73.txt 7.0
0_85.txt 0.0
3_9.txt 3.0
2_57.txt 2.0
2_43.txt 2.0
5_62.txt 5.0
5_76.txt 5.0
5_89.txt 5.0
2_80.txt 2.0
6_33.txt 6.0
6_27.txt 6.0
9_2.txt 9.0
8_22.txt 8.0
8_36.txt 1.0
1_12.txt 1.0
8_37.txt 1.0
1_13.txt 1.0
8_23.txt 8.0
9_3.txt 9.0
6_26.txt 6.0
6_32.txt 6.0
5_88.txt 5.0
2_81.txt 2.0
5_77.txt 5.0
5_63.txt 5.0
2_42.txt 2.0
2_56.txt 2.0
9_88.txt 9.0
3_8.txt 3.0
0_84.txt 0.0
7_72.txt 7.0
7_66.txt 7.0
0_47.txt 0.0
9_63.txt 9.0
9_77.txt 9.0
0_53.txt 0.0
3_16.txt 3.0
4_23.txt 4.0
4_37.txt 4.0
4_21.txt 4.0
3_28.txt 3.0
4_35.txt 4.0
3_14.txt 3.0
1_8.txt 1.0
9_61.txt 9.0
0_45.txt 0.0
0_51.txt 0.0
7_58.txt 7.0
9_75.txt 9.0
7_70.txt 7.0
0_79.txt 0.0
7_64.txt 7.0
9_49.txt 9.0
0_86.txt 0.0
2_40.txt 2.0
5_49.txt 5.0
2_54.txt 2.0
5_75.txt 5.0
5_61.txt 5.0
2_68.txt 2.0
2_83.txt 2.0
6_24.txt 6.0
6_30.txt 6.0
1_39.txt 1.0
1_11.txt 1.0
8_35.txt 1.0
6_18.txt 6.0
9_1.txt 9.0
8_21.txt 8.0
8_20.txt 8.0
9_0.txt 9.0
1_10.txt 1.0
6_19.txt 6.0
8_34.txt 8.0
6_31.txt 6.0
1_38.txt 1.0
6_25.txt 6.0
2_82.txt 2.0
5_60.txt 5.0
2_69.txt 2.0
5_74.txt 5.0
2_55.txt 2.0
2_41.txt 2.0
5_48.txt 5.0
9_48.txt 9.0
7_65.txt 7.0
7_71.txt 7.0
0_78.txt 0.0
0_50.txt 0.0
9_74.txt 9.0
7_59.txt 7.0
9_60.txt 7.0
0_44.txt 0.0
1_9.txt 1.0
3_15.txt 3.0
4_34.txt 4.0
4_20.txt 4.0
3_29.txt 3.0
3_11.txt 9.0
4_18.txt 4.0
4_24.txt 4.0
4_30.txt 4.0
3_39.txt 3.0
7_75.txt 7.0
9_58.txt 9.0
7_61.txt 7.0
0_68.txt 0.0
0_40.txt 0.0
7_49.txt 7.0
9_64.txt 9.0
9_70.txt 9.0
0_54.txt 0.0
0_83.txt 0.0
5_70.txt 5.0
2_79.txt 2.0
5_64.txt 5.0
2_45.txt 2.0
2_51.txt 2.0
5_58.txt 5.0
5_9.txt 5.0
2_86.txt 2.0
8_30.txt 8.0
1_14.txt 1.0
9_4.txt 9.0
8_24.txt 8.0
6_21.txt 6.0
1_28.txt 1.0
8_18.txt 8.0
6_35.txt 6.0
6_34.txt 6.0
8_19.txt 8.0
6_20.txt 6.0
1_29.txt 1.0
8_25.txt 8.0
9_5.txt 9.0
8_31.txt 8.0
1_15.txt 1.0
2_87.txt 2.0
5_8.txt 5.0
2_50.txt 2.0
5_59.txt 5.0
2_44.txt 2.0
5_65.txt 5.0
5_71.txt 5.0
2_78.txt 2.0
0_82.txt 0.0
9_71.txt 9.0
0_55.txt 0.0
0_41.txt 0.0
9_65.txt 9.0
7_48.txt 7.0
7_60.txt 7.0
0_69.txt 0.0
9_59.txt 9.0
7_74.txt 7.0
4_31.txt 4.0
3_38.txt 3.0
4_25.txt 4.0
3_10.txt 3.0
4_19.txt 4.0
3_12.txt 3.0
4_33.txt 4.0
4_27.txt 4.0
7_62.txt 7.0
7_76.txt 7.0
4_109.txt 4.0
0_57.txt 0.0
9_73.txt 9.0
9_67.txt 9.0
0_43.txt 0.0
7_89.txt 7.0
0_80.txt 0.0
5_67.txt 5.0
5_73.txt 5.0
2_52.txt 2.0
2_46.txt 2.0
5_98.txt 5.0
2_91.txt 9.0
2_85.txt 2.0
9_7.txt 9.0
8_27.txt 8.0
1_17.txt 1.0
8_33.txt 8.0
6_36.txt 6.0
6_22.txt 6.0
7_8.txt 7.0
7_9.txt 7.0
6_23.txt 6.0
6_37.txt 6.0
1_16.txt 1.0
8_32.txt 8.0
8_26.txt 8.0
9_6.txt 9.0
2_84.txt 2.0
5_99.txt 5.0
2_90.txt 2.0
2_47.txt 2.0
2_53.txt 2.0
5_72.txt 5.0
5_66.txt 5.0
7_88.txt 7.0
0_81.txt 0.0
9_66.txt 9.0
0_42.txt 0.0
0_56.txt 0.0
9_72.txt 9.0
7_77.txt 7.0
4_108.txt 4.0
7_63.txt 7.0
4_26.txt 4.0
4_32.txt 4.0
3_13.txt 3.0
4_55.txt 4.0
4_41.txt 4.0
3_48.txt 3.0
3_60.txt 3.0
4_69.txt 4.0
8_1.txt 8.0
3_74.txt 3.0
4_96.txt 4.0
4_82.txt 4.0
0_31.txt 0.0
7_38.txt 7.0
9_15.txt 9.0
0_25.txt 0.0
9_29.txt 9.0
7_10.txt 7.0
0_19.txt 0.0
2_34.txt 2.0
2_20.txt 2.0
5_29.txt 5.0
5_15.txt 5.0
6_50.txt 6.0
1_59.txt 1.0
8_69.txt 8.0
6_44.txt 6.0
8_41.txt 8.0
1_65.txt 1.0
1_71.txt 1.0
8_55.txt 8.0
6_78.txt 6.0
8_82.txt 8.0
0_8.txt 0.0
0_9.txt 0.0
8_83.txt 8.0
6_86.txt 6.0
1_70.txt 1.0
6_79.txt 6.0
8_54.txt 8.0
8_40.txt 8.0
1_64.txt 1.0
6_45.txt 6.0
8_68.txt 1.0
6_51.txt 6.0
1_58.txt 1.0
5_14.txt 5.0
2_21.txt 2.0
5_28.txt 5.0
2_35.txt 2.0
7_11.txt 7.0
0_18.txt 0.0
9_28.txt 9.0
0_24.txt 0.0
0_30.txt 0.0
9_14.txt 1.0
7_39.txt 7.0
4_83.txt 4.0
4_97.txt 4.0
3_75.txt 3.0
8_0.txt 8.0
3_61.txt 3.0
4_68.txt 4.0
4_40.txt 4.0
3_49.txt 8.0
4_54.txt 4.0
4_42.txt 4.0
4_56.txt 4.0
3_77.txt 3.0
8_2.txt 8.0
3_63.txt 3.0
4_81.txt 4.0
4_95.txt 4.0
0_26.txt 0.0
9_16.txt 9.0
0_32.txt 0.0
7_13.txt 7.0
2_23.txt 2.0
2_37.txt 2.0
5_16.txt 5.0
2_9.txt 2.0
6_47.txt 6.0
6_53.txt 6.0
8_56.txt 8.0
1_72.txt 1.0
1_66.txt 1.0
8_42.txt 8.0
6_84.txt 6.0
8_81.txt 8.0
8_80.txt 8.0
6_85.txt 6.0
1_67.txt 1.0
8_43.txt 8.0
8_57.txt 8.0
1_73.txt 1.0
6_52.txt 6.0
6_46.txt 6.0
2_8.txt 2.0
5_17.txt 5.0
2_36.txt 2.0
2_22.txt 2.0
7_12.txt 7.0
9_17.txt 1.0
0_33.txt 0.0
0_27.txt 0.0
4_94.txt 4.0
4_80.txt 4.0
3_62.txt 3.0
8_3.txt 8.0
3_76.txt 3.0
4_57.txt 4.0
4_43.txt 4.0
3_72.txt 3.0
8_7.txt 8.0
3_66.txt 3.0
4_47.txt 4.0
4_53.txt 4.0
6_8.txt 6.0
4_84.txt 4.0
4_90.txt 4.0
7_16.txt 7.0
0_23.txt 0.0
0_37.txt 0.0
9_13.txt 9.0
5_13.txt 5.0
2_26.txt 2.0
2_32.txt 2.0
1_77.txt 1.0
8_53.txt 8.0
8_47.txt 8.0
1_63.txt 1.0
6_42.txt 6.0
6_56.txt 6.0
8_90.txt 8.0
8_84.txt 8.0
1_88.txt 1.0
6_81.txt 6.0
1_89.txt 1.0
6_80.txt 6.0
8_85.txt 8.0
6_57.txt 6.0
6_43.txt 6.0
8_46.txt 8.0
1_62.txt 1.0
1_76.txt 1.0
8_52.txt 8.0
2_33.txt 2.0
2_27.txt 2.0
5_12.txt 5.0
0_36.txt 0.0
9_12.txt 9.0
0_22.txt 0.0
7_17.txt 7.0
4_91.txt 4.0
4_85.txt 4.0
6_9.txt 6.0
4_52.txt 4.0
4_46.txt 0.0
3_67.txt 3.0
8_6.txt 8.0
3_73.txt 3.0
3_65.txt 3.0
8_4.txt 8.0
3_71.txt 3.0
4_78.txt 4.0
4_50.txt 4.0
3_59.txt 3.0
4_44.txt 4.0
4_93.txt 4.0
4_87.txt 4.0
7_15.txt 7.0
9_38.txt 9.0
9_10.txt 9.0
0_34.txt 0.0
0_20.txt 0.0
7_29.txt 7.0
4_9.txt 4.0
5_10.txt 5.0
2_19.txt 2.0
2_31.txt 2.0
5_38.txt 5.0
2_25.txt 2.0
1_60.txt 1.0
8_44.txt 8.0
6_69.txt 6.0
8_50.txt 8.0
1_74.txt 1.0
8_78.txt 8.0
6_55.txt 6.0
6_41.txt 6.0
1_48.txt 1.0
8_87.txt 8.0
6_82.txt 6.0
6_83.txt 6.0
8_86.txt 8.0
6_40.txt 6.0
1_49.txt 1.0
6_54.txt 6.0
8_79.txt 8.0
8_51.txt 8.0
1_75.txt 1.0
1_61.txt 1.0
6_68.txt 6.0
8_45.txt 1.0
2_24.txt 2.0
2_30.txt 2.0
5_39.txt 5.0
5_11.txt 5.0
2_18.txt 2.0
4_8.txt 4.0
0_21.txt 0.0
7_28.txt 7.0
9_11.txt 9.0
0_35.txt 0.0
9_39.txt 9.0
7_14.txt 7.0
4_86.txt 4.0
4_92.txt 4.0
4_45.txt 4.0
4_51.txt 4.0
3_58.txt 3.0
3_70.txt 3.0
8_5.txt 8.0
4_79.txt 4.0
3_64.txt 3.0
8_8.txt 3.0
4_74.txt 4.0
4_60.txt 4.0
3_69.txt 3.0
3_41.txt 3.0
4_48.txt 4.0
3_55.txt 3.0
6_7.txt 6.0
3_82.txt 3.0
0_10.txt 0.0
7_19.txt 7.0
9_34.txt 9.0
9_20.txt 9.0
7_25.txt 7.0
7_31.txt 7.0
0_38.txt 0.0
4_5.txt 4.0
2_15.txt 2.0
5_20.txt 5.0
2_29.txt 2.0
5_34.txt 5.0
2_3.txt 2.0
6_71.txt 6.0
1_78.txt 1.0
8_48.txt 8.0
6_65.txt 6.0
8_60.txt 8.0
1_44.txt 1.0
1_50.txt 1.0
8_74.txt 8.0
6_59.txt 6.0
0_1.txt 0.0
1_87.txt 1.0
1_93.txt 1.0
1_92.txt 1.0
1_86.txt 7.0
0_0.txt 0.0
1_51.txt 1.0
6_58.txt 6.0
8_75.txt 8.0
8_61.txt 8.0
1_45.txt 1.0
6_64.txt 6.0
8_49.txt 8.0
6_70.txt 6.0
1_79.txt 1.0
2_2.txt 2.0
5_35.txt 5.0
5_21.txt 5.0
2_28.txt 2.0
2_14.txt 2.0
4_4.txt 4.0
7_30.txt 7.0
0_39.txt 0.0
7_24.txt 7.0
9_21.txt 9.0
0_11.txt 0.0
9_35.txt 9.0
7_18.txt 7.0
3_83.txt 3.0
6_6.txt 6.0
3_54.txt 3.0
3_40.txt 3.0
4_49.txt 4.0
4_61.txt 4.0
3_68.txt 3.0
8_9.txt 8.0
4_75.txt 4.0
4_63.txt 4.0
4_77.txt 4.0
3_56.txt 3.0
3_42.txt 3.0
6_4.txt 6.0
4_88.txt 4.0
3_81.txt 3.0
9_23.txt 9.0
9_37.txt 9.0
0_13.txt 0.0
7_32.txt 7.0
7_26.txt 7.0
4_6.txt 4.0
2_16.txt 2.0
5_37.txt 5.0
5_23.txt 5.0
2_0.txt 2.0
6_66.txt 6.0
6_72.txt 6.0
8_77.txt 8.0
1_53.txt 1.0
1_47.txt 1.0
8_63.txt 8.0
8_88.txt 8.0
0_2.txt 0.0
1_90.txt 1.0
1_84.txt 1.0
1_85.txt 1.0
1_91.txt 1.0
0_3.txt 0.0
8_89.txt 8.0
1_46.txt 1.0
8_62.txt 8.0
8_76.txt 8.0
1_52.txt 1.0
6_73.txt 6.0
6_67.txt 6.0
2_1.txt 2.0
5_22.txt 5.0
5_36.txt 5.0
2_17.txt 2.0
4_7.txt 4.0
7_27.txt 7.0
7_33.txt 7.0
9_36.txt 9.0
0_12.txt 0.0
9_22.txt 9.0
4_89.txt 4.0
3_80.txt 3.0
6_5.txt 6.0
3_43.txt 2.0
3_57.txt 3.0
4_76.txt 4.0
4_62.txt 4.0
3_53.txt 3.0
3_47.txt 3.0
4_66.txt 4.0
4_72.txt 4.0
4_99.txt 4.0
3_84.txt 3.0
6_1.txt 6.0
7_37.txt 7.0
7_23.txt 7.0
9_26.txt 9.0
0_16.txt 0.0
9_32.txt 9.0
4_3.txt 4.0
5_32.txt 5.0
5_26.txt 5.0
2_13.txt 2.0
2_5.txt 2.0
1_56.txt 1.0
8_72.txt 8.0
8_66.txt 8.0
1_42.txt 1.0
6_63.txt 6.0
6_77.txt 6.0
1_95.txt 1.0
1_81.txt 1.0
0_7.txt 0.0
0_6.txt 0.0
1_80.txt 1.0
1_94.txt 1.0
6_76.txt 6.0
6_62.txt 6.0
8_67.txt 8.0
1_43.txt 1.0
1_57.txt 1.0
8_73.txt 8.0
2_4.txt 2.0
2_12.txt 2.0
5_27.txt 5.0
5_33.txt 9.0
4_2.txt 9.0
0_17.txt 0.0
9_33.txt 9.0
9_27.txt 9.0
7_22.txt 7.0
7_36.txt 7.0
6_0.txt 6.0
4_98.txt 4.0
4_73.txt 4.0
4_67.txt 4.0
3_46.txt 2.0
3_52.txt 3.0
3_44.txt 3.0
3_50.txt 3.0
4_59.txt 4.0
4_71.txt 4.0
3_78.txt 3.0
4_65.txt 4.0
6_2.txt 6.0
7_20.txt 7.0
0_29.txt 0.0
7_34.txt 7.0
9_19.txt 9.0
9_31.txt 9.0
0_15.txt 0.0
9_25.txt 9.0
4_0.txt 4.0
5_25.txt 5.0
5_31.txt 5.0
2_38.txt 2.0
2_10.txt 2.0
5_19.txt 5.0
2_6.txt 2.0
1_41.txt 1.0
8_65.txt 1.0
6_48.txt 6.0
8_71.txt 8.0
1_55.txt 1.0
8_59.txt 8.0
6_74.txt 6.0
6_60.txt 6.0
1_69.txt 1.0
1_82.txt 1.0
1_96.txt 1.0
0_4.txt 0.0
0_5.txt 0.0
1_83.txt 1.0
6_61.txt 6.0
1_68.txt 1.0
6_75.txt 6.0
8_58.txt 8.0
8_70.txt 8.0
1_54.txt 1.0
1_40.txt 1.0
6_49.txt 6.0
8_64.txt 8.0
2_7.txt 2.0
2_11.txt 2.0
5_18.txt 5.0
5_30.txt 5.0
2_39.txt 2.0
5_24.txt 5.0
4_1.txt 4.0
9_24.txt 9.0
9_30.txt 9.0
0_14.txt 0.0
9_18.txt 9.0
7_35.txt 7.0
7_21.txt 7.0
0_28.txt 0.0
6_3.txt 6.0
4_64.txt 4.0
4_70.txt 4.0
3_79.txt 3.0
3_51.txt 3.0
4_58.txt 4.0
3_45.txt 3.0
4_17.txt 4.0
5_100.txt 5.0
3_22.txt 3.0
3_36.txt 3.0
1_2.txt 1.0
9_57.txt 9.0
4_105.txt 4.0
0_73.txt 0.0
0_67.txt 0.0
4_111.txt 4.0
9_43.txt 9.0
7_46.txt 7.0
7_52.txt 7.0
3_0.txt 3.0
9_80.txt 9.0
7_85.txt 7.0
7_91.txt 7.0
2_76.txt 2.0
2_62.txt 2.0
5_43.txt 6.0
5_57.txt 5.0
5_6.txt 5.0
2_89.txt 2.0
5_80.txt 5.0
5_94.txt 5.0
6_12.txt 6.0
1_27.txt 1.0
8_17.txt 8.0
1_33.txt 1.0
7_4.txt 7.0
7_5.txt 7.0
8_16.txt 8.0
1_32.txt 1.0
1_26.txt 1.0
6_13.txt 6.0
5_95.txt 5.0
2_88.txt 2.0
5_81.txt 5.0
5_7.txt 5.0
5_56.txt 5.0
5_42.txt 3.0
2_63.txt 2.0
2_77.txt 2.0
7_90.txt 7.0
7_84.txt 7.0
3_1.txt 3.0
9_81.txt 9.0
7_53.txt 7.0
7_47.txt 7.0
4_110.txt 4.0
0_66.txt 0.0
9_42.txt 9.0
9_56.txt 9.0
0_72.txt 0.0
4_104.txt 4.0
1_3.txt 1.0
3_37.txt 3.0
3_23.txt 3.0
5_101.txt 5.0
4_16.txt 4.0
5_103.txt 5.0
4_14.txt 4.0
3_35.txt 3.0
3_21.txt 3.0
4_28.txt 4.0
1_1.txt 1.0
9_40.txt 9.0
0_64.txt 0.0
4_112.txt 4.0
4_106.txt 4.0
0_70.txt 0.0
7_79.txt 7.0
9_54.txt 9.0
7_51.txt 7.0
0_58.txt 0.0
7_45.txt 7.0
9_68.txt 9.0
9_83.txt 9.0
3_3.txt 3.0
7_92.txt 7.0
7_86.txt 7.0
2_61.txt 2.0
5_68.txt 5.0
2_75.txt 2.0
5_54.txt 5.0
5_40.txt 5.0
2_49.txt 2.0
5_5.txt 5.0
5_97.txt 5.0
5_83.txt 5.0
8_28.txt 8.0
9_8.txt 9.0
6_11.txt 6.0
1_18.txt 1.0
1_30.txt 1.0
8_14.txt 8.0
6_39.txt 6.0
1_24.txt 1.0
7_7.txt 7.0
7_6.txt 7.0
1_25.txt 1.0
1_31.txt 1.0
6_38.txt 6.0
8_15.txt 8.0
6_10.txt 6.0
1_19.txt 1.0
9_9.txt 9.0
8_29.txt 8.0
5_82.txt 5.0
5_96.txt 5.0
5_4.txt 5.0
5_41.txt 5.0
2_48.txt 2.0
5_55.txt 5.0
2_74.txt 2.0
2_60.txt 2.0
5_69.txt 5.0
7_87.txt 7.0
7_93.txt 7.0
9_82.txt 9.0
3_2.txt 3.0
9_69.txt 9.0
7_44.txt 7.0
7_50.txt 7.0
0_59.txt 0.0
0_71.txt 0.0
4_107.txt 4.0
9_55.txt 9.0
7_78.txt 7.0
9_41.txt 9.0
4_113.txt 4.0
0_65.txt 0.0
1_0.txt 1.0
3_20.txt 3.0
4_29.txt 4.0
3_34.txt 3.0
4_15.txt 4.0
5_102.txt 5.0
3_30.txt 3.0
4_39.txt 4.0
3_24.txt 3.0
5_106.txt 5.0
4_11.txt 4.0
3_18.txt 3.0
1_4.txt 1.0
7_54.txt 7.0
9_79.txt 9.0
7_40.txt 7.0
0_49.txt 0.0
0_61.txt 0.0
7_68.txt 7.0
9_45.txt 9.0
9_51.txt 9.0
4_103.txt 4.0
0_75.txt 0.0
7_83.txt 7.0
3_6.txt 3.0
9_86.txt 9.0
5_51.txt 5.0
2_58.txt 2.0
5_45.txt 5.0
2_64.txt 2.0
2_70.txt 2.0
5_79.txt 5.0
5_92.txt 5.0
5_86.txt 5.0
5_0.txt 5.0
8_11.txt 6.0
1_35.txt 1.0
1_21.txt 1.0
6_28.txt 6.0
8_39.txt 1.0
6_14.txt 6.0
7_2.txt 7.0
7_3.txt 7.0
6_15.txt 6.0
8_38.txt 8.0
1_20.txt 1.0
6_29.txt 6.0
8_10.txt 8.0
1_34.txt 1.0
5_1.txt 5.0
5_87.txt 5.0
5_93.txt 5.0
2_71.txt 2.0
5_78.txt 5.0
2_65.txt 2.0
5_44.txt 5.0
5_50.txt 5.0
2_59.txt 2.0
3_7.txt 3.0
9_87.txt 9.0
7_82.txt 7.0
9_50.txt 9.0
0_74.txt 0.0
4_102.txt 4.0
0_60.txt 0.0
9_44.txt 9.0
7_69.txt 7.0
7_41.txt 7.0
0_48.txt 0.0
9_78.txt 9.0
7_55.txt 7.0
1_5.txt 1.0
4_10.txt 4.0
3_19.txt 3.0
5_107.txt 5.0
3_25.txt 3.0
3_31.txt 3.0
4_38.txt 4.0
3_27.txt 3.0
3_33.txt 3.0
4_12.txt 4.0
5_105.txt 5.0
1_7.txt 1.0
7_43.txt 7.0
7_57.txt 7.0
4_100.txt 4.0
0_76.txt 0.0
9_52.txt 9.0
9_46.txt 9.0
0_62.txt 0.0
7_80.txt 7.0
7_94.txt 7.0
9_85.txt 9.0
3_5.txt 3.0
5_46.txt 5.0
5_52.txt 5.0
2_73.txt 2.0
2_67.txt 2.0
5_85.txt 5.0
5_91.txt 5.0
5_3.txt 5.0
1_22.txt 1.0
1_36.txt 1.0
8_12.txt 8.0
6_17.txt 6.0
7_1.txt 7.0
7_0.txt 7.0
6_16.txt 6.0
1_37.txt 1.0
8_13.txt 8.0
1_23.txt 1.0
5_2.txt 5.0
5_90.txt 5.0
5_84.txt 5.0
2_66.txt 2.0
2_72.txt 2.0
5_53.txt 5.0
5_47.txt 5.0
9_84.txt 9.0
3_4.txt 3.0
7_95.txt 7.0
7_81.txt 7.0
9_47.txt 9.0
0_63.txt 0.0
0_77.txt 0.0
4_101.txt 4.0
9_53.txt 9.0
7_56.txt 7.0
7_42.txt 7.0
1_6.txt 1.0
5_104.txt 5.0
4_13.txt 4.0
3_32.txt 3.0
3_26.txt 3.0
```