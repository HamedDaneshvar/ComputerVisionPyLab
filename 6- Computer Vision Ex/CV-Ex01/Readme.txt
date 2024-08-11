Image_Segmentation: this file using U-Net model with all of dataset size -> every epoch about 12 min -> 10 epochs
Image_Segmentation_method1: this file using U-Net model with half of dataset size and more epochs -> every epoch about 6 min -> 25 epochs
Image_Segmentation_method2: this file using U-Net model with ResNet50 encoders section and half of dataset size and more epochs -> every epoch about 8 min -> 25 epochs


Image_Segmentation with 10 epoch and all of dataset
accuracy: 0.3579 - loss: 2.6065 - val_accuracy: 0.3546 - val_loss: 2.6536
Mean IoU on test data: 0.0741


Image_Segmentation_method1 with 25 epoch and half of dataset -> same condition with method 2
accuracy: 0.4211 - loss: 2.2797 - val_accuracy: 0.3620 - val_loss: 2.6324
Mean IoU on test data: 0.0771



Image_Segmentation_method2 with 25 epoch and half of dataset -> same condition with method 1
accuracy: 0.5154 - loss: 1.8382 - val_accuracy: 0.3255 - val_loss: 3.0995
Mean IoU on test data: 0.0721


description and compare these three files:
In the Image_Segmentation file, the UNET model was used along with all the dataset and the model was trained with 10 epochs. Also, the Image_Segmentation_method1 file is the same as the previous file, but half of the dataset is used and the model is trained with 25 epochs, and the Image_Segmentation_method2 file also uses the same half of the dataset as the previous file and also 25 epochs are trained, but instead of fully using the architecture UNET, its encoder part has been changed with ResNet50 model encoder, but the UNET architecture is completely used in the Image_Segmentation_method1 file.
The accuracy of the model in the Image_Segmentation file on the training and validation test data is very accurate and the difference between the two accuracy is small, but in the other two files, the accuracy difference between the training and validation test data is high, and this indicates that reducing the data sets the model towards Overfitting is a slave and if we had more resources and trained the first file i.e. Image_Segmentation more, we would have gotten better results. The mAP criterion is also in all three files with a thousandth difference that all three models have predicted the classes almost correctly and since the second model i.e. Image_Segmentation_method1 has the highest mAP, then it can be concluded that if the first model had more training, the result We would get better.
The model created by the Image_Segmentation_method2 file has the largest volume, i.e. 504 MB, but the models created by the other two files have a volume of 359 MB.


توضیحات و مقایسه هر سه فایل:
در فایل Image_Segmentation که ازمدل UNET به همراه تمام دیتاست استفاده شد و مدل با 10 epoch آموزش دیده شد. همچنین فایل Image_Segmentation_method1 نیز مانند حالت فایل قبلی است ولی از نصف دیتاست استفاده شده و مدل با 25 epoch آموزش دیده است و فایل Image_Segmentation_method2 نیز از همان نصف دیتاست فایل قبل استفاده کرده و همچنین 25 Epoch آموزش دیده است ولی از به جای استفاده کامل از معماری UNET، قسمت encoder آن با encoder مدل ResNet50 تغییر کرده است ولی در فایل Image_Segmentation_method1 کاملا از معماریUNET استفاده شده است.
دقت مدل در فایل Image_Segmentation روی داده های آموزشی و validation test دقت خوبی دارد و اختلاف دو دقت کم است ولی در دو فایل دیگر تفاوت دقت داده های آموزشی و validation test زیاد است و این نشان دهنده این است که کم کردن دیتاست مدل را به سمت overfit شدن برده است و در صورتی که اگر ریسورس بیشتری داشتیم و فایل اول را یعنی Image_Segmentation را بیشتر آموزش میدادیم نتیجه بهتری میگرفتیم. معیار mAP نیز در هر سه فایل با اختلاف هزارم است که هر سه مدل تقریبا کلاس ها را درست پیش بینی کرده اند و چون مدل دوم یعنی Image_Segmentation_method1 دارای بیشترین mAP است پس از این حالت نیز میتوان نتیجه گرفت که اگر مدل اول آموزش بیشتری میدید نتیجه بهتری میگرفتیم.
مدل ساخته شده توسط فایل Image_Segmentation_method2 دارای بیشترین حجم یعنی 504 MB است ولی مدل های ساخته شده توسط دو فایل دیگر 359 MB حجم دارد.
