# Final-Project-Proposal
## 1. Purpose:
Dự đoán được yếu tố ảnh hưởng đến học viên từ đó giúp tăng tỷ lệ hoàn thành khóa học của học viên trên nền tảng trực tuyến, đồng thời:
- Xác định được yếu tố nào ảnh hưởng nhiều, yếu tố nào ảnh hưởng ít.
- Từ những yếu tố trên đưa ra được các biện pháp nâng cao giúp học viên có hiệu quả hơn khi học trực tuyến.
## 2. Expected Outcome:
Đưa ra được các biện pháp giúp học viên nâng cao hiệu quả hơn khi học trực tuyến tư đó giúp thu hút thêm nhiều học viên hơn.
## 3. Data Overview:
### Nguồn: Predict Online Course Engagement Dataset
https://www.kaggle.com/datasets/rabieelkharoua/predict-online-course-engagement-dataset
### Mô tả:
- Bộ dữ liệu này thu thập số liệu về mức độ tương tác của người dùng từ nền tảng khóa học trực tuyến, tạo điều kiện phân tích các yếu tố ảnh hưởng đến việc hoàn thành khóa học. Bộ dữ liệu này bao gồm dữ liệu cụ thể về khóa học và số liệu về mức độ tương tác.
### Structure:
- UserID: Mã định danh duy nhất cho mỗi người dùng
- CourseCategory: Danh mục khóa học mà người dùng đã tham gia (ví dụ: Lập trình, Kinh doanh, Nghệ thuật,...)
- TimeSpentOnCourse: Tổng thời gian người dùng dành cho khóa học, tính bằng giờ
- NumberOfVideosWatched: Tổng số video người dùng đã xem
- NumberOfQuizzesTaken: Tổng số bài kiểm tra người dùng đã làm
- QuizScores: Điểm trung bình người dùng đạt được trong các bài kiểm tra (tính theo phần trăm)
- CompletionRate: Tỷ lệ phần trăm nội dung khóa học người dùng đã hoàn thành
- DeviceType: Loại thiết bị người dùng sử dụng (Loại thiết bị: Máy tính để bàn (0) hoặc Điện thoại di động (1))
- **CourseCompletion (Target Variable):** Trạng thái hoàn thành khóa học (0: Chưa hoàn thành, 1: Đã hoàn thành)
## 4. Tools and Technologies:
- Programming Languages: Python
- Librabies:
  - _Reading and processing data:_ **(pandas, numpy)**
  - _Visualizing data:_ **(matplotlib, seaborn)**
  - _Building and evaluating logistic regression models_: **(sklearn)**
  - _Normalizing data_: **(sklearn)**
  - _Evaluating model performance:_ **(sklearn)**
  - _Working with string data:_ **(io)**
## 5. Key Insights Discover:
Key Insights (Những hiểu biết sâu sắc):

Tương quan dương mạnh mẽ giữa các yếu tố liên quan đến hoạt động học tập và hoàn thành khóa học:

Số lượng bài kiểm tra đã làm (NumberOfQuizzesTaken), điểm số bài kiểm tra (QuizScores) và tỷ lệ hoàn thành (CompletionRate) đều có tương quan dương đáng kể với tỷ lệ hoàn thành khóa học (CourseCompletion).
Điều này cho thấy rằng việc tham gia tích cực vào các hoạt động học tập, làm bài kiểm tra và theo dõi tiến độ học tập có liên quan chặt chẽ đến việc hoàn thành khóa học thành công.
Tương quan dương giữa thời gian dành cho khóa học, số lượng video đã xem và hoàn thành khóa học:

Thời gian dành cho khóa học (TimeSpentOnCourse) và số lượng video đã xem (NumberOfVideosWatched) cũng có tương quan dương với tỷ lệ hoàn thành khóa học (CourseCompletion), mặc dù mức độ tương quan không mạnh bằng các yếu tố trên.
Điều này cho thấy rằng việc dành thời gian cho khóa học và xem video có thể góp phần vào việc hoàn thành khóa học, nhưng có thể không phải là yếu tố quyết định duy nhất.
Tương quan âm yếu giữa một số yếu tố:

