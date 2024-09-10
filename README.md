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

**Parallel computing:(kết nối chặt chẽ)**

- xử lý tính toán song là một phương pháp tính toán trong đó nhiều tác vụ được thực hiện đồng thời (cùng lúc) để tăng tốc độ xử lý và hiệu quả. 

- Parallel computing là kết nối chặt chẽ vì các bộ xử lý cần hoạt động đồng bộ và chia sẻ tài nguyên chung, làm việc song song trên cùng một bài toán, với yêu cầu giao tiếp nhanh và liên tục.

**Distributed computing: (kết nối lỏng lẻo)**

- Tính toán phân tán là một hệ thống gồm nhiều máy tính độc lập (có thể nằm ở các địa điểm khác nhau) kết nối với nhau qua mạng để thực hiện các nhiệm vụ chung.

- Distributed computing là kết nối lỏng lẻo vì các máy tính có thể hoạt động độc lập với nhau, giao tiếp qua mạng và không cần phải đồng bộ hóa liên tục. Các máy tính ở xa nhau và xử lý các phần khác nhau của công việc.

**Batch processing:**

- Chia công việc thành từng phần nhỏ và chạy chúng trên các máy riêng lẻ

- (xử lý theo lô) là phương pháp xử lý dữ liệu hoặc các công việc tính toán theo nhóm (lô) mà không cần sự can thiệp của người dùng trong quá trình thực hiện.

<img width="409" alt="Ảnh màn hình 2024-09-05 lúc 20 09 49" src="https://github.com/user-attachments/assets/e804bc97-3171-4680-940e-780258c48b3d">

**Real-time processing:**

- Xử lý dữ liệu tức thời

- hiện giờ hay dùng RAG

