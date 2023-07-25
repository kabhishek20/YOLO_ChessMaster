# YOLO_ChessMaster

> Ever played chess?? Do you have any idea what [lichess](https://lichess.org/) is?  
> Well it is a platform where chess lovers from any part of the world meet and compete among them. Interesting enough??

Here is a <code>**computer vision project**</code> related to something on that platform.
This has been made using <code>**python**</code> with the help of <code>**YoloV5**</code>. Tried out Yolov4 but took many hours of training so shifted to Yolov5 :(

The project includes:
- <code>**Collecting snapshots**</code> from Lichess, <code>**annotating it**</code> and making a <code>**dataset out of in YAML format**</code> for Yolo to understand.
- <code>**Training the computer vision model**</code> with the annotated images so that it can learn about the <code>**features and edges**</code>.
- <code>**Testing and storing the weight**</code> of the trained model for future use (If weights are not stored, then training it again will take 2 hours)

> How was the training process? How many images was it trained on?  
 Well, the model was trained for <code>**6 different classes**</code> (King, Queen, Pawn, Knight, Rook, Bishop). The number of instances of each class is in the image below.
![Class Labels](labels.jpg)


The images of training were resized to <code>**640*640**</code> and <code>**data augmentation**</code> was performed on the training dataset before training. The <code>**batch size was 16**</code> for 1 epoch and the model was trained for <code>**1381 epochs**</code>.
Training batch snapshots:


![Class Labels](train_batch0.jpg)
![Class Labels](train_batch1.jpg)
![Class Labels](train_batch2.jpg)

> So, what are the final outcomes?  
> The model can identify any chess piece and name it accordingly whether it is a king, queen, bishop, knight, pawn, or rook. It is working on images in any format as of now but can be implemented in real-time as well.

> What about the "Performance of model"?  
> The model has <code>**excellent performance**</code> (literally more than what I thought). The overall <code>**mAP(mean Average Precision) of the model is 99.30%**</code> with <code>**precision and recall as 0.933 and 0.971**</code> respectively. Going with the statement "picture speaks more than words" adding a few snapshots:



![model_summary](model_summary.png)
![Confusion Matrix](confusion_matrix.png)
![F1 Curve](F1_curve.png)
![P Curve](P_curve.png)
![R Curve](R_curve.png)
![Results](results.png)

