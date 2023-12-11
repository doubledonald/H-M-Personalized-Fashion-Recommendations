# HM-Personalized-Fashion-Recommendations
kaggle比赛  jupyter   
以用户向量和物品向量之间的相似度作为重要的特征，采用了多种 Recall 方法来做 candidate generation  
并使用了 Catboost 模型来训练特征数据，设计了一种基于运营商大数据的产品推荐模型。  
数据集过大，这里给出数据集下载链接：  
(https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations)   
下载数据集后，在文件夹中新建子文件夹 data/rawdata，在这里存放下载后的数据集，注意我们仅使用了 articls.csv，customers.csv，   
transactions_trian.csv，这三个数据集。  
同时在文件夹中建立 output 文件夹用于存放中间产生的数据文件以及结果。  
在记事本中用详细的代码使用指引，这里只给出不同记事本文件的含义    
基于矩阵分解的协同过滤模型：矩阵分解.ipynb   
“相似推荐”——推荐基于物品聚类的推荐算法：物品聚类.ipynb  
“猜你喜欢：——基于用户画像的推荐算法：用户画像.ipynb  
基于 LightFM- GBDT 的推荐模型：  
⚫ HM_get_data.ipynb —— 数据读入代码文件  
⚫ HM_feature.ipynb —— 构建特征工程代码文件  
⚫ HM_train_infer.ipynb —— 参数调整与模型训练文件  
⚫ users.pkl —— customer 信息转换成的 pkl 读入文件  
⚫ items.pkl —— articles 信息转换成的 pkl 读入文件  
⚫ lfm_i_i_week13_dim16_model.pkl —— 第 13 周 user-item 矩阵文件  
⚫ user_ohe_agg_week0_perceived_colour_value_id_idx.pkl —— 第0 周 groupby 后的 user 特征文件  
（注：由于数据量庞大，时间周期长，进行 LightFM 模型构建特征的运行结果文件体积过大，此处仅提交一个 week 的文件作为示例