![Ảnh màn hình 2024-09-10 lúc 14 59 08](https://github.com/user-attachments/assets/cb02f9c4-4a36-44d3-9c46-dbd3f0e4cea3)

## 3. Thuộc tính của Big Data 

**The Vs' of Big Data**

<img width="441" alt="Ảnh màn hình 2024-09-05 lúc 20 37 54" src="https://github.com/user-attachments/assets/33590110-8db5-4f6f-92fb-6b1963415ce7">

![Ảnh màn hình 2024-09-10 lúc 15 03 06](https://github.com/user-attachments/assets/3c12d66d-1d4b-4fdb-9e51-80c905c1684f)

- Velocity: đề cập đến tốc độ tạo dữ liệu mới và tốc độ di chuyển dữ liệu.

- Volume: đề cập đến khối lượng dữ liệu khổng lồ được tạo ra mỗi giây.

- Variety: đề cập đến các loại dữ liệu khác nhau mà chúng ta sử dụng hiện nay (ví dụ: tin nhắn, hình ảnh, dữ liệu cảm biến, video hoặc ghi âm giọng nói, dữ liệu có cấu trúc truyền thống...)

- Veracity: liên quan đến độ tin cậy của dữ liệu, đặc biệt là khi chất lượng và độ chính xác khó kiểm soát

- Value đề cập đến khả năng biến dữ liệu thành các giá trị.

- VARIABILITY: The ways in which the big data can be used and 

## 4. Kỹ thuật xử lý

**Batch processing:**
  
- thường được sử dụng khi chúng ta quan tâm đến khối lượng BIG DATA (volume) và sự đa dạng (variety) của dữ liệu. Trước tiên, chúng ta lưu trữ tất cả các dữ liệu cần thiết và sau đó xử lý nó trong một lần (điều này có thể dẫn đến độ trễ cao). (tính toán tổng hợp tiền lương hàng tháng, tổng hợp số liệu báo cáo định kỳ.)

**Stream processing (Realtime processing)**

- thường được sử dụng nếu chúng ta quan tâm đến thời gian phản hồi nhanh, xử lý dữ liệu ngay khi nhận được (độ trễ thấp). (Hệ thống phân tích luồng dữ liệu nhằm phát hiện các giao dịch bất thường và đưa ra cảnh báo gian lận; đồng thời, hệ thống này cũng được áp dụng trong giám sát giao thông để phát hiện kẹt xe, tai nạn và tự động điều chỉnh tín hiệu đèn giao thông nhằm đảm bảo lưu thông hiệu quả.)

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

- Hadoop Distributed File System (HDFS)

- Yarn

- MapReduce

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

-  Spark Core: Spark Core là thành phần cốt lõi của Apache Spark, chịu trách nhiệm điều phối và quản lý toàn bộ hệ thống. Nó cung cấp các chức năng cơ bản như quản lý bộ nhớ, thực hiện tác vụ và lên lịch các công việc tính toán. Spark Core cho phép xử lý dữ liệu trong bộ nhớ (in-memory), giúp tốc độ tính toán nhanh hơn so với việc đọc ghi trên ổ cứng.

- RDD là cấu trúc dữ liệu chính trong Spark, đại diện cho một tập hợp dữ liệu lớn được chia nhỏ và phân tán trên nhiều máy tính. RDD có khả năng phục hồi sau sự cố (resilient), có nghĩa là nếu một phần dữ liệu bị mất hoặc lỗi, nó có thể được tính toán lại từ các bước trước đó mà không ảnh hưởng đến toàn bộ quá trình. RDD hỗ trợ xử lý song song và phân tán, giúp Spark xử lý dữ liệu lớn một cách nhanh chóng và hiệu quả.

- Spark SQL: Spark SQL là một mô-đun trong Apache Spark cho phép làm việc với dữ liệu có cấu trúc, như các bảng hoặc cơ sở dữ liệu. Nó cung cấp khả năng truy vấn dữ liệu bằng ngôn ngữ SQL quen thuộc và cũng có thể kết hợp với các công cụ dữ liệu khác như Hive. Spark SQL giúp người dùng xử lý và phân tích dữ liệu có cấu trúc hoặc bán cấu trúc một cách dễ dàng.

-  MLlib: MLlib là thư viện machine learning (học máy) trong Apache Spark. Nó cung cấp các thuật toán và công cụ để xây dựng và huấn luyện các mô hình học máy như phân loại, hồi quy, phân cụm, và xử lý dữ liệu. MLlib hỗ trợ xử lý trên dữ liệu lớn và giúp dễ dàng triển khai các mô hình học máy trong môi trường phân tán.

- GraphX: là một mô-đun của Spark dành cho việc xử lý và phân tích dữ liệu đồ thị (graph data), như các mạng xã hội, đồ thị liên kết.
Nó cung cấp các công cụ để thao tác, tính toán trên đồ thị (nodes, edges), đồng thời hỗ trợ các thuật toán phân tích đồ thị như PageRank.
GraphX giúp phân tích các cấu trúc dữ liệu phức tạp và tìm ra các mối quan hệ giữa các phần tử trong dữ liệu.

- Spark Streaming: Add-on của API Spark cho phép xử lý luồng dữ liệu trực tiếp với khả năng mở rộng và thông lượng cao, giúp xử lý dữ liệu một cách hiệu quả. Hệ thống này có thể hoạt động bằng nhiều thuật toán khác nhau, và sau khi dữ liệu được nhận, nó sẽ được cung cấp cho các file cơ sở dữ liệu hoặc hiển thị trên các dashboard trực tiếp. Spark sử dụng phương pháp micro-batching để thực hiện việc streaming thời gian thực (real-time streaming), chia dữ liệu thành các lô nhỏ để xử lý liên tục. Quá trình này diễn ra qua 3 giai đoạn: Gathering (thu thập dữ liệu), Processing (xử lý dữ liệu), và Data Storage (lưu trữ dữ liệu).

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

- SparkContext là entry point cho bất kỳ chức năng nào của Spark.

- Nó chịu trách nhiệm kết nối ứng dụng với Spark Cluster, quản lý tài nguyên và phân phối công việc cho các worker node (máy tính xử lý)

- SparkContext là thành phần trung tâm giúp thiết lập môi trường thực thi Spark và cung cấp các công cụ cần thiết để làm việc với dữ liệu phân tán trên cụm Spark. (phòng khách)

**Spark Session**

- SparkSession là cổng vào hợp nhất của Spark, giúp đơn giản hóa việc quản lý các chức năng và tài nguyên của Spark, đồng thời cung cấp một API dễ sử dụng cho các thao tác xử lý dữ liệu.

- Spark Session cho phép truy cập đến tất cả các chức năng của Spark (SQL, DataFrame, Streaming) trong một đối tượng duy nhất.

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

![Ảnh màn hình 2024-09-10 lúc 17 54 35](https://github.com/user-attachments/assets/bb76aa4e-40d8-4c5a-a91b-21471d734fbf)

## 3. Làm việc với RDDs

**Cách tạo RDD**

- Sử dụng parallelize(collection) để tạo ra RDD

- Sử dụng getNumPartitions(): để lấy số lượng partition đang có của RDD.

Chú ý: sc (SparkContext) chỉ khai báo và run 1 lần trong một ứng dụng.

- Sử dụng textFile("tên file", [minPartitions]) để tạo RDD từ dữ liệu bên ngoài.

# Buổi 2: PySpark RDDs (07/09/2024) (tt)

**RDD operation cơ bản**

***Transformation***

- Transformation là các thao tác được áp dụng lên RDD để tạo ra một RDD mới. Tuy nhiên, chúng không thực thi ngay lập tức mà chỉ được đánh dấu (lazy evaluation). Spark chỉ thực hiện các transformation khi có một action gọi đến.

-Các transformation là lazy (trì hoãn), nghĩa là Spark chỉ xây dựng một đồ thị tính toán (DAG) mà không thực sự thực hiện việc tính toán cho đến khi action được kích hoạt.

<img width="888" alt="Ảnh màn hình 2024-09-07 lúc 10 40 59" src="https://github.com/user-attachments/assets/fe40f443-03a7-477d-9ca4-5a991c6c6e4d">

- flatMap(): trả về 0/ 1/ nhiều giá trị cho từng element trong RDD gốc.

***Action***

- Action là thao tác khiến Spark thực sự thực hiện các tính toán trên RDD. Khi một action được gọi, Spark sẽ thực hiện tất cả các transformation trước đó và trả về kết quả hoặc thực hiện một hành động cụ thể như ghi dữ liệu xuống ổ cứng.

- Các Action trong Spark là các hàm trả về kết quả cuối cùng của các tính toán RDD. sử dụng lineage graph để tải dữ liệu lên Nó theo một thứ tự cụ thể. Sau khi tất cả các transformation được thực hiện, action trả về kết quả cuối cùng cho Spark Driver. Action là operation cung cấp non-RDD value.

<img width="733" alt="Ảnh màn hình 2024-09-07 lúc 10 43 40" src="https://github.com/user-attachments/assets/3e9f54b0-e316-4414-9f7c-c3ba4b396027">

<img width="928" alt="Ảnh màn hình 2024-09-10 lúc 19 57 48" src="https://github.com/user-attachments/assets/dc5798da-bdee-4396-8d6d-7de4a3846c94">

- reduce(function): được sử dụng để tổng hợp các phần tử của regular RDD. Function này giao hoán (thay đổi thứ tự của toán hạng không thay đổi kết quả) và kết hợp

- saveAsTextFile("folder_name"): lưu trữ RDD vào trong thư mục folder_name với mỗi partition àl một file riêng lẻ.

**Pair RDDs**
