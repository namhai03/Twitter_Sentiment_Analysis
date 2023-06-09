# Twitter_Sentiment_Analysis
## Giới thiệu 

Phân tích tình cảm đề cập đến việc xác định cũng như phân loại các tình cảm được thể hiện trong nguồn văn bản. Tweets thường hữu ích trong việc tạo ra một lượng lớn dữ liệu tình cảm khi phân tích. Những dữ liệu này rất hữu ích trong việc hiểu ý kiến của mọi người về nhiều chủ đề khác nhau.

Do đó, chúng tôi cần phát triển Mô hình phân tích tình cảm học máy tự động để tính toán nhận thức của khách hàng. Do sự hiện diện của các ký tự không hữu ích (collectively termed as the noise) cùng với dữ liệu hữu ích.

Mục đích của tôi là phân tích cảm xúc của các tweet được cung cấp từ bộ dữ liệu bằng cách phát triển một quy trình học máy liên quan đến việc sử dụng ba bộ phân loại (	Linear Support Vector Classifier, Bernoulli Naive Bayes và RandomForest) cùng với việc sử dụng Term Frequency- Inverse Document Frequency (TF-IDF ). 

## Problem Statement

Trong dự án này, tôi cố gắng triển khai mô hình phân tích tình cảm Twitter giúp vượt qua những thách thức trong việc xác định tình cảm của các tweet.

Các đặc tính liên quan đến tập dữ liệu là:

1. ids: ID mỗi Tweets

2. date: Thời gian đăng bình luận

3. flag: Nó đề cập đến truy vấn. Nếu không có truy vấn nào như vậy tồn tại thì không có câu hỏi.

4. user: Tên user đăng bình luận

5. text: Nội dung bình luận

6. Sentiment: Gán nhãn mỗi tweet

## Project Pipeline

Các bước thực hiện:

1. Import các thư viện cần thiết

2. Đọc và ghi tập dữ liệu 

3. Thông tin và kiểu dữ liệu

4. Tiền xử lí dữ liệu

5. Trực quan hóa 

6. Tách dữ liệu thành tập train, test

7. Chuyển đổi dữ liệu bằng TF-IDF Vectorizer

8. Xây dựng mô hình 

## Data Preprocessing
Trong bài toán được đưa ra ở trên, trước khi huấn luyện mô hình, tôi đã thực hiện một số bước tiền xử lý trên tập dữ liệu, chủ yếu liên quan đến việc loại bỏ stopword (từ dừng), loại bỏ emojis (biểu tượng cảm xúc). Sau đó, văn bản được chuyển đổi thành chữ thường để tăng tính tổng quát hóa.

Tiếp theo, dấu câu được làm sạch và loại bỏ, giúp giảm bớt các nhiễu không cần thiết trong tập dữ liệu. Sau đó, chúng tôi cũng loại bỏ các ký tự lặp lại trong từ cũng như loại bỏ các URL vì chúng không có ý nghĩa quan trọng.

Cuối cùng, chúng tôi đã thực hiện Stemming (giảm từ xuống dạng gốc của chúng) và Lemmatization (giảm các từ xuống dạng gốc gọi là "lemma") để đạt được kết quả tốt hơn.


