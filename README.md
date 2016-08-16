# SentenceClassifier
a chinese sentences classifier

##说明
　　这是一个中文句子分类器，由于词向量和语料文件太大，就不上传了。目前我上传了已经转化过的句子向量映射表，可以直接抽象成训练神经网络的训练集和测试集。

##用法
　　进入bin\x64\Debug目录下，运行“NeuroNetworkClassifier.exe”，点击“加载映射表”，选择当前目录下的“DataVector_400_[1492-167]_31_12400_12.vecmap”文件，加载后可以在界面上看到语料参数。
接下来点击“训练新模型”，可以在新窗口中设置神经网络的隐藏层结构，默认只有一层，10个节点，点击数字后可以在下方修改，也可以添加更多隐藏层，并任意修改节点数，确定后便会开始训练模型，模型训练迭代两次后就能看到动态的性能曲线图。

##例子
　　运行 “NeuroNetworkClassifier.exe” ，可以直接点击加载模型，选择当前目录下的 “Classifier_[1492-167]_12400-20-12_650--3--44.model” ，可以看到我自己训练过的模型。可以看出目前由于训练样本太少，测试集的误差率依然很高。现在再点击“加载模型”，选择 “Classifier_[20296-2184]_10400-20-12_560--2--6.model” ，可以看到现在模型性能表现相对较好。
　　