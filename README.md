# 人工智能pixiv高质量涩图爬虫
# 能学会你xp的AI涩图爬虫

爬虫部分基于 [PixivCrawler](https://github.com/CWHer/PixivCrawler.git) 修改实现，
涩图识别分类部分使用 [ConvNeXt](https://github.com/facebookresearch/ConvNeXt.git) 作为backbone的分类模型实现，
性能优于Trasnformer类模型。

## 自动筛选效果

<img src="imgs/c1.jpg" >

## 环境配置
环境配置参考 [ConvNeXt](https://github.com/facebookresearch/ConvNeXt.git)

需要 **pytorch==1.8**

## 使用方法
下载预训练权重放在```ckpt/```文件夹内:

[下载权重](https://pan.baidu.com/s/1pAiR6YrQ9uZxmUc1JZ6R7A) 提取码：o4ps

根据 [PixivCrawler](https://github.com/CWHer/PixivCrawler.git) 的说明配置爬虫，设置账号和cookie，设置要爬的内容

运行命令启动AI爬虫:
```bash
python AIcrawler.py --ckpt 模型权重 --n_images 总图像个数 [--keyword 关键字] 
```

## 按自己的xp训练模型
用```labeler.py```打标签，需要至少5000张图。

修改参数，运行脚本训练:
```bash
python train.sh
```

其他训练设置参考 [ConvNeXt](https://github.com/facebookresearch/ConvNeXt.git)