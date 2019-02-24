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
    - [Apriori](关联规则学习(Association rule Lerning)/Apriori.md)
- 分类(Classification)
    - [SVC](https://php-ml.readthedocs.io/en/latest/machine-learning/classification/svc/)
    - [k-Nearest Neighbors](https://php-ml.readthedocs.io/en/latest/machine-learning/classification/k-nearest-neighbors/)
    - [Naive Bayes](https://php-ml.readthedocs.io/en/latest/machine-learning/classification/naive-bayes/)
- 回归(Regression)
    - [Least Squares](https://php-ml.readthedocs.io/en/latest/machine-learning/regression/least-squares/)
    - [SVR](https://php-ml.readthedocs.io/en/latest/machine-learning/regression/svr/)
- Clustering
    - [k-Means](https://php-ml.readthedocs.io/en/latest/machine-learning/clustering/k-means/)
    - [DBSCAN](https://php-ml.readthedocs.io/en/latest/machine-learning/clustering/dbscan/)
- Metric
    - [Accuracy](https://php-ml.readthedocs.io/en/latest/machine-learning/metric/accuracy/)
    - [Confusion Matrix](https://php-ml.readthedocs.io/en/latest/machine-learning/metric/confusion-matrix/)
    - [Classification Report](https://php-ml.readthedocs.io/en/latest/machine-learning/metric/classification-report/)
- Workflow
    - [Pipeline](https://php-ml.readthedocs.io/en/latest/machine-learning/workflow/pipeline)
- 神经网络(Neural Network)
    - [Multilayer Perceptron Classifier](https://php-ml.readthedocs.io/en/latest/machine-learning/neural-network/multilayer-perceptron-classifier/)
- 交叉验证(Cross Validation)
    - [Random Split](https://php-ml.readthedocs.io/en/latest/machine-learning/cross-validation/random-split/)
    - [Stratified Random Split](https://php-ml.readthedocs.io/en/latest/machine-learning/cross-validation/stratified-random-split/)
- 特征选择(Feature Selection)
    - [Variance Threshold](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-selection/variance-threshold/)
    - [SelectKBest](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-selection/selectkbest/)
- 预处理(Preprocessing)
    - [Normalization](https://php-ml.readthedocs.io/en/latest/machine-learning/preprocessing/normalization/)
    - [Imputation missing values](https://php-ml.readthedocs.io/en/latest/machine-learning/preprocessing/imputation-missing-values/)
- 特征提取(Feature Extraction)
    - [Token Count Vectorizer](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-extraction/token-count-vectorizer/)
    - [Tf-idf Transformer](https://php-ml.readthedocs.io/en/latest/machine-learning/feature-extraction/tf-idf-transformer/)
- 数据集(Datasets)
    - [Array](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/array-dataset/)
    - [CSV](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/csv-dataset/)
    - [Files](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/files-dataset/)
    - [SVM](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/svm-dataset/)
    - [MNIST](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/mnist-dataset/)
    - Ready to use:
        - [Iris](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/iris/)
        - [Wine](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/wine/)
        - [Glass](https://php-ml.readthedocs.io/en/latest/machine-learning/datasets/demo/glass/)
- Models management
    - [Persistency](https://php-ml.readthedocs.io/en/latest/machine-learning/model-manager/persistency/)
- 数学
    - [Distance](https://php-ml.readthedocs.io/en/latest/math/distance/)
    - [矩阵(Matrix)](https://php-ml.readthedocs.io/en/latest/math/matrix/)
    - [集合(Set)](https://php-ml.readthedocs.io/en/latest/math/set/)
    - [统计(Statistic)](https://php-ml.readthedocs.io/en/latest/math/statistic/)



