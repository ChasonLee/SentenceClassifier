# SentenceClassifier
an ANN-based chinese sentence classifier

##说明
- 这是一个基于中文词向量和BP神经网络的中文句子分类器，句子向量目前只是简单的词向量组合。由于词向量和语料文件太大，我已上传到百度网盘：http://pan.baidu.com/s/1nvEnLn7
- 选择需要的文件，放在bin\x64\Debug目录里。
- 开发环境：WIN10 + VS2015
- 注意：这只是一个BP神经网络的测试程序，界面可能还有不少bug，请勿在意……

##用法
- 进入bin\x64\Debug目录下，运行“NeuroNetworkClassifier.exe”，点击“加载词向量”，选择当前目录下的“wiki.zh.text.jian.seg.vector”文件，由于文件很大（1.6G），加载时间会比较长（1~2分钟左右）。
- 加载词向量完成后，可以加载数据集，选择“dataset5”文件夹下的所有文件，加载过程可能需要十几秒。数据集加载完成后，程序会将数据随机分离成训练集和测试集。现在在当前目录下会生成一个“DataVector.vecmap”文件，这是当前生成的向量映射表，以后需要继续训练模型时，可以直接加载此映射表，不需要再加载词向量和数据集。
- 通过点击“保存映射表”，可以将此映射表另存为其他名字。网盘上还有我加载好的两个映射表，文件名以“.vecmap”结尾，可供参考。
- 有了训练集和测试集后，接下来点击“训练新模型”，可以在新窗口中设置神经网络的隐藏层结构，默认只有一层，10个节点，点击数字后可以在下方修改，也可以添加更多隐藏层，并任意修改节点数，确定后便会开始训练模型，模型训练迭代两次后就能看到动态的性能曲线图。训练开始后，可以随时停止和开始训练，训练结果默认会保存到“Classifier.model”。

##例子
- 运行 “NeuroNetworkClassifier.exe” ，可以直接点击加载模型，选择当前目录下的“Classifier_[1492-167]_12400-20-12_650--3--44.model” 
![](https://github.com/ChasonLee/SentenceClassifier/raw/master/img/model1.jpg)
- 这是我自己训练过的模型。目前由于训练样本太少，测试集的误差率依然很高。
- 现在再点击“加载模型”，选择“Classifier_[20296-2184]_10400-20-12_560--2--6.model” 
![](https://github.com/ChasonLee/SentenceClassifier/raw/master/img/model2.jpg)
- 可以看到现在模型性能表现相对较好。

##引用
- 中文词向量来源于维基百科，参考：http://www.52nlp.cn/%E4%B8%AD%E8%8B%B1%E6%96%87%E7%BB%B4%E5%9F%BA%E7%99%BE%E7%A7%91%E8%AF%AD%E6%96%99%E4%B8%8A%E7%9A%84word2vec%E5%AE%9E%E9%AA%8C
- 加载数据集时，使用的中文分词算法来源于哈工大LTP：http://www.ltp-cloud.com/
　　
