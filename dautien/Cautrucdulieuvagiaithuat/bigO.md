
## big O là gì ?



Thuật toán là một một chuôi các thủ tục nhằm thưc hiện một nhiệm vụ nào đó với số bước thực hiện là hữu hạn.Có thể coi từng dòng code của bạn là thuật toán . Đế đánh giá thuật toán người ta dùng kí hiệu chữ "O lớn".Tạm thời để nó qua 1 bên ta xét trường hợp sau .VTV3 trong khoảng thời gian này phát sóng chương trình "chọn đâu cho đúng " .Đến vòn cuối cùng MC đọc câu hỏi có đáp án là số ,và người chơi đưa ra câu trả lời.Nếu câu trả lời cao hơn so với đáp án MC nhắc nhở "xuống" ,còn thấp hơn thì nhắc nhở "lên".Yêu cầu trong 90 giây trả lời được 5 câu hỏi là giành được giải thường cao nhất của chương trình.

Như vậy cần đưa ra được đáp án đúng với số bước đoán cang it càng tốt .Cách mà nhiều người chơi là đọc lần lượi cho đến khi đạt được kêt quả đúng . Đây là cách mà chắc chắn không lập trình viên nào lựa chọn.
    VD Câu hỏi "mĩ ném bom xuống Hiroshima năm bao nhiêu ".thay vì liệt kê lần lượi từ 1900 đên 2000 hãy bắt đầu với 1950 rồi nhận được nhắc nhở là nhỏ hơn bạn tiếp tục đoán 1925 -> Lớn hơn->1933 ->lớn hơn _>1945 >chính xác . rõ ràng cách này giảm được rất nhiều bước. 

Mỗi khi nhắc đến thuật toán cái mà người ta nhắc kem theo luôn là thời gian chạy(running time).như ví dụ trên:nếu mỗi lần đoán mất 1 giây ,theo cách bình thường ta mất 45 giây,còn tìm theo số ở giữa ta mất 4s .Kí hiệu "chữ O lớn"  là kí tự đặc biệt cho bạn biết mức độ nhanh của thuật toán . Các kí hiệu thường gặp:O(n),O(logn),O(nLogn),O(n*n),O(n!),...Trong Kí hiệu O Log n Là logarit cơ số 2 của n .

Nếu hiếu theo cách đơn giản mỗi vòng for bạn lặp từ 0 đến n thì cho ta thời gian chạy là n.Lồng trong đó 1 vòng for tương tự ta có thời gian chạy là n*n,độ tăng chường 1 số thuật toán cho bởi hình sau   :

![image-20200818114827207](image-20200818114827207.png)

Thời gian chạy một số thuật toán cơ bản :

+ O(log n),được gọi là "log time".Ví dụ :tìm kiếm nhị phân
+ O(n) ,được gọi là "linear time",Ví dụ: tìm kiếm đơn giản
+ O(n*log n) ,Ví dụ: Thuật toán sắp xếp nhanh (quicksort)
+ O(n^2) ,Ví dụ : Các thuật toán sắp xếp cơ bản như nổi bọt ,chèn ,chọn
+ O(n!) ,Ví dụ: thuật toán cho bài toán người du lịch

