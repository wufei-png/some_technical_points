## 记录一个折腾我半天的在自己电脑上安装 cuda 的坑。

实验室服务器好像不太行，要求我先在自己电脑上跑。好嘛，根据项目的代码确定 python 和 pytorch 版本，从官网获取对应的 cuda cudnn 版本，好嘛，一顿安，先安 cuda cudnn 驱动 ，然后就安包，pytorch 官网一搜 new bing 和网上教程验证，带 cudatoolkit 的是 gpu 版本的 pytorch：conda install pytorch==1.5.0 torchvision==0.6.0 cudatoolkit=10.2 -c pytorch 直接怼，显示 torchvision 通道内找不到，行，去掉这个再按，安上了检测不到 gpu，检查半天 conda list 显示 pytorch 是 cpu 版本，关键是中间我还验证过 print(torch.**version**)没显示 cpu，gpu 和 cpu 版本都只显示版本号，太坑了，最后上 anaconda 官网找了一个私人通道才安上
