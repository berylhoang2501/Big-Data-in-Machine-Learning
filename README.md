![Ảnh màn hình 2024-09-05 lúc 18 44 05](https://github.com/user-attachments/assets/6f030cbb-82ca-4839-a254-4f5a35a040c6)

- 20 bài cho 4 điểm

- bài thi 6 câu 

- 4 bài tập cộng điểm, sẽ không có phần giải thích, deadline 2 ngày sau khi giao bài tập + điểm

![Ảnh màn hình 2024-09-05 lúc 18 47 31](https://github.com/user-attachments/assets/db89622c-dd3e-4995-81da-784bc88dbce3)

- Apache spark standalone worker là ndung sẽ học trong buổi offline

- Phải giải quyết bài tập và bài thi bằng môi trường Pyspark và big data, không dc dùng sklearn và machine learning truyển thông

> # Buổi 1: Tổng quan Big Data (05/09/2024)

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

> # Buổi 2: Tổng quan PySpark (07/09/2024)

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

> # Buổi 2: PySpark RDDs (07/09/2024)

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

> # Buổi 3: PySpark RDDs (07/09/2024) (tt)

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

- Các dataset trong thực tế thường đi theo cặp key/value

- Mỗi row là một key ánh xạ đến một hoặc nhiều value

- Pair RDD là một dạng data structure đặc biệt để làm việc với kiểu data dạng này

- Pair RDD: Key là identifier và value là dữ liệu

**Transformation trên pair RDDs**

- reduceByKey(): kết hợp các value cùng key

- sortByKey(): trả về một RDD được sắp xếp theo key

- groupByKey(): nhóm các value có cùng key

- join(): nối RDD dựa trên key của chúng

**Action trên pair RDDs**

- Các action nào dùng dc trên RDDs thì đều dùng đc trên pair RDDs

- CountByKey(): đếm số lượng value cho từng key

- collectAsMap(): trả về key-value pair trong RDD theo định dạng dictionary

> # Buổi 4: PySpark SQL & DataFrame (12/09/2024) 

<img width="938" alt="Ảnh màn hình 2024-09-12 lúc 19 36 37" src="https://github.com/user-attachments/assets/f112d696-8212-428b-b762-e82d502823f9">

## 1. Giới thiệu Spark SQL

- Là một module của Spark, hỗ trợ truy vấn dữ liệu qua SQL và Hive Query Language

<img width="902" alt="Ảnh màn hình 2024-09-12 lúc 19 37 56" src="https://github.com/user-attachments/assets/fc2febd8-efa4-4ee5-89f5-41ea728cca13">

## 2. Giới thiệu Spark DataFrame

**DataFrame**

-  Giống như bảng trong cơ sở dữ liệu, với các cột đại diện cho feature/attribute và mỗi dòng là một đối tượng dữ liệu.

-  So với RDD hơi khó học của Spark, từ Spark 2.0 trở lên, DataFrame được ưa chuộng hơn vì cú pháp gọn gàng và dễ làm việc.

**PySpark DataFrame cũng chia sẻ một số đặc điểm chung với RDD:**

-  Immutable ni nature (bất biến)

-  Lazy Evaluations

-   Distributed

**Ưu điểm của DataFrame**

<img width="833" alt="Ảnh màn hình 2024-09-12 lúc 19 52 54" src="https://github.com/user-attachments/assets/113a8696-0d83-46c0-a0a3-6738c27b17e2">

## 3. Làm việc với PySpark DataFrame

**Các function cơ bản**

<img width="818" alt="Ảnh màn hình 2024-09-12 lúc 20 25 37" src="https://github.com/user-attachments/assets/e88a4061-0e59-4c07-b5c2-3b1804a69032">

**Các function trên cột**

<img width="758" alt="Ảnh màn hình 2024-09-12 lúc 20 39 00" src="https://github.com/user-attachments/assets/6e82ad60-7111-46ca-8239-2936639be8d4">

**Các function thao tác dữ liệu**

<img width="707" alt="Ảnh màn hình 2024-09-12 lúc 20 51 24" src="https://github.com/user-attachments/assets/b32d336e-c3af-4d13-bffe-f61421f23c61">

- withColumn(‘column_name’, function): tạo cột mới

- withColumnRenamed(‘old_name’, ‘new_name’): đổi tên cột

**Các function làm sạch dữ liệu**

<img width="712" alt="Ảnh màn hình 2024-09-12 lúc 21 10 32" src="https://github.com/user-attachments/assets/c110a4fa-5edd-4458-9096-316d9d2888ff">

**Các function lọc dữ liệu**

<img width="424" alt="Ảnh màn hình 2024-09-12 lúc 21 17 28" src="https://github.com/user-attachments/assets/6961eb00-eb17-434e-ae56-ea13481d5b13">

> # Buổi 4: PySpark SQL & DataFrame (14/09/2024) (tt)

**Conditional clause**

- .when(<if condition>, <then x>)

- .otherwise()

**User defined functions - UDFs**

- Là Python method

- Được đóng gói trong pyspark.sql.functions.udf

- Được lưu trữ như variable

- Được gọi như một function Spark thông thường

**Trực quan hóa dữ liệu**

- <Spark_DataFrame_name>.toPandas(): Chuyển PySpark DataFrame thành DataFrame

- Sử dụng các biểu đồ dành cho DataFrame để vẽ như histogram, barchart, ...

**Các function khác**

- na.fill(value): tìm và thay thế giá trị nul

- replace(old_value, new_value, column_name): tìm giá trị và thay thế bằng giá trị mới

- repartition(): phân vùng dữ liệu của RDD

## 4. Làm việc với PySpark SQL

**Thực thi SQL Query**

- createOrReplace Temp View("table_name"): tạo table tạm/view

-  sql(query): thực thi truy vấn

-  Truy vấn có điều kiện với WHERE

- Truy vấn với LIKE

- Truy vấn với SUBSTRING/SUBSTR(column_name, from, length)

- Truy vấn với ORDER BY

- Truy vấn với GROUP BY

## 5. Caching & Parquet

**Caching**

- Làm việc với cache

- <DataFrame_name>.cache() : đưa DataFrame vào cache trước Action

- <DataFrame_name> is_cached : xác định trạng thái của DataFrame

- <DataFrame_name>.unpersist() :bỏ DataFrame ra khỏi cache
  
**Parquet**

> # Buổi 5: Data preprocessing (14/09/2024)

## 1. Data Cleaning

**Xóa các thuộc tính không liên quan**

- <New_DataFrame> = <DataFrame_name>.drop(*[list_column_names])

**Lọc dữ liệu theo text**

<img width="455" alt="Ảnh màn hình 2024-09-14 lúc 10 49 47" src="https://github.com/user-attachments/assets/f7276842-d67e-48e0-af7e-0028add4d3f4">

**Xóa dữ liệu outlier theo phân phối chuẩn**

<img width="860" alt="Ảnh màn hình 2024-09-14 lúc 10 56 25" src="https://github.com/user-attachments/assets/7578ce7a-c6be-4a5b-8e2f-d5b2c4a77026">

**Xóa dữ liệu NA, NULL**

<img width="870" alt="Ảnh màn hình 2024-09-14 lúc 11 12 48" src="https://github.com/user-attachments/assets/cd8c17a3-9f7d-44ef-9452-2bc57f476729">

**Xóa dữ liệu trùng lắp**

- <DataFrame_name>. drop_duplicates()

> # Buổi 6: Data preprocessing (17/09/2024) (tt 1)

**MinMax Scaling**

**Standard Scaling - Standardization (Z-score Normalization)**

**Log Scaling**

**Dữ liệu bị thiếu (Missing Data)**

- isNull(): để kiểm tra dữ liệu thiếu

- heatmap(): để trực quan lượng dữ liệu thiếu của thuộc tính

**Xoá dữ liệu thiếu**

- Giá trị thiếu của thuộc tính rất ít >-xóa dòng

- Giá trị thiếu của thuộc tính nhiều (> tỷ lệ)-> xóa thuộc tính (xóa cột)

**Điền dữ liệu khi bị thiếu**

- Rule Based: giá trị điền dựa trên business logic

- Statistics Based: giá trị điền có thể àl mean, median...

- Model Based: giá trị điền là giá trị dự đoán từ model (sử dụng model để dự đoán dữ liệu)

- fillna(value, subset=None)

## 2. Feature Engineering

**Có thể tạo ra tính năng mới**

- Dựa trên các công thức tính toán (cộng, trừ, nhân, chia, tỷ lệ...)

- Dùng regular expression extract (pyspark.sql .functions.regexp_extract)

**regexp_extract(column_name, regex, group_number)**

**TimeFeature**

**Trích xuất tính năng (Extracting Feature)**

- Trích xuất text thành feature mới

- Cắt chuỗi (splitting) thành feature mới

- Tạo nhiều thuộc tính mới (exploding) cho record

- Pivot

- Join

> # Buổi 7: Data preprocessing (19/09/2024) (tt 2)

**Binarizing, Bucketing & Encoding**

- Binarizing: Là kỹ thuật tạo ra một feature mới từ một feature đang có nhưng dưới dạng nhị phân (0 hoặc 1) theo một ngưỡng cho trước (mặc định: threshold = 0)

- Bucketing: Là kỹ thuật tối ưu hóa phân tách dữ liệu thành các phần để dễ quản ýl hơn (buckets), để phân vùng dữ liệu (data partitioning). Động lực là để tối ưu hóa hiệu suất của truy vấn join query bằng cách tránh xáo trộn (avoiding shuffles) các bảng trong join. Các kết quả của Bucketing ít trao đổi hơn, vì việc xáo trộn có thể không cần thiết - cả hai DataFrame có thể đã được đặt trong cùng một phân vùng (partition).

- StringIndexer

- One hot encoding: là kỹ thuật mã hóa các thuộc tính phân loại dưới dạng một one-hot numeric array.

> # Buổi 7: Spark MLlib (19/09/2024)

<img width="1128" alt="Ảnh màn hình 2024-09-19 lúc 20 03 11" src="https://github.com/user-attachments/assets/e5aa06f1-b097-41e2-a6db-943ec3114efc">

## 1. Giới thiệu Spark MLlib

**Spark MLlib**

- Là một thư viện Machine Learning.

- Là một component phía trên Spark Core để phân tích dữ liệu bằng các thuật toán Machine Learning.

- Hoạt động trên các hệ thống phân tán (distributed system) và có thể mở rộng.

- Giúp thực hiện các công việc classification, clustering, linear regression, và các thuật toán machine-learning khác với Spark MLlib.

**MLlib có 3 chức năng ML**

- Data preparation: Feature extraction, transformation, selection, hashing of categorical features, natural language processing methods

- Machine learning algorithms: Regression, classification, clustering algorithms...

- Utilities: Descriptive statistics, chisquare testing, linear algebra (sparse &dense matrices, vectors), model evaluation methods

**MLlib cung cấp các tool**

- ML Algorithms: classification, regression, clustering &collaborative filtering

- Featurization: feature extraction, transformation, dimensionality
reduction &selection

- Pipelines: constructing, evaluating, tuning ML Pipelines

- Persistence: saving &load algorithms, models & Pipelines

- Utilities: linear algebra, statistics, data handling...

## 2. Spark MLlib algorithms

<img width="762" alt="Ảnh màn hình 2024-09-19 lúc 20 17 06" src="https://github.com/user-attachments/assets/1d15e759-cba1-4003-bb40-7d6e5191ffd2">

**Công việc của các nhóm thư viện**

- milib.classification: hỗ trợ classification, giúp chúng ta phân loại với: binary classification, multiclass classification analysis, ví dụ như Random Forest, Naive Bayes, Decision Tree...

- mllib.clustering: hỗ trợ việc clustering, giúp ta nhóm các subset của các thực thể chúng này với các thực thể khác dựa trên các đặc điểm chung của chúng.

- mllib.regression: hỗ trợ việc tìm ra các mối quan hệ và sự phụ thuộc giữa các variables.

- mllib.linalg: MLlib utilities dùng cho linear algebra.

- mllib.fpm (Frequent pattern matching): hỗ trợ việc khai thác các frequent items, itemsets, subsequences hoặc các substructures khác (thường là một trong những bước đầu tiên để phân tích large-scale dataset).

- mllib.recommendation: Collaborative filtering package thường được sử dụng cho các recommender system. Các kỹ thuật này giúp điền vào các missing entries của một user item association matrix.

## 3. Xây dựng model

**Các bước thực hiện**

- Xác định vấn đề

- Chuẩn bị &chuẩn hóa dữ liệu, xác định inputs, output

- Chuẩn bị train/test dataset

- Xây dựng model với train dataset

- Đánh giá model với test dataset

- Lưu trữ & tải model

- Dự đoán mới

**Chuẩn bị & chuẩn hóa dữ liệu, xác định inputs, output**

> # Buổi 8: PySpark ML - Linear &Logistic Regression, Pipeline (21/09/2024)

## 1. Linear Regression

- Phân tích hồi quy tuyến tính được sử dụng để dự đoán giá trị của một biến dựa trên giá trị của một hay nhiều biến khác.

- Biến muốn dự đoán được gọi là biến phụ thuộc (dependent variable).

- Biển đang sử dụng để dự đoán giá trị của biến khác được gọi là biến độc lập (independent variable).

## 2. Logistic Regression

- Logistic Regression là một thuật toán thuộc nhóm Supervised Learning sử dụng rất hiệu quả cho classification.

- Logistic Regression (còn gọi là Logit Regression) thường được sử dụng để ước tính xác suất mà một mẫu thuộc về một lớp cụ thể (ví dụ: xác suất một khách hàng có mua hàng?)

<img width="665" alt="Ảnh màn hình 2024-09-21 lúc 09 35 28" src="https://github.com/user-attachments/assets/eeb4a274-08e2-4316-a6ef-e413c841ae9d">

**Đánh giá**

- Confusion Matrix

<img width="680" alt="Ảnh màn hình 2024-09-21 lúc 09 36 17" src="https://github.com/user-attachments/assets/8a8c85e4-c900-4c3e-9182-dbc3a2375a73">

> # Buổi 9: PySpark ML - Linear & Logistic Regression, Pipeline (24/09/2024) (tt)

## 3. Pipeline

- Một pipeline mô tả hoặc mô hình hóa quy trình Machine Learning: code, release, thực hiện trích xuất dữ liệu, tạo mô hình huấn luyện và điều chỉnh thuật toán.

- Một pipline là một loạt các thao tác cần thực hiện.

- Chúng ta có thể áp dụng từng thao tác riêng lẻ hoặc có thể áp dụng pipeline

> # Buổi 9: PySpark Mllib – Tree Models (24/09/2024)

## 1 Decision Tree

## 2. RandomForest

<img width="750" alt="Ảnh màn hình 2024-09-24 lúc 20 51 25" src="https://github.com/user-attachments/assets/7e75a074-5f2c-4157-acf7-fb370d96ddde">

> # Buổi 10: PySpark Mllib – Tree Models (26/09/2024) (tt)

## 3. Gradient-BoostedTrees

- Boosting" hỗ trợ cho các mô hình Machine Learning để cải thiện độ chính xác của dự đoán.

- Boosting algorithm (Thuật toán tăng cường) là một trong những thuật toán được sử dụng khá rộng rãi nhằm mục đích tăng cường thuật toán để cải thiện độ chính xác của các mô hình.

<img width="818" alt="Ảnh màn hình 2024-10-01 lúc 00 22 54" src="https://github.com/user-attachments/assets/361a0acb-4711-409b-997c-f809cc9034d7">

> # Buổi 10: PySpark Mllib - Clustering, Recommender System (26/09/2024)

## 1. Clustering K-Means

<img width="807" alt="Ảnh màn hình 2024-10-01 lúc 00 25 47" src="https://github.com/user-attachments/assets/514cd390-d244-481c-9467-e8dd32ace894">

- Cách tính khoảng cách: Euclidean Distance, Manhattan Distance, Cosine Similarity

**Sử dụng kết quả phân cụm**

<img width="727" alt="Ảnh màn hình 2024-10-01 lúc 00 27 31" src="https://github.com/user-attachments/assets/47d1eec2-b228-41ee-b7e1-6d064e2b8dc5">

> # Buổi 11:  PySpark Mllib - Clustering, Recommender System (24/09/2024)

## 2. Recommender System - ALS

**Có hai recommender system phổ biến nhất là Collaborative Filtering (CF) và Content-Based**

<img width="636" alt="Ảnh màn hình 2024-09-28 lúc 08 10 03" src="https://github.com/user-attachments/assets/e385fa69-a223-4e4a-87ae-78c62317021e">

- Collaborative filtering tạo ra các đề xuất dựa trên kiến thức của người dùng về thái độ đối với các item, nó sử dụng kiến thức của số đông ("wisdom of the crowd") để đề xuất các item.

- Content-based recommender system tập trung vào các thuộc tính của item và cung cấp cho người dùng các đề xuất dựa trên sự tương tự giữa chúng.

**Rating: có 2 loại là explicit và implicit**

<img width="1013" alt="Ảnh màn hình 2024-09-28 lúc 08 23 21" src="https://github.com/user-attachments/assets/a22c4a2b-29cc-4f15-98fd-76a816cda238">

## 3. Association rules - FPGrowth

**Association rule learning**

- Là một phương pháp Machine Learning dựa trên trên quy tắc để khám phá mối quan hệ giữa các biến trong cơ sở dữ liệu lớn. Nó dùng để xác định các quy tắc mạnh được phát hiện trong cơ sở dữ liệu bằng cách sử dụng một số thuật toán thú vị.

**FP-growth algorithm (FP: frequent pattern)**

![Ảnh màn hình 2024-10-01 lúc 00 54 08](https://github.com/user-attachments/assets/2a2ff43a-6761-4135-8773-d2b204ff8ab6)


> # Buổi 12:  NLP (01/10/2024)

## 1. Giới thiệu

- Xử lý ngôn ngữ tự nhiên (NLP) là thành phần chính trong nhiều hệ thống khoa học dữ liệu (phải hiểu hoặc suy luận về một văn bản).

- Ví dụ một số ứng dụng: Sentiment analysis, Clustering News Articles (phân cụm tin tức), Suggesting similar books (đề xuất các sách tương tự), Grouping Legal Documents (phân nhóm tài liệu), Analyzing Consumer Feedback (phân tích phản hồi của khách hàng), Spam Email Detection (phát hiện mail rác)

**Một số quy trình NLP cơ bản**

- Compile al documents (Corpus, tổng hợp tât cả tài liệu)

- Featurize the words to numerics (chuyển đổi từ thành số)

- Compare features of documents (so sánh thuộc tính của các tài liệu)

- Spark có rất nhiều công cụ pyspark.ml.feature để hỗ trợ toàn bộ quá trình này và làm cho công việc trở nên dễ dàng hơn, như:

Tokenizer 

StopWordsRemover 

NGram

CountVectorizer

TF-IDF

**Tokenize**

- Hiểu đơn giản, Tokenization là quá trình lấy văn bản (ví dụ như một câu) và chia nó thành các term riêng lẻ (thường là các từ). Một lớp Tokenizer cung cấp chức năng này.

**StopWordsRemover**

- stop word là những từ nên được loại bỏ từ input, bởi vì các từ này xuất hiện thường xuyên và không mang nhiều ý nghĩa. ví dụ như, "is", "at", "which", "on"

**Ngram**

- Tham số n được sử dụng để xác định số lượng term trong mỗi n-gram. Output sẽ bao gồm một chuỗi n-gram trong đó mỗi n-gram được biểu diễn bằng một chuỗi phân tách bằng dấu cách của n từ liên tiếp (n consecutive words).

**CountVectorizer**

- Lớp CountVectorizer và CountVectorizerModel giúp chuyển đổi một bộ sưu tập văn bản thành một vector đếm. Kết quả khi chuyển đổi biến phân loại thành một vector đếm là one-hot encoded vector. Kích thước của vector sẽ bằng với sốloại khác nhau mà chúng ta có.

- Khi không có a-priori dictionary, CountVectorizer có thể được sử dụng như Estimator để trích xuất
từ vựng và tạo ra CountVectorizerModel.

**TF-IDF**

- Để hạn chế những từ phổ biến này từ việc áp đảo mô hình, một hình thức chuẩn hóa có thể được sử dụng. TF-IDF có tác dụng làm giảm giá trị của các từ phổ biển, đồng thời tăng trọng số của các từ không xảy ra trong nhiều tài liệu.

## 2. Các công cụ cho NLP




















