# OAI_MUSH_HUTECH
ĐÂY LÀ REPO SOURCE CODE SOLUTION CHO CUỘC THI MUSHROOM IAMAGE CLASSIFICATION ĐƯỢC HỘI TIN HỌC VIỆT NAM VÀ TRƯỜNG HUTECH TỔ CHỨC
CÓ 2 FOLDER CHÍNH 1 FOLDER LÀ SRC CODE CHO VÒNG SEMI-FINAL VÀ 1 LÀ CHO VÒNG FINAL

## SEMI FINAL SOLUTION
### DATA PREPROCESS AND AUGMENT
Dựa vào quan sát dữ liệu ban đầu tụi em nhận thấy việc giữ nguyên ảnh gốc là 32*32 mang đi train cho các kiến trúc cnn sẽ không được kết quả tốt, vì vậy nhóm em đã sử dụng ISR (IMAGE SUPER-RESOLUTION) dùng để scale lại ảnh từ 32*32 lên 64

<div align="center">
    <img src="https://github.com/truong04/OAI_MUSH_HUTECH/blob/main/SRC/SEMI/ISR.png" alt="alt text" width="700"/>
</div> 


Sau thực nghiệm huấn luyện và kiểm thử model, nhóm chúng em nhận ra trong 4 class nấm thì có class số 2 bị ảnh hưởng bởi background có màu sặc sỡ nên tụi em đã augment ảnh xám bằng cách với mỗi ảnh màu sẽ tạo thêm 1 ảnh xám nữa như vậy mỗi class sẽ có n*2 số lượng (n là số ảnh gốc) mục đích của việc này là để model khi predict ít bị ảnh hưởng bởi background có màu sặc sỡ và muốn model tập trung vào hình dạng và các đường nét trên nấm nhưng cũng không bỏ ảnh màu để model vẫn có thể học được màu sắc của nấm.
<div align="center">
  <img src="https://github.com/truong04/OAI_MUSH_HUTECH/blob/main/SRC/SEMI/COLOR-XAM.png?raw=true" alt="alt text" width="700"/>
</div> 


### TRAINING AND EVAL
Trong quá trình thực nghiệm thì tụi em chọn model EfficientNetV2S phù hợp với tiêu chí là model nhẹ (tránh overfit do data train của btc chỉ có 1400 mẫu) nhưng cũng cho hiệu suất tốt, kết quả cuối cùng của nhóm đạt được 91% accuracy trên vòng public test xếp thứ 12 và được tham dự vòng chung kết (các tham số huấn luyện đều nằm trong code)

Confusion matrix cuối cùng khi đã cải thiện được độ phủ của class 2 từ chỉ 90/150 sample đúng lên 124/150 đúng
<div align="center">
  <img src="https://github.com/truong04/OAI_MUSH_HUTECH/blob/main/SRC/SEMI/EVAL.jpg" alt="alt text" width="700"/>
</div> 

## SEMI FINAL SOLUTION
### DATA PREPROCESS AND AUGMENT
Dựa vào quan sát dữ liệu ban đầu tụi em nhận thấy việc giữ nguyên ảnh gốc là 32*32 mang đi train cho các kiến trúc cnn sẽ không được kết quả tốt, vì vậy nhóm em đã sử dụng ISR (IMAGE SUPER-RESOLUTION) dùng để scale lại ảnh từ 32*32 lên 64

<div align="center">
    <img src="https://github.com/truong04/OAI_MUSH_HUTECH/blob/main/SRC/SEMI/ISR.png" alt="alt text" width="700"/>
</div> 


Sau thực nghiệm huấn luyện và kiểm thử model, nhóm chúng em nhận ra trong 4 class nấm thì có class số 2 bị ảnh hưởng bởi background có màu sặc sỡ nên tụi em đã augment ảnh xám bằng cách với mỗi ảnh màu sẽ tạo thêm 1 ảnh xám nữa như vậy mỗi class sẽ có n*2 số lượng (n là số ảnh gốc) mục đích của việc này là để model khi predict ít bị ảnh hưởng bởi background có màu sặc sỡ và muốn model tập trung vào hình dạng và các đường nét trên nấm nhưng cũng không bỏ ảnh màu để model vẫn có thể học được màu sắc của nấm.
<div align="center">
  <img src="https://github.com/truong04/OAI_MUSH_HUTECH/blob/main/SRC/SEMI/COLOR-XAM.png?raw=true" alt="alt text" width="700"/>
</div> 


### TRAINING AND EVAL
Trong quá trình thực nghiệm thì tụi em chọn model EfficientNetV2S phù hợp với tiêu chí là model nhẹ (tránh overfit do data train của btc chỉ có 1400 mẫu) nhưng cũng cho hiệu suất tốt, kết quả cuối cùng của nhóm đạt được 91% accuracy trên vòng public test xếp thứ 12 và được tham dự vòng chung kết (các tham số huấn luyện đều nằm trong code)

Confusion matrix cuối cùng khi đã cải thiện được độ phủ của class 2 từ chỉ 90/150 sample đúng lên 124/150 đúng
<div align="center">
  <img src="https://github.com/truong04/OAI_MUSH_HUTECH/blob/main/SRC/SEMI/EVAL.jpg" alt="alt text" width="700"/>
</div> 





