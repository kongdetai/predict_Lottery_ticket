# 双色球彩票号码预测

项目比较简单，仅作为娱乐项目，但没想到关注人比预期要多，特此感谢大家关注，祝大家都能发财！
因为项目本身涉及到爬虫，机器学习，后端服务技术，而且是面向开发者的，我默认大家有这方面技术背景且能解决一些常识问题，故没有做太多细节说明，特此表示抱歉。
项目仅仅是抛砖引玉，很多地方都不是绝对的，目的是为了感兴趣的朋友可以自定义调试。

## Getting Started
执行 python get_train_data.py 用于获取训练数据，
如果出现解析错误，应该看看网页 http://datachart.500.com/ssq/history/newinc/history.php 是否可以正常访问

执行 python train_model.py 用于模型训练，模型训练完成会保存至model文件下，默认是一个球一个序列模型，训练结束后会得到7个模型文件，
我是i7-8550U 的CPU + NVIDIA GeFore MX150 GPU, 整个训练时间大概40分钟左右，训练时间太久的话可以减小epochs参数值。
build_model函数中定义得模型可修改定义，但要保证输入输出shape与原模型一致。

执行 python run_api.py 启动一个微服务，获取每天预测号码，获取预测访问url为: http://127.0.0.1:5000/predict_api
服务部署在后台，可以直接在浏览器上每日获取预测结果。

### Installing

python3.6 环境，相关库和版本在 requirements.txt 下

pip install -r requirement.txt

若安装存在问题，可手动依次安装，具体安装库产生问题，需自行解决

## Running the tests

![avatar](img/001.png)

![avatar](img/002.png)

![avatar](img/003.png)
