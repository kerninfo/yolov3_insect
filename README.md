# yolov3_insect
Yolov3 algorithm for AI identification of insects
使用yolov3算法进行AI识虫

Requirements:
首先安装Paddlepaddle库
训练样本库位于:
链接：https://pan.baidu.com/s/1T9X7VRL7_kDfhXg650EChQ 
提取码：lody
下载后,解压到源码目录即可.

进入源码目录:
启动训练：
# use_gpu = False  # 如果使用GPU训练的话,那么将它改成True
python train.py

评估测试样本集：
# yolov3_epoch100 为训练的模型参数保存的文件
python eval.py --image_dir=./insects/test/images --weight_file=./yolov3_epoch100

预测:
python predict.py --image_name=./insects/test/images/2244.jpeg --weight_file=./yolo_epoch100
预测结果保存为: output_pic.png
