### 先验关联

关联规则学习是基于[先验算法](https://en.wikipedia.org/wiki/Apriori_algorithm)的频繁项集挖掘.

#### 构造方法参数

+ $support - [支持度](https://en.wikipedia.org/wiki/Association_rule_learning#Support)的最小阈值，表示X和Y同时出现的概率。
+ $confidence -[置信度](https://en.wikipedia.org/wiki/Association_rule_learning#Confidence)的最小阈值，表示X和Y同时出现的概率占X出现概率的比率。

```php
use Phpml\Association\Apriori;

$associator = new Apriori($support = 0.5, $confidence = 0.5);
```

#### 训练

要训练关联，只需提供训练样本和标签（数组）。. 

例子:

```php
$samples = [['alpha', 'beta', 'epsilon'], ['alpha', 'beta', 'theta'], ['alpha', 'beta', 'epsilon'], ['alpha', 'beta', 'theta']];
$labels  = [];

use Phpml\Association\Apriori;

$associator = new Apriori($support = 0.5, $confidence = 0.5);
$associator->train($samples, $labels);
```

你可以使用多个数据集来训练，预测基于所有训练数据.

#### 预测

使用`predict`方法预测样本标签。您可以提供一个样本或一组样本：

```php
$associator->predict(['alpha','theta']);
// return [['beta']]

$associator->predict([['alpha','epsilon'],['beta','theta']]);
// return [[['beta']], [['alpha']]]
```

#### 关联

获取生成的关联规则只需使用`rules`方法。

```php
$associator->getRules();
// return [['antecedent' => ['alpha', 'theta'], 'consequent' => ['beta'], 'support' => 1.0, 'confidence' => 1.0], ... ]
```

#### 频繁项集

生成k长度的频繁项集只需使用`apriori`方法。

```php
$associator->apriori();
// return [ 1 => [['alpha'], ['beta'], ['theta'], ['epsilon']], 2 => [...], ...]
```
