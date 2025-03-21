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
### 1. Tác động của các yếu tố đến với khả năng hoàn thành khóa học:
- Quizzes Taken (Số lượng bài kiểm tra đã làm): Cho thấy rằng việc học viên làm nhiều bài kiểm tra có liên quan chặt chẽ đến việc họ hoàn thành khóa học.
- Videos Watched (Số video đã xem): Cho thấy rằng việc xem video bài giảng có ảnh hưởng tích cực đến khả năng hoàn thành khóa học.
- Quizzes Scores (Điểm trung bình các bài kiểm tra): Cho thấy rằng điểm số trong các bài kiểm tra cũng có mối liên hệ với việc hoàn thành khóa học, nhưng không mạnh mẽ bằng số lượng bài kiểm tra đã làm hay số lượng video đã xem.
- Time Spent (Thời gian học): Cho thấy rằng thời gian học không phải là yếu tố quyết định đến khả năng hoàn thành khóa học.
### 2.  Tầm quan trọng của việc tương tác và đánh giá:
Cho thấy rằng việc học viên tương tác với các bài kiểm tra (cả về số lượng và chất lượng) đóng vai trò quan trọng trong việc dự đoán khả năng hoàn thành khóa học. Đồng thời cũng nhấn mạnh tầm quan trọng của việc học viên chủ động tiếp thu kiến thức thông qua video bài giảng.
### 3.  Thời gian học không phải là yếu tố quyết định:
Điều này có thể cho thấy rằng chất lượng học tập (thể hiện qua việc làm bài kiểm tra và xem video) quan trọng hơn số lượng thời gian học.
