![Ảnh màn hình 2024-09-05 lúc 18 44 05](https://github.com/user-attachments/assets/6f030cbb-82ca-4839-a254-4f5a35a040c6)

- 20 bài cho 4 điểm

- bài thi 6 câu 

- 4 bài tập cộng điểm, sẽ không có phần giải thích, deadline 2 ngày sau khi giao bài tập + điểm

![Ảnh màn hình 2024-09-05 lúc 18 47 31](https://github.com/user-attachments/assets/db89622c-dd3e-4995-81da-784bc88dbce3)

- Apache spark standalone worker là ndung sẽ học trong buổi offline

- Phải giải quyết bài tập và bài thi bằng môi trường Pyspark và big data, không dc dùng sklearn và machine learning truyển thông

# Buổi 1: Tổng quan Big Data (05/09/2024)

## 1. Giới thiệu Big Data 

-  "Dữ liệu lớn là một lĩnh vực áp dụng các phương pháp để phân tích, trích xuất thông tin một cách có hệ thống hoặc xử lý các tập dữ liệu quá lớn hoặc phức tạp khó có thể xử lý bằng các ứng dụng xử lý dữ liệu truyền thống."

-  Gồm có cấu trúc và không có cấu trúc. Nhưng khối lượng dữ liệu không quan trọng, những gì tổ chức làm với dữ liệu mới quan trọng. -> làm cho dữ liệu tạo ra giá trị thì mới quan trọng.

**Lịch sử của Big Data**

- Sự xuất hiện của các open-source framework như Hadoop và Spark đã làm cho việc xử lý và lưu trữ dữ liệu lớn trở nên dễ dàng và chi phí thấp hơn.

## 2. Thuật ngữ

**Cluster Computing**

- Computer cluster là một tập hợp các máy tính được kết nối lỏng lẻo hoặc kết nối chặt chẽ với nhau và chúng có thể được xem như một hệ thống duy nhất. Không giống grid computer, computer cluster có mỗi node được thiết lập để thực hiện cùng một tác vụ, được điều khiển và lên lịch bởi phần mềm.

- Clustered computing: thu thập nhiều tài nguyên từ nhiều máy

<img width="779" alt="Ảnh màn hình 2024-09-05 lúc 20 01 50" src="https://github.com/user-attachments/assets/c89557e0-568c-4d86-8c15-6bc4ece6bbb4">

**Parallel computing:**

**Distributed computing:**

**Batch processing:**

- Chia công việc thành từng phần nhỏ và chạy chúng trên các máy riêng lẻ

<img width="409" alt="Ảnh màn hình 2024-09-05 lúc 20 09 49" src="https://github.com/user-attachments/assets/e804bc97-3171-4680-940e-780258c48b3d">

**Real-time processing:**

- hiện giờ hay dùng RAG

## 3. Thuộc tính của Big Data 

**The Vs' of Big Data**

<img width="441" alt="Ảnh màn hình 2024-09-05 lúc 20 37 54" src="https://github.com/user-attachments/assets/33590110-8db5-4f6f-92fb-6b1963415ce7">

- Velocity

- Volume

- Variety

## 4. Kỹ thuật xử lý

**Batch processing:**
  
- thường được sử dụng khi chúng ta quan tâm đến khối lượng BIG DATA (volume) và sự đa dạng (variety) của dữ liệu.

**Stream processing (Realtime processing)**

- thường được sử dụng nếu chúng ta quan tâm đến thời gian phản hồi nhanh, xử lý dữ liệu ngay khi nhận được (độ trễ thấp).

**Hệ thông xử lý Big Data**

- Hadoop/MapReduce: Scalable & fault tolerant framework viết bằng Java (Open source, Batch processing)

- Apache Spark: hệ thống điện toán theo cụm siêu nhanh (lightning fast cluster computing system) (Open source, Batch processing &real-time processing)

## 5. Giới thiệu Apache Spark

**Đặt vấn đề**

<img width="669" alt="Ảnh màn hình 2024-09-05 lúc 20 59 43" src="https://github.com/user-attachments/assets/a48bed45-a62c-4bcc-8cf2-0daaa2ec0f1d">

**Đặc điểm của Distributed System**

- Distributed process có thể truy cập đến tài nguyên tính toán trên một số máy tính được kết nối qua mạng.

- Các máy tính được phân tán dễ dàng mở rộng quy mô, chỉ cần thêm nhiều máy hơn.

- Có khả năng chịu lỗi, nếu một máy bị lỗi, toàn bộ mạng vẫn có thể tiếp tục.

**ApacheTMT Hadoop®**

- Apache Hadoop software library là một framework cho phép xử lý phân tán các tập dữ liệu lớn trên các cụm máy tính bằng các mô hình lập trình đơn giản. Nó được thiết kế để mở rộng quy mô từ các máy chủ đơn lẻ đến hàng ngàn máy, mỗi máy cung cấp tính toán và lưu trữ cục bộ.

<img width="468" alt="Ảnh màn hình 2024-09-05 lúc 21 06 39" src="https://github.com/user-attachments/assets/ba3eb5e1-e460-48ad-ad18-5c6725641436">

**Apache Spark**

- Là một công cụ phân tích hợp nhất để xử lý dữ liệu quy mô lớn.

- Là một trong những công nghệ mới nhất đang được sử dụng để xử ýl Big Data nhanh chóng và dễ dàng.

- Là một Apache open source project

- Được AMPLab tại UC Berkeley công bố lần đầu vào tháng 02/2013

- Rất phổ biến vì rất dễ sử dụng và có tốc độ nhanh.

**Lý do chọn Apache Spark?**

- Tốc độ (speed): thực hiện khối lượng công việc (workloads) nhanh hơn so với Hadoop (hơn 100 lần so với trong memory, hơn 10 lần so với trên disk).

- Hiệu năng cao (high performance) cho cả dữ liệu theo batch và streaming, sử dụng bộ lập lịch DAG (Directed Acyclic Graph) hiện đại (state-of-the-art DAG scheduler), tối ưu hóa truy vấn và công cụ thực thi vật  (physical execution engine).

**Spark vs MapReduce**

- MapReduce ghi hầu hết dữ liệu vào đĩa sau mỗi map và reduce operation

- Spark giữ hầu hết dữ liệu trong bộ nhớ sau mỗi lần chuyển đổi (transformation)

- Spark có thể tràn ra disk nếu memory đầy.

- Spark thực hiện công việc nhanh hơn 100 lần so với MapReduce.

## 6. Apache Spark Components

<img width="939" alt="Ảnh màn hình 2024-09-05 lúc 21 23 46" src="https://github.com/user-attachments/assets/58565a4e-3681-466d-9723-8c16901052c3">

# Buổi 2: Tổng quan PySpark (07/09/2024)

## 1. Giới thiệu PySpark 

PySpark là Python API dành cho Spark được phát hành bởi cộng đồng Apache Spark giúp hỗ trợ Python với Spark.

**Đặc điểm chính của PySpark**

- Real time computations: thực hiện tính toán BIG DATA trên thời gian thực, với in-memory processing trong PySpark framework có độ trễ thấp (low
latency)

- Polyglot: PySpark framework tương thích với các ngôn ngữ khác nhau 

- Caching &disk persistence

- Fast processing

- Works well with RDD

## 2. Lý do chọn PySpark

## 3. Cài đặt & cầu hình PySpark

## 4. Spark Context, Spark Session

**Spark Context**

- SparkContext là thành phần trung tâm giúp thiết lập môi trường thực thi Spark và cung cấp các công cụ cần thiết để làm việc với dữ liệu phân tán trên cụm Spark. (phòng khách)

**Spark Session**

- SparkSession là cổng vào hợp nhất của Spark, giúp đơn giản hóa việc quản lý các chức năng và tài nguyên của Spark, đồng thời cung cấp một API dễ sử dụng cho các thao tác xử lý dữ liệu.

- entry point, chìa khoá để mở cửa bước vào căn phòng hỗ trợ cho data set, data frame, tiền xử lý dữ liệu

- function dùng cho không gian chung (SC) thì có thể dùng trong không gian riêng, nhưng không gian riêng thì chỉ có không gian riêng dùng, trừ khi đc cho phép.

# Buổi 2: PySpark RDDs (07/09/2024)

## 1. Giới thiệu RDDs 

- R (Resilient - khả năng phục hồi)

- D (Distributed - phân phối)

- Ds (Datasets - bộ dữ liệu)

<img width="552" alt="Ảnh màn hình 2024-09-07 lúc 10 27 36" src="https://github.com/user-attachments/assets/16e9c3dd-02e3-4b16-bcfd-6d4d7cff87be">

## 2. RDDs operations

- Có hai thao tác cơ bản có thể được thực hiện trên RDD, đó là: Transformation và Action

**Transformation**

<img width="888" alt="Ảnh màn hình 2024-09-07 lúc 10 40 59" src="https://github.com/user-attachments/assets/fe40f443-03a7-477d-9ca4-5a991c6c6e4d">

**Action**

- Các Action trong Spark là các hàm trả về kết quả cuối cùng của các tính toán RDD. sử dụng lineage graph để tải dữ liệu lên Nó theo một thứ tự cụ thể. Sau khi tất cả các transformation được thực hiện, action trả về kết quả cuối cùng cho Spark Driver. Action là operation cung cấp non-RDD value.

<img width="833" alt="Ảnh màn hình 2024-09-07 lúc 10 43 40" src="https://github.com/user-attachments/assets/3e9f54b0-e316-4414-9f7c-c3ba4b396027">

## 3. Làm việc với RDDs

**Cách tạo RDD**

- Sử dụng parallelize(collection) để tạo ra RDD

- Sử dụng getNumPartitions(): để lấy số lượng partition đang có của RDD.
