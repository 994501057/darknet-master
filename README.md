![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

# Darknet #
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).
：
要记得：一定make clean，然后make
cfg，data，names文件均可自己创建
cfg文件：打开cfg文，搜索yolo并修改classes，random，
/home/d/Desktop/darknet-master/cfg/yolov3-math-demo.cfg
/home/d/Desktop/darknet-master/cfg/yolov3-math-four.cfg
/home/d/Desktop/darknet-master/cfg/yolov3-math-four-demo.cfg
/home/d/Desktop/darknet-master/cfg/yolov3-math-fours.cfg
/home/d/Desktop/darknet-master/cfg/yolov3-math-fours-one.cfg
data文件：修改classe的类别数，train，valid，names的路径
/home/d/Desktop/darknet-master/cfg/math-four.data
/home/d/Desktop/darknet-master/cfg/math-fours.data
/home/d/Desktop/darknet-master/cfg/math-fours-one.data
/home/d/Desktop/darknet-master/cfg/maths.data
names文件：修改为自己标注的类别，一行一类，names文件均为自己创建
/home/d/Desktop/darknet-master/data/demo.names#测试用
/home/d/Desktop/darknet-master/data/math-four.names测试用
/home/d/Desktop/darknet-master/data/math-fours.names
/home/d/Desktop/darknet-master/data/math-fours-one.names
txt文件中为训练图片的路径（可以为相对路径）
/home/d/Desktop/darknet-master/scripts/2019_train.txt
测试图片的路径可以为相对路径）
/home/d/Desktop/darknet-master/scripts/2019_val.txt
全部图片的绝对路径
/home/d/Desktop/darknet-master/scripts/train.txt
类别标注的位置的归一化（图片和归一化的txt文件放在一起）
/home/d/Desktop/darknet-master/scripts/VOCdevkit/VOC2019/labels
/home/d/Desktop/darknet-master/scripts/VOCdevkit/VOC2019/JPEGImages
批量测试图片
/home/d/Desktop/darknet-master/tu
批量测试所需图片路径（相对路径）
/home/d/Desktop/darknet-master/test.txt
批量输出的文件夹
/home/d/Desktop/darknet-master/data/out
训练命令：./darknet detector train cfg/voc.data cfg/yolov3-voc.cfg darknet53.conv.74（darknet53.conv.74官网下载）
测试：./darknet detector test cfg/openimages.data cfg/yolov3-openimages.cfg yolov3-openimages.weights（训练的权重文件）*.png(jpg)
批量测试：./darknet detector test cfg/openimages.data cfg/yolov3-openimages.cfg yolov3-openimages.weights之后输入测试txt文件路径
