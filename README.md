# shiba-inu-san

## 動作環境  
OS: Ubuntu16.04 on VirtualBox  
Python: 3.5.6  
TensorFlow: 1.10.1  
メモリ: 2G  
  
## 実行コマンド
**学習**
```
python retrain.py \
  --bottleneck_dir=bottlenecks \
  --saved_model_dir=inception \
  --summaries_dir=training_summaries/basic \
  --output_graph=retrained_graph.pb \
  --output_labels=retrained_labels.txt \
  --image_dir=learning_data
```
  
**判別**
```
# 柴犬判別
python label_image.py --image shiba_Inu.jpg --graph retrained_graph.pb --labels retrained_labels.txt

# 秋田犬判別
python label_image.py --image akita_inu.jpeg --graph retrained_graph.pb --labels retrained_labels.txt

# 紀州犬判別
python label_image.py --image kishu.jpg --graph retrained_graph.pb --labels retrained_labels.txt
```
