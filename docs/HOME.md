# PHP-ML - PHP的机器学习类库

![PHP-ML](https://raw.githubusercontent.com/php-ai/php-ml/master/docs/assets/php-ml-logo.png)

PHP中学习机器的新方法。算法、交叉验证、神经网络、预处理、特征提取等。集成在一个类库中。

PHP版本  >= 7.1.

`分类算法(classification)` 的简单示例:

```php
require_once __DIR__ . '/vendor/autoload.php';

use Phpml\Classification\KNearestNeighbors;

$samples = [[1, 3], [1, 4], [2, 4], [3, 1], [4, 1], [4, 2]];
$labels = ['a', 'a', 'a', 'b', 'b', 'b'];

$classifier = new KNearestNeighbors();
$classifier->train($samples, $labels);

$classifier->predict([3, 2]);
// return 'b'
```

## 安装

类库还在开发中，但是你可以使用Composer安装:

```
composer require php-ai/php-ml
```

## 例子

一些示例脚本 [php-ai/php-ml-examples](https://github.com/php-ai/php-ml-examples).

## 特性

- 关联规则学习(Association rule Lerning)
    - [Apriori](关联规则学习/Apriori.md)
- 分类(Classification)
    - [支持向量机(SVC)](https://php-ml.readthedocs.io/en/latest/machine-learning/classification/svc/)
    - [K最近邻算法(k-Nearest Neighbors)](https://php-ml.readthedocs.io/en/latest/machine-learning/classification/k-nearest-neighbors/)
    - [朴素贝叶斯算法(Naive Bayes)](https://php-ml.readthedocs.io/en/latest/machine-learning/classification/naive-bayes/)
- 回归(Regression)
    - [最小二乘法(Least Squares)](https://php-ml.readthedocs.io/en/latest/machine-learning/regression/least-squares/)
    - [支持向量回归(SVR)](https://php-ml.readthedocs.io/en/latest/machine-learning/regression/svr/)
- 聚类(Clustering)
    - [基于距离的聚类算法(k-Means)](https://php-ml.readthedocs.io/en/latest/machine-learning/clustering/k-means/)
    - [具有噪声的基于密度的聚类算法(DBSCAN)](https://php-ml.readthedocs.io/en/latest/machine-learning/clustering/dbscan/)
- 指标(Metric)
    - [精度(Accuracy)](https://php-ml.readthedocs.io/en/latest/machine-learning/metric/accuracy/)
    - [混淆矩阵(Confusion Matrix)](https://php-ml.readthedocs.io/en/latest/machine-learning/metric/confusion-matrix/)
    - [分类评估(Classification Report)](https://php-ml.readthedocs.io/en/latest/machine-learning/metric/classification-report/)
- 工作流(Workflow)
    - [管道(Pipeline)](https://php-ml.readthedocs.io/en/latest/machine-learning/workflow/pipeline)
- 神经网络(Neural Network)
    - [多层感知器分类器(Multilayer Perceptron Classifier)](https://php-ml.readthedocs.io/en/latest/machine-learning/neural-network/multilayer-perceptron-classifier/)
- 交叉验证(Cross Validation)
    - [Random Split](https://php-ml.readthedocs.io/en/latest/machine-learning/cross-validation/random-split/)
    - [Stratified Random Split](https://php-ml.readthedocs.io/en/latest/machine-learning/cross-validation/stratified-random-split/)
- 特征选择(Feature Selection)
    - [方差过滤(Variance Threshold)](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-selection/variance-threshold/)
    - [最佳选择(SelectKBest)](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-selection/selectkbest/)
- 预处理(Preprocessing)
    - [归一化(Normalization)](https://php-ml.readthedocs.io/en/latest/machine-learning/preprocessing/normalization/)
    - [插补缺失值(Imputation missing values)](https://php-ml.readthedocs.io/en/latest/machine-learning/preprocessing/imputation-missing-values/)
- 特征提取(Feature Extraction)
    - [令牌计数向量器(Token Count Vectorizer)](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-extraction/token-count-vectorizer/)
    - [词频-逆文本频率转换器(Tf-idf Transformer)](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-extraction/tf-idf-transformer/)
- 数据集(Datasets)
    - [Array](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/array-dataset/)
    - [CSV](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/csv-dataset/)
    - [Files](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/files-dataset/)
    - [SVM](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/svm-dataset/)
    - [MNIST](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/mnist-dataset/)
    - 准备:
        - [鸢尾花(Iris)](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/iris/)
        - [酒(Wine)](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/wine/)
        - [玻璃(Glass)](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/glass/)
- 模型管理(Models management)
    - [持久性(Persistency)](https://php-ml.readthedocs.io/en/latest/machine-learning/model-manager/persistency/)
- 数学(Math)
    - [距离(Distance)](https://php-ml.readthedocs.io/en/latest/math/distance/)
    - [矩阵(Matrix)](https://php-ml.readthedocs.io/en/latest/math/matrix/)
    - [集合(Set)](https://php-ml.readthedocs.io/en/latest/math/set/)
    - [统计(Statistic)](https://php-ml.readthedocs.io/en/latest/math/statistic/)



