---
layout: post
categories: blog
author: nhs000
tags: 
- aws
title: AWS prepare
date: 2018-09-29
---

# Table of Contents

1.  [Exams review](#exams-review)
    1.  [What you should review](#what-you-should-review)
    2.  [EC2 Exams wrong](#ec2-exams-wrong)
    3.  [Additional exam tips](#additional-exam-tips)
        1.  [Kenesis](#kenesis)
        2.  [EBS vs instance store](#ebs-vs-instance-store)
        3.  [SWF Actors](#swf-actors)
        4.  [Ec2](#ec2)
        5.  [AWS Organization](#aws-organization)
        6.  [VPC Peering](#vpc-peering)
        7.  [Direct connect](#direct-conncet)
        8.  [Security Token SErvice (STS)](#security-token-service-sts)
    4.  [Elastic container service](#elastic-container-service)
    5.  [Review quizlet](#org7378ac3)
2.  [Notes](#notes)
    1.  [IAM - Identiy and Access Management](#iam---identiy-and-access-management)
        1.  [Roles](#roles)
        2.  [Policy](#policy)
    2.  [S3](#s3)
        1.  [Availability](#org25c6786)
        2.  [S3 classes](#orgd9d4756)
        3.  [Charge](#charge)
        4.  [Version controlling](#version-controlling)
        5.  [Replication](#replication)
        6.  [Security and encryption](#security-and-encryption)
    3.  [Cloudfront - CDN](#cloudfront---cdn)
    4.  [Storage gateway](#storage-gateway)
    5.  [EC2](#ec2-1)
        1.  [Options](#options)
        2.  [Instance types](#instance-types)
        3.  [EBS](#ebs)
        4.  [Security groups](#security-groups)
        5.  [Network and security](#network-and-security)
        6.  [ELB - Elastic Load Balancer](#elb---elastic-load-balancer)
        7.  [EC2 instance meta-data](#ec2-instance-meta-data)
        8.  [Bootstrap scrip](#bootstrap-scrip)
        9.  [Auto-scaling](#auto-scaling)
        10. [Elastic File System EFS](#elastic-file-system-efs)
        11. [ENI - Elastic Network Interface](#orgd415acf)
        12. [LAMBDA](#lambda)
    6.  [API gateway](#api-gateway)
    7.  [Lamda](#lamda)
    8.  [Route 53](#route-53)
        1.  [DNS](#dns)
        2.  [Routing policies](#routing-policies)
    9.  [Database 101](#org81268b0)
        1.  [Exam tips](#orgcbf085e)
        2.  [Notes](#orga4df95f)
        3.  [Multi-AZ Read replicas](#org3b34c63)
        4.  [DynamoDB](#org2ac98e2)
        5.  [Redshift](#org30d50e3)
        6.  [ElasticCache](#orgabcf9cd)
    10. [VPC](#vpc)
    11. [SQS](#sqs)
    12. [SWF](#swf)
    13. [Elastic transcode](#elastic-transcode)
    14. [Kinesis](#kinesis)
        1.  [Kinesis stream](#kinesis-stream)
        2.  [Kinesis Firehose](#kinesis-firehose)
        3.  [Kinesis Analytics](#kinesis-analytics)
    15. [SNS](#sns)
        1.  [Subcribers:](#subcribers)
    16. [Well-architected](#well-architected)
        1.  [Security](#security)
        2.  [Reliability](#reliability)
        3.  [Perfomance effective](#perfomance-effective)
        4.  [Cost optimization](#cost-optimization)
    17. [ElasticSearch](#org3230a15)
        1.  [NRT: Gần Realtime, 1 document có thể được indexed và searchable trong vòng 1s](#org0aa5d1f)
        2.  [Cluster: 1 tập hợp các node](#org5895bec)
        3.  [Node: 1 phần của cluster](#org839af9c)
        4.  [Index:](#orgd17a604)
        5.  [Document:](#orgee8e66c)
        6.  [Shards, Replicas:](#org4f4db18)
    18. [WAF - Web Application Firewall](#orgcc06046)
    19. [復習](#org7d171bc)
        1.  [Exam feedbacks](#orgef32300)
        2.  [Well-architected framework](#orga87e067)
        3.  [Redshift <code>[5/6]</code>](#orgc5f5734)
        4.  [EBS Storage <code>[4/4]</code>](#org5f34a8d)
        5.  [S3 <code>[5/6]</code>](#org1fe8924)
        6.  [Storage Gateway <code>[3/3]</code>](#orgd5f9157)
        7.  [VPCS/ Subnets / Peering <code>[6/6]</code>](#org5b9e453)
        8.  [EC2 classes <code>[5/5]</code>](#org0cae2da)
        9.  [RDS <code>[4/6]</code>](#orgcb72676)
        10. [Setting up 3, 2, 1 Tier web application <code>[0/3]</code>](#org89e4daa)
        11. [ECS - Elastic Container Servicer AWS Beanstalk <code>[3/4]</code>](#orgcdea899)
        12. [Hybrid Architecture:](#orgafa0f68)
        13. [LAMBDA, APi gateway <code>[2/2]</code>](#org94116af)
        14. [AWS Config](#org95917f9)
        15. [NGINX apps](#org5481c52)
        16. [AWS Cognito](#org65e7014)
        17. [AWS Practice exams](#org9df6f68)


<a id="exams-review"></a>

# Exams review


<a id="what-you-should-review"></a>

## What you should review

-   When trying to grant an amazon account access to S3 using access
    control lists what method of identification should you use to
    identify that account with?
    -   The email address of the account or the canonical user ID
-   Which of the following is not supported by AWS Import/Export?
-   You work for a market analysis firm who are designing a new
    environment. They will ingest large amounts of market data via
    Kinesis and then analyse this data using Elastic Map Reduce. The data
    is then imported in to a high performance NoSQL Cassandra database
    which will run on EC2 and then be accessed by traders from around the
    world. The database volume itself will sit on 2 EBS volumes that will
    be grouped into a RAID 0 volume. They are expecting very high demand
    during peak times, with an IOPS performance level of approximately
    15,000. Which EBS volume should you recommend?
-   Which of the following is not a valid configuration type for AWS
    Storage gateway.
-   Which of the following is NOT a valid SNS subscribers?


<a id="ec2-exams-wrong"></a>

## EC2 Exams wrong

1.  Placement group can be in mutiple AZs?
    -   Wrong

2.  Can delete a snapshot which is root volume of an AMI?
    -   No

3.  In a default VPC, all AWS EC2 instances are assigned 2 IP addresses
    at launch are: Private IP address and public IP Address.
4.  If a instance is provisioned in a public security group, it's not
    automatic pulic to internet


<a id="additional-exam-tips"></a>

## Additional exam tips


<a id="kenesis"></a>

### Kenesis

-   Used to consume big data
-   Stream large amounts of social media
-   Process large amounts of data:
-   Redshift for business intelligence


<a id="ebs-vs-instance-store"></a>

### EBS vs instance store

-   EBS are persistent
-   EBS can be detached and reattached to other EC2 instances
-   Instance store are not persistent, lost data when stop EC2 instance
-   Cannot be detached and reattached, they exist only for the life of
    that instance


<a id="swf-actors"></a>

### SWF Actors

-   Workflow starters:
-   Deciders
-   Activity workers


<a id="ec2"></a>

### Ec2

-   Ec2 meta query:
-   curl <http://169.254.169.254/latest/meta-data>
-   wget <http://169.254.169.254/latest/meta-data>


<a id="aws-organization"></a>

### AWS Organization

-   Root account -> OU account (AWS Account)
-   Paying
-   Test/Dev account
-   Production account
-   ..
-   Price is lower: Bằng cách tổng tất cả các chi phí vào 1 tài khoản ->
    được giảm giá


<a id="vpc-peering"></a>

### VPC Peering

-   Nối các vpc với nhau
-   Có thể nối các vpc ở các AWS account khác nhau nhưng cùng 1 region
-   Không có tính bắc cau
-   Không thể peer nếu các VPC trùng internal block ip


<a id="direct-conncet"></a>

### Direct connect

-   Kết nối your intranet và Amazon VPC


<a id="security-token-service-sts"></a>

### Security Token SErvice (STS)

-   Grant users limited and temporary acces to AWS resources. Users can
    come from three sources


<a id="elastic-container-service"></a>

## Elastic container service

-   ECS: Allows you to manage docker containers on a cluster of ec2
    instances
-   Images are stored in a Registry, such as DockerHub or AWS ECR (Amazon
    EC2 Container Registry)
-   A Task definition is required to run Docker containers in Amazon ECS
-   are text files in JSON format that describe one or more containers
    that form your application
-   Nhu la 1 cloud formation template but for docker, configure things
    such as the amount of CPU, RAM etc
-   Allows you tu run and maintain a specified number of instances of a
    task definition simultaneously in an ECS cluster
-   ECS cluster is a logical grouping of container instances that you can
    place tasks on
-   Cluster can contain multiple different container instance types
-   Are region-specific
-   Container instances can only be part of one cluster at a time
-   Can create IAM policies for your clusters to allow or restitrct
    users'access to specific clusters


<a id="org7378ac3"></a>

## Review quizlet

-   TODO


<a id="notes"></a>

# Notes


<a id="iam---identiy-and-access-management"></a>

## IAM - Identiy and Access Management

-   Setup áp dụng cho toàn bộ region
-   root account = accout khi đăng nhập bằng email.
    -   Có mọi quyền thực thi mọi thứ trên aws
    -   Administration Access
-   Power user có mọi quyền truy cập vào các resource của aws nhưng ko
    thể thay đổi user và group trong IAM.
    -   Power user permission
-   Default secret key only showed once when finishing creating a new
    user.
    -   Can create new access-secret key.
-   Có thể thêm permission cho user bằng cách add user vào 1 group hoặc
    thêm trực tiếp permission mà ko cần thông qua group.
-   1 user can be member of maximum 10 groups


<a id="roles"></a>

### Roles

    IAM roles are a secure way to grant permissions to entities that you trust. Examples of entities include the following:
    
    IAM user in another account
    Application code running on an EC2 instance that needs to perform actions on AWS resources
    An AWS service that needs to act on resources in your account to provide its features
    Users from a corporate directory who use identity federation with SAMLflymd

-   Ví dụ tạo role cho EC2 có thể call các service khác như Lambda, S3
    -   Roles -> Create role -> EC2 -> Select use case -> Choose permission
        policy
-   Khi gán role cho ec2 instance thì instance đấy có thể kết nối đến aws
    mà không cần phải configure credential.
-   Được tạo trong IMA và là global cho mọi regions.
-   Gán cho EC2 instance một role thì có thể tự động truy cập lệnh aws ở
    trong instance đó mà không phải lưu key, secret
-   Có thể thay đổi role của một instance kể cả sau khi đã launched sử
    dụng console hoặc command
-   Role là global


<a id="policy"></a>

### Policy

-   Is a document that provides a formal statement of one or more
    permissions.


<a id="s3"></a>

## S3

-   Object storage vs block storage (EC2)
    -   Key - value storage
        -   Key ( object name)
        -   Value (sequence of bytes)
        -   Version ID (Important for versioning)
        -   Metadata (created date, updated date &#x2026;)

-   File is 0 - 5TB and storaged in bucket (aka folder)
-   Unlimited storage
-   When write object (PUT new objects) then you can read it immediately
    but when update or delete (PUT or DELETE) object it takes time to
    update.
-   Link: <https://{bucket-name}.s3-website-{region\_code}.amazonaws.com>


<a id="org25c6786"></a>

### Availability

-   Standard: 99.9{9} 
    -   99.99% over a given year
-   S3 with RRS the AVAILABILITY is 99.99%


<a id="orgd9d4756"></a>

### S3 classes

-   Setting trong phần properties của object
-   S3 - IA: 
    -   For data that is accessed less frequently but requires rapid access when needed.
-   RRS
    -   Reduced Redundancy Storage: dùng để lưu trữ các data có thể generate ra được ? ( Ví dụ thumbnail của ảnh &#x2026;)
-   Glacier: 
    -   Dùng để lưu archieved datas, mấy vài tiếng đến vài ngày để lấy được data.


<a id="charge"></a>

### Charge

-   Storage
-   Number of requests
-   Storage management pricing ( phí quản lý các loại data theo tag &#x2026;)
-   Data transfer pricing

1.  S3 transfer acceleration

    -   Sử dụng các server cloudfront phân tán để tăng tốc tộ upload file của
        người dùng.


<a id="version-controlling"></a>

### Version controlling

-   Store all versions of objects
-   Can't be disabled, only suspended
-   Can use MFA mutil-factor authentication when deleting.


<a id="replication"></a>

### Replication

-   Version control must be enabled in both buckets
-   Only new or changed files is copied.
-   Permission not copied


<a id="security-and-encryption"></a>

### Security and encryption

1.  Bucket policy

    Policy cho toàn bộ object trong bucket

2.  Access Control List ACL

    -   Policy cho từng object riêng biệt trong bucket hoặc cho cả bucket

3.  Encryption

    1.  In transit
    
    2.  Mã hoá trong khi truyền dữ liệu sử dụng ssl/tls
    
    3.  At rest
    4.  Server side
        -   SSE-S3
        -   SSE-KMS
        -   SSE-C
    
    5.  Client side You encrypt your files and upload to S3.


<a id="cloudfront---cdn"></a>

## Cloudfront - CDN

Cache dữ liệu tại 50 edge location trên thế giới giúp giảm độ trễ.


<a id="storage-gateway"></a>

## Storage gateway

-   Valid configuration type:
    -   Gateway-cached volumes
    -   gateway-stored volumes
    -   Gateway-virtual tape library


<a id="ec2-1"></a>

## EC2


<a id="options"></a>

### Options

-   On Demand: trả tiền theo từng giờ ( windows instance) hoặc từng giây
    ( linux instance)
    -   Tự scale vào 1 khoảng thời gian nhất định
-   Reserverd: Đặt trước với capacity reservation, bằng cách ký hợp đồng
    1 hoặc 3 năm.
    -   Giảm giá cho từng giờ sử dụng.
-   Spot: Cho phép chọn giá mà bạn muốn cho instance capacity -> giúp tiết kiệm
    -   Ví dụ một bệnh viện có nhiều dữ liệu nhưng muốn giảm cost và cho thống kê chạy trong khoảng 0am-4am => Đấu giá
    -   Nếu tự terminate EC2 thì sẽ phải trả luôn cả giờ làm tròn (2h30 thì coi như đến 3h)
    -   Nhưng nếu EC2 bị terminate do giá cao hơn giá bid thì sẽ chỉ phải trả 2h 
        -   Spot nghĩa là tập trung 1 điểm nào đó nếu như ứng dụng của bạn có flexible start and end times.
-   Dedicated hosted: host được tạo ra để dùng riêng cho bạn.
    -   Sử dụng các liencse có sẵn
    -   Sử dụng các server có sắn
-   Different types of virtualization available on EC2
    -   Para-Virtual (PV) and Hardware Virtual Machine (HVM)


<a id="instance-types"></a>

### Instance types

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<thead>
<tr>
<th scope="col" class="org-left">Family</th>
<th scope="col" class="org-left">Speciality</th>
<th scope="col" class="org-left">Usecase</th>
</tr>
</thead>

<tbody>
<tr>
<td class="org-left">D2</td>
<td class="org-left">Dense Storage</td>
<td class="org-left">FileServer, DataWareHouse, Hadoop</td>
</tr>


<tr>
<td class="org-left">R4</td>
<td class="org-left">Memory Optimized</td>
<td class="org-left">Memory Extensive Apps</td>
</tr>


<tr>
<td class="org-left">M4</td>
<td class="org-left">General purpose</td>
<td class="org-left">Application Server</td>
</tr>


<tr>
<td class="org-left">C4</td>
<td class="org-left">Computed Optimized</td>
<td class="org-left">Cpu extensive app</td>
</tr>


<tr>
<td class="org-left">G2</td>
<td class="org-left">Graphics Intensive</td>
<td class="org-left">Video encoding, 3d Application streaming</td>
</tr>


<tr>
<td class="org-left">I2</td>
<td class="org-left">High speed storage</td>
<td class="org-left">NoSQL DB, Datawarehouse</td>
</tr>


<tr>
<td class="org-left">F1</td>
<td class="org-left">Field programable gate array</td>
<td class="org-left">Hardware acceleration for your code</td>
</tr>


<tr>
<td class="org-left">T2</td>
<td class="org-left">Low cose, general purpose</td>
<td class="org-left">Webserver, small DBs</td>
</tr>


<tr>
<td class="org-left">P2</td>
<td class="org-left">Graphic, general purpose GPUs</td>
<td class="org-left">Machine learning, bitcoin mining</td>
</tr>


<tr>
<td class="org-left">X1</td>
<td class="org-left">Memory optimized</td>
<td class="org-left">Apache SPARK&#x2026;</td>
</tr>
</tbody>
</table>

> DR MC GIFT PX


<a id="ebs"></a>

### EBS

-   GP2: General Purpose SSD
    -   IOPS: 3 -> 10000, burst up to 3000
-   Provisioned IOPS SSD
    -   Sử dụng cho các ứng dụng sử dụng nhiều IO như large relational database or NoSQL database
    -   IOPS: > 10000
-   Throughtput Optimized HDD (ST1)
    -   Big data, data warehouse, log volumn &#x2026;
    -   Can't use as boot volumn
-   Cold HDD
    -   Sử dụng cho các workload thỉnh thoảng mới được sử dụng
    -   File server
    -   Can't use as boot volumn
-   Magnetic
    -   Volumn giá rẻ nhất mà có thể boot được
    -   Sử dụng cho workload thỉnh thoảng được sử dụng
    -   Một khi đã tạo thì không thay đổi được volumn
-   Không thể encrypt boot volumn của các AMI default nhưng có thể
    encrypt cho các AMI mà mình tạo ra .
-   You can't mount 1 EBS volume to multiple EC2 instances, instead use
    EFS
-   Default thì EBS sẽ bị deleted khi Ec2 instance của nó bị terminated
    nhưng có thể lựa chọn để giữ lại được.
    -   Turn off flag deleteOnTemination

1.  Thực hành, snapshot

    -   Muốn thay đổi AZ của volumn thì phải tạo snapshot -> tạo volumn mới
        từ snapshot và thay đổi AZ của volumn này.
    -   Snapshot is stored in S3.
        -   Phải stop instance thì mới tạo được snapshot
        -   Chụp snapshot từ lần thứ 2 sẽ nhanh hơn lần đầu do chỉ các phần thay
            đổi mới được copy.
        -   Tự động encrypt volume
        -   Có thể share các unencrypted snapshot cho các tài khoản AWS khác hoặc
            đăng public.
    -   Muốn tạo snapshot cho các ổ đãi RAID thì trước hết phải ngừng tất cả
        các thao tác IO rồi sau đó flush cache và terminate instace rồi mới
        tạo snapshot.

2.  Root volumne : EBS vs instance store

    -   Instance store - Ephemeral Storage : không thể bị stop. Một khi nó bị
        stop do underlying system (aws system) thì nó sẽ bị mất hết dữ liệu.
    -   EBS có thể stop mà không mất dữ liệu.
    -   Cả 2 đều có thể reboot mà ko mất dữ liệu.
    -   Thông thường cả 2 sẽ mất dữ liệu khi bị terminated nhưng EBS cho phép
        lựa chọn giữ lại dữ liệu trong root volume.
    -   EBS volume được tạo ra từ EBS snapshot
    -   Instance volume được tạo ra từ template stored trong S3


<a id="security-groups"></a>

### Security groups

-   Có thể add security groups vào 1 ec2 instance.
-   Stateful: Khi bạn add 1 inbound rule thì nó sẽ tự động add outbound
    rule tương ứng
-   Có thể cài đặt các allow rule nhưng không thể tạo ra các deny rule
    -   Sử dụng network access list trong VPC
-   Mỗi Security group chỉ tồn tại trong 1 region? // Cần confirm


<a id="network-and-security"></a>

### Network and security

1.  Key pairs

    -   Hiển thị các key pair ssh


<a id="elb---elastic-load-balancer"></a>

### ELB - Elastic Load Balancer

-   Phải để security group cho các node open thì load balancer mới
    checkhealth đượckj.

1.  Application Load Balancer

    -   LB ở tầng thứ 7, Application Layer.
    -   Mới xuất hiện
    -   Hiệu quả tốt hơn Classic Load Balancer
    -   Có thể thêm target group để chỉ định protocol và port mà muốn tạo
        load balancing

2.  Classic load balancer

    -   Hoặc động ở tầng thứ 4, TCP Layer
    -   Load balancer protocol: Là giao thức để chuyển balancing cho các node


<a id="ec2-instance-meta-data"></a>

### EC2 instance meta-data

-   SSH vào instance và curl đến đia chỉ
    `http://196.254.196.254/latest/meta-data/` để lấy meta của instance .


<a id="bootstrap-scrip"></a>

### Bootstrap scrip

-   Khi launch 1 instace
-   Configure detail -> Advanced detail -> User data -> paste bootstrap
    scrip into here.


<a id="auto-scaling"></a>

### Auto-scaling

-   Create auto-scaling group
    -   Tạo autoscaling group template: là template của các instance được tạo
        thêm để scaling
        -   Nhấn vào sẽ đi đến chỗ cấu hình 1 ec2 instance giống với khi
            launch 1 instance
    
    -   Group size: số instance được tạo ra ban đầu
    -   Subnet: các AZ được sử dụng để tạo các instace khi auto-scaling
    -   Load balancer: Thêm các instace được tạo ra để scaling vào 1 nhóm
        load balancer
-   Auto-scaling policy
    -   Khi nào thì thêm instance


<a id="elastic-file-system-efs"></a>

### Elastic File System EFS

-   Is a file storage service for EC2.
-   Tự tăng giảm kích thước khi thêm hoặc xoá files.
-   Data được lưu cross trong các AZ của 1 region.
-   Block base storage ( S3: object base storage)
    
        Giúp việc lưu giữ file ( thuường là server file) được tập trung lại 1 nơi

-   EFS : nhiều instances cso thể mount vào 1 EFS. EBS: chỉ 1 instance có
    thể mount vào 1 EBS


<a id="orgd415acf"></a>

### ENI - Elastic Network Interface

-   is a logical networking component in a VPC that represents a virtual network card.


<a id="lambda"></a>

### LAMBDA

-   Là nơi bạn upload code và AWS sẽ lo tất cả về phần server. Chỉ cần
    tạo event trigger.
-   Phù hợp cho các service event-driven
-   Xử lí các response từ API gateway hoặc các api call từ AWS SDKs.
-   LAMBDA có thể trigger các lambda khác hoặc các service khác của AWS
    SDKs.
-   **Mỗi 1 xử lý cho 1 event là 1 instance của LAMDA. Các instances của
    lambda có thể ở các AZ hoàn toàn khác nhau.**
-   Tự scale -> không cần quan tâm về Elastic Load Balancer &#x2026;

1.  Thực hành

    -   From scratch:
    -   Runtime: C#, Python, Java, Go, Nodejs
    -   Một function không thể có thời gian xử lý quá 5p. Nếu quá phải break
        ra thành nhiều function và cho chúng gọi lẫn nhau.
    -   Sử dụng AWS-XRay để debug Lambda


<a id="api-gateway"></a>

## API gateway

-   Enable CORS on method/resource ??
    -   Mục đích là gì?
-   API key and usage plans??
-   Phải config endpoint cho phía client trùng với endpoint của API
    gateway


<a id="lamda"></a>

## Lamda

-   Change lambda role to role containing "cdaLambdaRole"
-   Execution role?
-   Ensure Lambda can post to DynamoDB
-   Configure SQS for anyone to post to queue


<a id="route-53"></a>

## Route 53

-   By default, Amazon DNS khong response lai cac request tu ben ngoai
    VPC


<a id="dns"></a>

### DNS

1.  Exam notes

    -   ELB do not have pre-defined IPv4 address, you resolve to them using a
        DNS Name

2.  Concepts

    -   Top level domains: The last word in a domain name.
        -   Ex: .com, .edu, .gov&#x2026;
    -   The second level domain name: The the second word in domain name
        -   Ex: .co (.co.uk), .gov (.gov.uk)
    -   The top level domain names are controlled by IANA (Internet Assigned
        Numbers Authority) in a root zone database which consitent all
        available top domain names.
        -   <http://www.iana.org/domains/root/db>
    -   Domain registrars
        -   A registra is an authority that can assign domain names under one or
            more top-level domain names.
        -   Each domain is registered in a central database called WhoIS
            database.
    -   SOA Records
    -   NS Records
    -   A Record: Used by computer to translate the name of the domain to the
        IP address.
    -   TTL: Time to Live
        -   The length that a DNS Record is cached in Resolving Server or users
            own local PC
        -   When you go to a website, your PC is going to check whether or not it
            has that address in cache. If not it is going to the DNS resolving
            server.
    -   CNAMES: A Conanical Name
        -   Map a domain to another domain name.
        -   CNAME can't be used for naked domain names (domain that doesn't have
            'www'), it must be an A record or an alias.
    -   Alias records:
    -   Work like a CNAME record in that you can map one DNS name to another
        'target' DNS name.


<a id="routing-policies"></a>

### Routing policies

1.  Simple
2.  Weighted
3.  Latency
4.  Failover
5.  Geolocation


<a id="org81268b0"></a>

## Database 101


<a id="orgcbf085e"></a>

### Exam tips

-   Get free storage AP: getStorageSpace


<a id="orga4df95f"></a>

### Notes

-   RDS - Online transaction processing - OLTP
    -   SQL
    -   Mysql
    -   PostgreSQL
    -   Oracle
    -   Aurora
        -   6 copies of my date are stored by default.
    -   MariaDB
    -   Maximum backup retention period: 35days.
    -   Automated backups are enabled by default for a new DB instance.
    -   RDS does not currently support increasing storage on a SQL Servce DB
        instance.
    -   in RDS, changes to the backup window take effect immediately
-   DynamoDB - NoSQL
    -   Can not select a specific AZ in which to plce your DynamoDB table
-   Redshift - OLAP - Online analysis processing
    -   Copy production DB and run analysis queries in copied DB so it doesn't harm the production DB.
    -   The combined Value, Name must not exceed 400KB


<a id="org3b34c63"></a>

### Multi-AZ Read replicas

Two types of backups: Automated backup, Database Snapshots

-   Automated backup
    -   Enabled by default
    -   Stored in S3, you get free storage space equal to the size of the DB
    -   Deleted when RDS is deleted
-   Snapshot - Stored even after original RDS instances is deleted.
-   Restored version of RDS will be a new RDS instance with new DNS endpoint.
-   Multi-AZ
    -   Disaster Recovery only.
    -   Have a extracy copy of your production DB in another AZ.
    -   AWS handles the replication for you so when your DB is written to this write
        will automatically be synchronized to the stand by database.
-   Replicas
    -   Improve performance.
    -   Allow you to have a read-only copy of production DB.
    -   Use read replicas primarily for very read-heavy database workloads.
    -   Maximum 5 replicas
    -   Cloudwatch should watch getReplicaLag


<a id="org2ac98e2"></a>

### DynamoDB


<a id="org30d50e3"></a>

### Redshift

-   ppppppppDatawarehouse
-   Columnar storage
-   Advanced compression
-   MPP: Massively parallel processing: automatically distributes datas and
    query across all nodes.
-   Charge:
    -   Compute node hours
    -   Backup
    -   Data transfer
-   Currently only avaiable in 1 AZ
-   Can restore to new AZ
-   Block size for its columnar storage: 1024KB / 1MB


<a id="orgabcf9cd"></a>

### ElasticCache

-   Webservice makes it easy to deploy, operate, slace in in-memory cache in the
    cloud.
    -   Support two open-source in-memory caching engines:
        -   Memcached
            -   Memory object caching system.
        -   Redis
            -   Opensource in-memory key-value store that supports datastructure such as
                sorted sets and lists.


<a id="vpc"></a>

## VPC

-   Each regions -> max 5 VPCs
-   Automatically created:
    -   Route table
    -   Network ALC (Access control list)
        -   Stateless
            -   Inbound rule va outbound rules rieng biet
    -   Security group
        -   All outbound traffic is allowed by default
-   Network address translation (NAT)
    -   NAT instance
        -   Disable source/destination check
        -   Must be in public subnet
        -   Route out of the private subnet to NAT instance
        -   Traffic depends on NAT instance size.
        -   Associate with security group
        -   Have to disable Source/Destination Checks
    -   NAT gateway
        -   Auto scale to 10Gps
        -   Not associate with security group
        -   Automatic assigned public IP
        -   More secure than NAT instance
-   Network ACL
    -   Can associate ACl with multiple subnets
    -   If don't, subnet automatically associated with default ACL
    -   A subnet can associate with one ACL, one ACL can associated with multiple
        subnets.
    -   Contains number of rules in order and evaluated starting from lowest value.


<a id="sqs"></a>

## SQS

-   Pull based system
-   Messages size is 256KB
-   Messages kept in queue 1 minute to 14 days
    -   Default is 4 days
-   Visibily time out is the amount of time after the reader picks up the
    message.
    -   Max is 12 hours
    -   If the message is processed by provided job then the message will be
        deleted.
    -   If not, the message is visible again and another process will process
        it
        -   This results the same message being delivery twice

-   SQS is pull based, not push based.
-   Messages are 256kB size
-   Messages can be kept in queue from 1 minut to 14 days. Default is 4
    days.
-   Visibility Time out is the amount of time that the message is
    invisible in SQS queue after a reader picks up the message. If the
    reader processed before the the visibility time out expires, the
    message wil be deleted. If not, the message will be came visibility
    again and another process will process it. This could result the same
    message is processed twice.
-   SQS ensures that a message will be processed at least once.
-   Long polling:
    -   Not return a response if the message queue being polled is empty
    -   Return a response when a message arrives in the message queue. Or the
        long poll times out.
-   Can't be FIFO.


<a id="swf"></a>

## SWF

-   Task oriented queue
-   Ensure task is assigned only once and is never duplicated.
-   Workflow starters: Start a workflow.
-   Deciders: Control flow of activity task in workflow execution.
    -   If something has finished in workflow or failed, Deciders decides
        what to do next.

-   Acitivity workers: Carry out the activity tasks.


<a id="elastic-transcode"></a>

## Elastic transcode

-   Jobs, pipelines, presets, notifications
-   Convert file type


<a id="kinesis"></a>

## Kinesis

Is a platform in AWS allow you to send streaming data. Make it easy to
load and analyze data.


<a id="kinesis-stream"></a>

### Kinesis stream

-   (PC, SP, Ec2)
-   -> (Kinesis Stream): Store data in shards for 24 by default and can
    be set to max 7 days
-   -> (Ec2): Consumers: Take the data and turn it to somthing useful.


<a id="kinesis-firehose"></a>

### Kinesis Firehose

-   (PC, SP, Ec2)
-   -> (Kinesis Firehose):
    -   Don't worry about manually adding shard.
    -   Use lambda to analyze data in realtime.
    -   After analyzing you can send it to S3.

-   -> S3 / Redshift, ElasticSearch


<a id="kinesis-analytics"></a>

### Kinesis Analytics

-   Allow you to run sequel queries then store into S3, Redshift,
    ElasticSearch cluster.


<a id="sns"></a>

## SNS


<a id="subcribers"></a>

### Subcribers:

-   HTTP
-   HTTPS
-   Email
-   Email-JSON
-   SQS
-   Application
-   Lambda


<a id="well-architected"></a>

## Well-architected

1.  General design principles

2.  Stop guessing your capacity needs.
3.  Cloud scales automatically
4.  Testing systems at production scale
5.  Automate make architectual experimentation easier
6.  Allow for evolutionary architectures
7.  Data-driven architectures


<a id="security"></a>

### Security

-   Apply security at all levels
-   Subnet, Access control list (ACL), &#x2026;
-   Enable traceability
-   Automatet responses to security events
-   Automate security best practices

1.  Data protection


<a id="reliability"></a>

### Reliability

-   Realiability in the cloud consists of 3 aresas:
-   Foundations
    -   How are you managing AWS service limits for your account?
    -   How are you planning your network topology on AWS

-   Change management
    -   How to adapt to changes in demand
    -   How to monitor AWS resource
    -   How to execute change management

-   Failure management
    -   How to backup data
    -   How to plan recovery


<a id="perfomance-effective"></a>

### Perfomance effective

-   Use server-less architectures


<a id="cost-optimization"></a>

### Cost optimization

-   Matched supply and demand
-   Autoscaling
-   Cost-effective resources
-   EC2 (reserved instanced - can moved to another region), AWS Trsuted
    Advisor
-   Expenditure awareness
-   Cloudwatch alamrs, SNS
-   Optimizing over time
-   AWS Blog, AWS Trusted Advisor


<a id="org3230a15"></a>

## ElasticSearch


<a id="org0aa5d1f"></a>

### NRT: Gần Realtime, 1 document có thể được indexed và searchable trong vòng 1s


<a id="org5895bec"></a>

### Cluster: 1 tập hợp các node


<a id="org839af9c"></a>

### Node: 1 phần của cluster

-   Lưu trữ data
-   Tham gia vào quá trình index, search của cluster
-   Join vào cluster bằng naming convention?
-   1 cluster có thể có bn node tùy ý


<a id="orgd17a604"></a>

### Index:

-   1 collection của các document có thuộc tính tương tự nhau
-   Có thể chứa vô hạn documents


<a id="orgee8e66c"></a>

### Document:

-   Đơn vị chưa thông tin có thể indexed được
-   Lưu dưỡi dạng json


<a id="org4f4db18"></a>

### Shards, Replicas:

-   Chia index ra các shards bởi vì nếu để vào 1 node thì kích thước index quá lớn hoặc mất quá nhiều tg đế lấy data cho 1 request
-   1 shard là 1 đơn vị độc lập, full chức năng, và có thể được hosted ở any node
-   Giúp tăng khả năng horizontally split or scale, parallelize operations across shards
-   Replicas shards i.e Replicas là bản copy của shard để có thể fail over và parallelize


<a id="orgcc06046"></a>

## WAF - Web Application Firewall


<a id="org7d171bc"></a>

## 復習


<a id="orgef32300"></a>

### Exam feedbacks

<https://acloud.guru/forums/aws-certified-solutions-architect-associate/discussion/-L7uITWGWEI21g2BXL1_/Exam%20Feedback%20-%20SAA%20February%202018%20Edition>
I also went through all recommended whitepapers and FAQs (EC2, S3, VPC, Route 53, RDS, SQS) at <https://aws.amazon.com/certification/certification-prep>, 


<a id="orga87e067"></a>

### TODO Well-architected framework

1.  Whitepaper presented in the Exam Blue Print
2.  Most cost-optimized
3.  Highly available system
4.  Security, cost


<a id="orgc5f5734"></a>

### DONE Redshift <code>[5/6]</code>

1.  Surprising number of questions in this area
2.  [X] Perform encryption
    1.  Encryption property is immutable
    2.  Setting when launching
    3.  Changing have to unload data and reload with encryption setting
    4.  Use AWS KMS or hardware security module to encrypt
3.  [X] Cross-region backups/replication
    1.  Config to copy snapshot(automatic / manual) to another region.
    2.  Automatic snapshot is deleted when reached the retention time period (can change and separate from source region - default 7 days)
        1.  Deleted when disable automatic snapshot copy
    3.  Manual snapshot can only by manually deleted.
    4.  Change destination: disable snapshot copy -> re-enable and change destination region
    5.  Transfer charges
4.  [X] Disaster recovery of a cluster
5.  [X] Review Redshift FAQs
    1.
6.  [ ] Try setup a cluster
7.  [X] Security
    1.  [X] Security group


<a id="org5f34a8d"></a>

### DONE EBS Storage <code>[4/4]</code>

1.  [X] Different storage solution (S3, EBS, EFS, EBS-Provisioned IOPS, ..)
    1.  How to implement and change theme
    2.  Genral purpose
    3.  Provisioned SSD
    4.  Throughput optimized HDD
    5.  Cold HDD
2.  [X] Choosing the optimum (performance + cost) EBS storage solution
3.  [X] EBS vs storage gateway vs S3 vs RDS vs EFS
    1.  Read EFS FAQs
    2.  AWS Storage Gateway connects on premise storage to the S3 repository.
    3.  You can mount EFS onto several EC2 instances at the same time.
4.  [X] Read FAQs


<a id="org1fe8924"></a>

### DONE S3 <code>[5/6]</code>

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-26 Wed 00:04]</span></span>
-   [X] Connect cloudfront
    1.  Create distribution
    2.  Add s3 bucket as Origin Domain Name
-   [X] Connect VPC enpoints
-   [X] Hashing prefix for performance
-   [X] Lifecycle policies, tiers of storage?
-   [X] Read FAQs
    1.  Storage types: s3 - standard, s3 IA, s3 rrs, s3 one-zone is, glacier
    2.  Price:
        1.  Transfer : Same region -> no cost, otherwise charged
        2.  Versioning: all version is summed up
        3.  Access control: IAM policy, bucket policy, ACL, Query String Authencation
        4.  Standard IA :
            1.  deleted from S3 Standard-IA within 30 days will be charged for a full 30 days.
            2.  has a minimum object storage charge of 128KB. Objects smaller than 128KB in size will incur storage charges as if the object were 128KB.
            3.  Glacier APIs to access objects that I’ve archived to Amazon Glacier? - Only accessible through the Amazon S3 APIs or the Amazon S3 Management Console.
        5.  Query in place
            1.  S3 select
            2.  Amazon Athena
            3.  Redshift spectrum
        6.  s3 noti
            1.  no cost
        7.  s3 transfer acceleration
        8.  Object tag
        9.  Lifecycle
            1.  No cost
        10. Cross-region replication
-   [ ] Do labs


<a id="orgd5f9157"></a>

### DONE Storage Gateway <code>[3/3]</code>

1.  DONE File gateway: using industry-standard file protocols

    -   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-26 Wed 00:46]</span></span>
    -   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-26 Wed 00:46]</span></span>

2.  DONE Volumn gateway: Can mount

    -   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-26 Wed 00:46]</span></span>
    -   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-26 Wed 00:46]</span></span>
    
    1.  Cache volume:
    
        -   Retain a copy of frequently accessed data subsets locally
    
    2.  Stored volume
    
        -   store all your data locally and backup point-in-time to S3
        -   For example, if you need replacement capacity for disaster recovery, you can recover the backups to Amazon EC2.
        -   Inexpensive

3.  DONE Tape gateway:

    -   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-27 Thu 00:08]</span></span>
    -   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-27 Thu 00:08] </span></span>
    -   cost-effectively and durably archive backup data in Amazon Glacier


<a id="org5b9e453"></a>

### DONE VPCS/ Subnets / Peering <code>[6/6]</code>

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-18 Tue 23:24]</span></span>
-   [X] Clear on VPC and networking concepts
-   [X] VPC endpoints, Ec2 internet accessibility

    + A VPC endpoint enables you to create a private connection between your VPC and another AWS service. 
    + Interface endpoint : is an elastic network interface with a private IP address that serves as an entry point for traffic destined to a supported service
    + Gateway endpoint: A gateway endpoint is a gateway that is a target for a specified route in your route table, used for traffic destined to a supported AWS service

1.  [X] When traffic stays in VPC or goes over the public internet
2.  [X] VPC Flow Logs
    1.  Publishing Flow Logs to CloudWatch Logs / S3
3.  [X] Security groups vs network ACLs: IP blacklist
4.  [X] VPC FAQs
    -   Ex: How to keep private S3 connections when using VPNs


<a id="org0cae2da"></a>

### DONE EC2 classes <code>[5/5]</code>

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-27 Thu 23:02]</span></span>
-   [X] Convertible Standard reserved vs Reversed Instances
    1.  <https://aws.amazon.com/ec2/pricing/reserved-instances/>
    2.  Convertible Standard reserved: cho phép thay đổi thuộc tính của reversed instance nhưng giá đắt hơn
-   [X] Spot vs spot block instances
    1.  Spot blocks: Spot Instances with a specified duration
-   [X] Do lab with EBS and find how to save file in EBS
-   [X] classic ELB vs ALB, NLB (network load balancer) including cost
    1.  ALB: Layer 7: Have others informations like SSL, HTTPS, return code, http header reading
    2.  NLB: Layer 4: It's just a connect
    3.  Price: CLB > ALB ~ NLB
-   [X] EC2 FAQs


<a id="orgcb72676"></a>

### DONE RDS <code>[4/6]</code>

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 00:05]</span></span>
-   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-28 Fri 00:12]</span></span>
-   [ ] Optimizing DB performance
-   [X] Elasticcache, Replicas, Aurora
    -   Elasticache
        -   Key-value cache
    -   Replicas
    -   Aurora
-   [X] Cross regioni snapshot copying, read replicas
    -   Can copy witin same region, across regions, across aws accounts
        -   Copy auto snapshot across accounts:
            1.  Create manual snapshot from auto snapshot
            2.  Copy manual snapshot to the other account.
        -   Copy across regions:
            -   First copy is full copy
        -   Copy encrypt snapshot
            -   Same region: use same KMS key or use new KMS key
            -   Across region: must create new KMS key because KMS key is region-specific
    -   Sharing snapshot
        -   Both encrypted and uncrypted can be copied
        -   Uncrypted shared:
            -   Can restore directly without copy
            -   Can copy across regions
        -   Encrypted shared:
            -   Must copy and then restore from copy
            -   Must have access to the KMS key that used to encrypt
                -   By sharing KMS key
            -   Can only copy it in same region
-   [ ] What each DB specialized in
-   [X] How encryption is done and what is used
    -   Encrypt instance
    -   Data sent between source and replicas is encrypted
-   [X] RDS FAQs


<a id="org89e4daa"></a>

### TODO Setting up 3, 2, 1 Tier web application <code>[0/3]</code>

1.  [ ] Knowing how to cost optimize
2.  [ ] Mix reserved instances and spot instances
3.  [ ] Different between Application ELB vs classic ELB, Ec2 reverse-proxy
    1.  Ec2 reverse-proxy


<a id="orgcdea899"></a>

### DONE ECS - Elastic Container Servicer AWS Beanstalk <code>[3/4]</code>

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 12:46]</span></span>
-   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 12:46]</span></span>
-   [X] ECS
    -   Task definition: This a blueprint that describes how a docker container should launch
    -   Task : This is a running container with the settings defined in the Task Definition.
    -   Service — Defines long running tasks of the same Task Definition
    -   Container Instance — This is just an EC2 instance
    -   Cluster — A logic group of EC2 instances
    -   Free
-   [X] Beanstalk
    -   Beanstalk is much more of a Platform-As-A-Service (PaaS). You push your raw code to it and it handles setting up the services, deploying code, and controlling the environment.
    -   Free
-   [ ] Split up processing jobs, non-critical batch component
-   [X] Beanstalk vs CodeFormation vs CodeDeploy vs ElasticCache


<a id="orgafa0f68"></a>

### DONE Hybrid Architecture:

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 13:45]</span></span>
-   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 13:45]</span></span>
-   VPN
    -   You can enable access to your remote network from your VPC by attaching a virtual private gateway to the VPC
    -   A virtual private gateway is the VPN concentrator on the Amazon side of the VPN connection


<a id="org94116af"></a>

### DONE LAMBDA, APi gateway <code>[2/2]</code>

-   State "REVIEW"     from "PROCESSING" <span class="timestamp-wrapper"><span class="timestamp">[2018-09-30 Sun 01:09]</span></span>
-   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 16:04]</span></span>
-   [X] Lamda Read FAQs
    1.  When you update a Lambda function, there will be a brief window of time, typically less than a minute, when requests could be served by either the old or the new version of your function.
    2.  Limit for number of concurrent executions per account per region
        1.  Applied at an account level
    3.  Multiple VPCs
        1.  Only by peering VPC
-   [X] API gateway
    1.  Amazon API Gateway does not support unencrypted (HTTP) endpoints


<a id="org95917f9"></a>

### TODO AWS Config


<a id="org5481c52"></a>

### TODO NGINX apps


<a id="org65e7014"></a>

### PROCESSING AWS Cognito

-   State "PROCESSING" from "TODO"       <span class="timestamp-wrapper"><span class="timestamp">[2018-09-29 Sat 16:17]</span></span>
-   Authencation service


<a id="org9df6f68"></a>

### TODO AWS Practice exams