Có một số tương quan âm yếu giữa các yếu tố như số lượng bài kiểm tra đã làm (NumberOfQuizzesTaken), điểm số bài kiểm tra (QuizScores) với thời gian dành cho khóa học (TimeSpentOnCourse) và số lượng video đã xem (NumberOfVideosWatched).
Điều này có thể cho thấy rằng học sinh làm nhiều bài kiểm tra hơn hoặc có điểm kiểm tra cao hơn có thể dành ít thời gian hơn cho việc xem lại tài liệu hoặc video. Tuy nhiên, mức độ tương quan yếu cho thấy mối quan hệ này không quá đáng kể.
Thiết bị sử dụng (DeviceType) có tương quan rất yếu với các yếu tố khác:

Thiết bị sử dụng (DeviceType) có tương quan rất yếu với tất cả các yếu tố khác, cho thấy rằng loại thiết bị được sử dụng có thể không ảnh hưởng đáng kể đến kết quả học tập.


Hypotheses Based on the Insights (Các giả thuyết dựa trên những hiểu biết sâu sắc):

Giả thuyết 1: Học sinh hoàn thành nhiều bài kiểm tra hơn sẽ có tỷ lệ hoàn thành khóa học cao hơn.
Giả thuyết 2: Học sinh có điểm kiểm tra cao hơn sẽ có tỷ lệ hoàn thành khóa học cao hơn.
Giả thuyết 3: Học sinh có tỷ lệ hoàn thành các phần trong khóa học cao hơn sẽ có tỷ lệ hoàn thành toàn bộ khóa học cao hơn.
Giả thuyết 4: Học sinh dành nhiều thời gian cho khóa học hơn sẽ có tỷ lệ hoàn thành khóa học cao hơn.
Giả thuyết 5: Học sinh xem nhiều video hơn sẽ có tỷ lệ hoàn thành khóa học cao hơn.
Giả thuyết 6: Học sinh làm nhiều bài kiểm tra hơn có thể dành ít thời gian hơn cho việc xem lại tài liệu khóa học hoặc video.
Giả thuyết 7: Loại thiết bị được sử dụng không ảnh hưởng đáng kể đến kết quả học tập.

Recommendations Based on Analysis Results (Khuyến nghị dựa trên kết quả phân tích):

Tập trung vào các yếu tố ảnh hưởng mạnh đến việc hoàn thành khóa học:

Số lượng bài kiểm tra đã làm (NumberOfQuizzesTaken): Đây là yếu tố có tác động lớn nhất đến việc hoàn thành khóa học (coef = 0.3046). Khuyến khích học viên làm nhiều bài kiểm tra hơn bằng cách cung cấp các bài kiểm tra thường xuyên, bài kiểm tra thực hành và các hoạt động tương tác.
Điểm số bài kiểm tra (QuizScores): Điểm số bài kiểm tra cũng có tác động đáng kể (coef = 0.0721). Cung cấp phản hồi chi tiết về bài kiểm tra, tài liệu ôn tập và các buổi hỗ trợ để giúp học viên cải thiện điểm số.
Tỷ lệ hoàn thành (CompletionRate): Đây là yếu tố có tác động mạnh thứ hai (coef = 0.0360). Theo dõi tiến độ học tập của học viên và cung cấp hỗ trợ kịp thời cho những người có nguy cơ bỏ học.
Khuyến khích xem video và dành thời gian cho khóa học:

Số lượng video đã xem (NumberOfVideosWatched): Xem video có tác động tích cực đến việc hoàn thành khóa học (coef = 0.1272). Cung cấp các video hấp dẫn, dễ hiểu và có liên quan đến nội dung khóa học.
Thời gian dành cho khóa học (TimeSpentOnCourse): Dành thời gian cho khóa học cũng có tác động tích cực (coef = 0.0202). Khuyến khích học viên dành đủ thời gian cho việc học tập bằng cách cung cấp lịch trình học tập, nhắc nhở và các công cụ quản lý thời gian.
