之前的隐私图像检测：
PicAlert： Privacy-aware image classification and search. SIGIR 2012: 35-44最早最常用的公开隐私数据集 大多数私人图像都包含人，这会导致对所考虑的私人对象的偏见（63%的私人图像包含人）； 可能的标签是私有的、公共的和不可决定的（如果不能对图像标签做出决定）。

PrivacyAlert: A Dataset for Image Privacy Prediction. ICWSM 2022: 1352-1361； 发的一篇公开隐私数据集的论文； 从Flickr中提取的最近图像开发的数据集；
图像隐私检测做的全监督-->半监督

图像隐私风险预测：
Towards a Visual Privacy Advisor: Understanding and Predicting Privacy Risks in Images. ICCV 2017: 3706-371 隐私数据集，多个隐私标注 name_ful全名,username用户名，phone电话，email邮箱，education_history教育经历，email_content邮件内容，address_current_partial家庭住址，ticket门票，passport护照， Receipt收据，credit_card信用卡，student_id学生卡，drivers_license驾驶执照，medicine病史 这个数据集的标签是隐私属性
先通过多标签图像分类任务得出图像中具体存在的对象，再根据自己调查出每个对象的隐私得分得出每张图像的隐私分数。

PrivAttNet: Predicting Privacy Risks in Images Using Visual Attention. ICPR 2020
PrivAttNet的注意力机制是基于一个卷积神经网络（CNN）和一个全连接层（FC）的组合。它首先使用CNN来提取图像的特征，然后使用FC来计算每个特征图的权重，这些权重就是注意力分数。注意力分数越高，表示该特征图对隐私分数的贡献越大。然后，它将所有的特征图按照注意力分数加权求和，得到一个最终的特征向量，这个向量就是用来预测隐私分数的输入。

Privacy Attributes-aware Message Passing Neural Network for Visual Privacy Attributes Classification，2020，ICPR
通过构建图神经网络来探索各对象之间的关联性

多标签图像分类任务





