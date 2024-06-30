---

title: "Làm Quen Với Git Phần 2"
date: 2024-04-21T12:31:48.383Z
description: "Git siêu cơ bản"
draft: false
hideToc: false
enableToc: true
enableTocContent: false
author: Trịnh Thanh Thiên
authorEmoji: 👩‍💻
pinned: true
tags:
- git
- code
series:
- Git Siêu Cơ Bản
categories:
- dev
image: images/git/bai1/git.webp
---

## 1. Ngữ cảnh
* Là một lập trình viên bạn thường xuyên nhận được các yêu cầu tư đơn vị là tải mã nguồn về, kéo source code, hoặc kéo Project từ GitHub về máy để chạy, để kiểm tra, hoặc là để tham khảo,...
> Tải xuống một Project có sẵn từ GitHub về máy tính cá nhân

* Hoặc bạn thường xuyên nhận được các yêu cầu từ cấp trên là bạn hãy đẩy mã nguồn, đẩy source code lên GitHub đi để team cùng làm việc.
> Chỉnh sửa nội dung mã nguồn được tải về từ GitHub
> Đẩy Project có sẵn tại máy tính cá nhân lên GitHub
* Một Project == một Repository trên GitHub == một Folder trên máy tính cá nhân (chúng ta có thể hiểu tương đương như thế cho dễ nha)

## 2. Chuẩn bị
- Tạo một tài khoản GitHub cá nhân
- Đã cài đặt Git trên máy tính cá nhân
- Tạo một thư mục đặt tên GitTutorial trên máy tính cá nhân

## 3. Nội dung
* Tải (Clone) một Project từ GitHub về máy tính cá nhân thông qua giao thức Https
* Đẩy mã nguồn (source code) có sẵn từ máy tính cá nhân lên Project của GitHub
* Đẩy Project có sẵn trên máy tính cá nhân lên GitHub

### 3.1. Tải mã nguồn từ GitHub về máy tính cá nhân thông qua giao thức Https
* Để tải mã nguồn từ trang GitHub về máy tính thì việc đầu tiên chúng ta cần xác định vị trí lưu mã nguồn trên máy tính cá nhân của chúng ta, để khi tải mã nguồn về thì nó sẽ lưu ở đâu trên máy tính cá nhân của chúng ta
  * *Trong bài này chúng ta sẽ sử dụng thư mục **GitTutorial** làm nơi lưu mã nguồn*
* Để tải mã nguồn từ trang GitHub về máy tính cá nhân chúng ta làm như sau

1. Tại màn hình Web Browser truy cập vào địa chỉ GitHub mà bạn muốn tải mã nguồn
*Ở ví dụ này, địa chỉ mình muốn tải mã nguồn là: https://GitHub.com/zzossig/hugo-theme-zzo" ![alt text](../../img/step1.png)
1. Xuất hiện màn hình như ảnh dưới > bấm chọn biểu tượng **code** ![alt text](../../img/step2.png)
2. Xuất hiện bảng **menu optins** như hình > chọn **tab** **Https** > copy địa chỉ **Https** ![alt text](../../img/step3.png)
3. Trên máy tính cá nhân, truy cập vào thư mục GitTutorial đã được tạo ở bước chuẩn bị
4. Tại thư mục GitTutorial > phải chuột chọn **Open Git Bash here**![alt text](../../img/step5.png)
5. Xuất hiện màn hình Git command > nhập lệnh Git clone "Link GitHub Https" > Enter
- *Link GitHub Https: là link mà bạn đã copy tại bước 3*
- *Ở ví dụ này mình sẽ nhập đường dẫn là: https://GitHub.com/zzossig/hugo-theme-zzo.git* ![alt text](../../img/step6.png)
1. Đảm bảo quá trình tải Project đã được bắt đầu, xuất hiện thông báo **cloning** hình như ảnh bên dưới ![alt text](../../img/step7.png)
2. Đảm bảo quá trình tải Project về đã hoàn thành, xuất hiện thông báo **done** như hình bên dưới![alt text](../../img/step8.png)
3. Quay trở lại thư mục **GitTutorial** > đảm bảo đã xuất hiện **Folder** mới có tên trùng với tên Project trên GitHub như ảnh dưới![alt text](../../img/step9.png)
4.  Mở Folder vừa tải về đảm bảo đã xuất hiện các nội dung như ảnh dưới, có nghĩa là chúng ta đã tải Project về thành công ![alt text](../../img/step10.png)
> Vậy là chúng ta đã biết cách **Clone/Download/Tải/Kéo** một **Project** từ **GitHub** về máy tính cá nhân thông qua giao thức **Https**
> Vậy là từ giờ trở đi nếu có ai đó đưa nói bạn hãy kéo code về để chạy đi và đưa cho bạn một đường dẫn thì bạn chỉ cần sử dụng câu lệnh git clone là đã có thể download source code về rồi nha

### 3.2 Đẩy Project có sẵn trên máy tính cá lên lên GitHub - Project trống
Để có thể đẩy một Project có sẵn từ máy tính cá nhân lên trang GitHub chúng ta cần tạo sẵn một Repository trống trên trang GitHub

* Tạo Repository trên GitHub
1. Tại trình duyệt Web truy cập vào địa chỉ: https://GitHub.com/login
2. Tại màn hình GitHub chọn Sign In > đăng nhập bằng tải khoản GitHub cá nhân ![alt text](../../img/step3_1.png)
3. Tại màn hình **GitHub** chọn > click chọn biểu tượng **profile** > chọn **your repository** ![alt text](../../img/step3_2.png)
4. Tại màn hình **Repository** > chọn **New**![alt text](../../img/step3_3.png)
5. Tại màn hình Create a new repository > khai báo thông tin như ảnh dưới > Create repository
   1. Nhập Repository name: Giturial01
   2. Sau khi khai báo Repository name > kéo xuống cuối trang và chọn Create repository ![alt text](../../img/step3_4.png)
6. Đảm bảo đã tạo được Repository thành công, xuất hiện hình như ảnh dưới ![alt text](../../img/step3_5.png)
7. Sau đó ta sẽ copy thông tin **git remote add origin https://yourlinkrepository.git** ![alt text](../../img/step3_6.png)

* Tải Project từ máy tính cá nhân lên Repository
1. Tại thư mục **GitTutorial** mình đã tạo ở bước chuẩn bị > khởi tạo thư mục mới tên **GitTurial01** ![alt text](../../img/step3_7.png)
2. Tại thư mục **Gitutorial01** > tạo file text tên **Readme.txt** ![alt text](../../img/step3_8.png)
3. Trong file Readme.txt > nhập nội dung **"Hello world"** > Save > đóng file text ![alt text](../../img/step3_9.png)
4. Tại thư mục GitTutorial01 > phải chuột chọn Open Git Bash here 
*Mọi người lưu ý là muốn tải source code từ thư mục nào thì chúng ta NÊN Open Git Bash ở thư mục đó nha, khi chúng ta thao tác tải source code về cũng thế* ![alt text](../../img/step3_10.png)
5. Tại màn hình git command > ta nhập git init > Enter 
*git init là viết tắt của git initialize tức là bắt đầu khởi gạo git trên thư mục này* ![alt text](../../img/step3_11.png)
6. Tiếp theo ta nhập dòng lệnh git remote add origin + thông tin https://yourlinkrepository mà chúng ta đã copy tại bước 7 trước đó > Enter
*git remote là câu lệnh để chúng ta kết nối máy tính của chúng ta đến repository GitHub*  ![alt text](../../img/step3_12.png)
1. Nếu màn hình Git Bash không báo lỗi gì thì có nghĩa là chúng ta đã kết nối đến Github thành công ![alt text](../../img/step3_13.png)
2. Tiếp theo chúng ta nhập git status > enter
*Trong đó git status là câu lệnh giúp chúng ta kiểm tra sự thay đổi của project*
*Trong ví dụ này thì git báo là chúng ta có một file Readme.txt bị thay đổi (tên fie sẽ màu đỏ)* ![alt text](../../img/step3_14.png)
4. Tiếp theo chúng ta nhập git add . > Enter
*Mọi người lưu ý là git add + (dấu chấm) nha, có nghĩa là thêm tất cả, chúng ta sẽ thêm tất cả những gì bị thay đổi vào git* ![alt text](../../img/step3_15.png)
10. Tiếp theo ta nhập lại git status > Enter > đảm bảo file Readme.txt đã đổi trạng thái sang mau xanh như hình dưới
*Tức là chúng ta đã add thành công* ![alt text](../../img/step3_16.png)
11. Tiếp tục nhập git commit -m "your message" > Enter
*Với tham số -m nghĩa là message*
*Nội dung message chúng ta nhập tùy ý nha, sao cho nó có ý nghĩa nhất*
*Với lệnh git commit, các nội dung thay đổi đã được add sẽ tiến vào trạng thái sẵn sàng để đẩy lên GitHub* ![alt text](../../img/step3_17.png)
12. Nếu màn hình Git Bash không báo gì > có nghĩa chúng ta đã commit thành công ![alt text](../../img/step3_18.png)
13. Xác định tên nhánh (branch)
*Với tên nhánh là thông tin xuất hiện cuối mỗi câu nhắc lệnh*
*Trong ví dụ của mình thì tên nhánh sẽ là "master" ![alt text](../../img/step3_19.png)
15. Cuối cùng ta dùng lệnh git push -u origin + <tên nhánh> > Enter 
*Git push là câu lệnh giúp chúng ta đẩy những thay đổi đã lưu trong git commit từ máy tính cá nhân lên GitHub nha* ![alt text](../../img/step3_20.png)
17. Xuất hiện Pop-up yêu cầu chúng ta chứng thực chúng ta là chủ sở hữu của Repository mà chúng ta đang muốn kết nối nha > chọn Sign in with your browser ![alt text](../../img/step3_21.png)
18. Chúng ta sẽ được chuyển hướng đến trang đăng nhập GitHub > đăng nhập tài khoản GitHub cá nhân > Sign in ![alt text](../../img/step3_22.png)
19. Đảm bảo đã đăng nhập thành công > xuất hiện thông báo như ảnh dưới ![alt text](../../img/step3_23.png)
20. Quay lại màn hình Git Bash > đảm bảo đã Upload thành công > xuất hiện thông báo "done" ![alt text](../../img/step3_24.png)
21. Quay lại trang Repository của chúng ta > nhấn F5 > kiểm tra lại > đảm bảo đã xuất hiện File Readme.txt với nội dung "Hello World" ![alt text](../../img/step3_25.png)
> Vậy là chúng ta đã biết cách upload một Project có sẵn trên máy tính cá nhân lên GitHub - Project (Repository)


### 3.3  Chỉnh sửa nội dung mã nguồn được tải về từ GitHub
Trong trường hợp chúng ta đã có sẵn một Repository có mã nguồn trên GitHub, bây giờ chúng ta muốn tải về để chỉnh sửa mã nguồn đó, để update nội dung thì chúng ta làm như sau:
* Để giả lập một Repository đang chứa mã nguồn trên GitHub, chúng ta sẽ tạo mới đồng thời một Repository và File README.
1. Tại trình duyệt Web truy cập vào địa chỉ: https://GitHub.com/login
2. Tại màn hình GitHub chọn Sign In > đăng nhập bằng tải khoản GitHub cá nhân ![alt text](../../img/step3_1.png)
3. Tại màn hình **GitHub** chọn > click chọn biểu tượng **profile** > chọn **your repository** ![alt text](../../img/step3_2.png)
4. Tại màn hình **Repository** > chọn **New**![alt text](../../img/step3_3.png)
5. Tại màn hình **Create a new repository** > khai báo thông tin như ảnh dưới > Create repository
   1. Nhập Repository name: **GitTurial00**
   2. Sau khi khai báo Repository name > click chọn **Add a README file**
   3. Sau đó kéo xuống cuối trang và chọn **Create repository **![alt text](../../img/step2_5.png)
6. Đảm bảo đã tạo được **Repository** thành công, xuất hiện hình như ảnh dưới ![alt text](../../img/step2_6.png)
7. Tại màn hình > chọn biểu tượng cây bút để chỉnh sửa File **README** ![alt text](../../img/step2_7.png)
1. Tại màn hình chỉnh sửa File **README** > nhập nội dung là **"I'm GitHub"** ![alt text](../../img/step2_8.png)
2. Sau khi chỉnh sửa nội dung File **README** > chọn **commit changes** ![alt text](../../img/step2_8.png)
3. Tại màn hình **Commit changes** > chọn nút **commit changes** ![alt text](../../img/step2_9.png)
4. Đảm bảo nội dung File **README** đã được chỉnh sửa thành công ![alt text](../../img/step2_10.png)
5. Tại màn hình màn hình **README** > chọn **GitTutorial00** để trở về màn hình Project ![alt text](../../img/step2_11.png)
6. Tại màn hình Project > chọn nút Code > copy URL Https 
*Nội dung vừa copy: https://github.com/Thien1n/GitTutorial00.git*

> vậy là chúng ta đã có một Repository đang chứa mã nguồn trên GitHub, giả sử File mã nguồn của chúng ta là File README > việc tiếp theo chúng ta là chỉnh sửa, cập nhật nội dung File README từ Git

* Chỉnh sửa mã nguồn trên GitHub thông qua Git
1. Tại thư mục GitTutorial đã tạo tại bước chuẩn bị > phải chuột chọn **Open Git Bash here** ![alt text](../../img/step2_15.png)
2. Tại màn hình Git Bash > nhập Git Clone + "YourLinkProject" > Enter
*YourLinkProject: ở đây là URL mình đã copy ở bước 13 ở trên nha*
*YourLinkProject của mình là: https://github.com/Thien1n/GitTutorial00.git* ![alt text](../../img/step2_13.png)
3. Đảm bảo đã clone Project về máy tính cá nhân thành công > xuất hiện thông báo Done  ![alt text](../../img/step2_14.png)
4. Tại màn hình thư mục GitTutorial > đã xuất hiện thư mục GitTutorial00 > double click để mở thư mục GitTutotial00 ![alt text](../../img/step2_16.png)
5. Tại thư mục GitTutorial00 > xuất hiện file README > phải chuột chọn Open With Notepad ![alt text](../../img/step2_17.png)
6. tại màn hình Notepad chúng ta chỉnh sửa, cập nhật nội dung bằng cách thêm dòng **"Im Git from Local"** > lưu file lại và đóng file README ![alt text](../../img/step2_18.png)

> Vậy là chúng ta vừa chỉnh sửa mã nguồn bằng cách nhập thêm các nội dung mới cho File README, bây giờ chúng ta sẽ upload mã nguồn lên lại Repository của chúng ta trên GitHub hay còn gọi là Update mã nguồn
* Upload mã nguồn
1. Tại thư mục GitTutorial00 > ta phải chuột chọn **Open Git Bash here** ![alt text](../../img/step2_19.png)
2. Tại màn hình Git Bash > nhập git status > Enter ![alt text](../../img/step2_22.png)
3. Xuất hiện dòng chữ màu đỏ thể hiện File README đã có sự thay đổi ![alt text](../../img/step2_20.png)
4. Tiếp tục nhập > git add . > Enter ![alt text](../../img/step2_21.png)
5. Đảm bảo quá trình add đã hoàn tất > màn hình không báo lỗi gì cả
6. tiếp tục nhập > git status > đảm bảo xuất hiện dòng chữ xanh lá ![alt text](../../img/step2_23.png)
7. tiếp tục nhập > git commit -m "your message"  ![alt text](../../img/step2_24.png)
*your message: bạn có thể nhập nội dung tùy ý sao cho có ý nghĩa nhất*
8. Đảm bảo đã commit thành công > màn hình báo đã changed ![alt text](../../img/step2_26.png)
8. Cách xác định tên nhánh (branch) 
*Với tên nhánh là thông tin xuất hiện cuối mỗi câu nhắc lệnh*
*Trong ví dụ của mình thì tên nhánh sẽ là "main"  ![alt text](../../img/step2_25.png)
9. tại màn hình Git bash ta nhập git push -u origin + "tên nhánh" ![alt text](../../img/step2_27.png)
10. đảm bảo đã upload mã nguồn lên GitHub thành công > màn hình báo Done ![alt text](../../img/step2_28.png)
*lưu ý, có thể trong quá trình Push mã nguồn mà GitHub xuất hiện PopUp bắt các bạn Login để chứng minh bạn là chủ sở hữu hoặc có quyền tương tác trên Repository này, các bạn cứ chọn Login bình thường như mình đã hướng dẫn ở phàn trước nha"
11. Quay lại màn hình Repository > bấm F5
12. Đảm bảo File README của mình đã có thêm nội dung mới là **Im Git from Local** ![alt text](../../img/step2_29.png)
> Vậy là chúng ta đã biết cách tải mã nguồn từ GitHub về để chỉnh sửa, sau đó push/upload lên lại GitHub, nếu sau này bạn nhận được một yêu cầu là hãy tải mã nguồn từ từ GitHub về để chỉnh sửa và cho bạn một đường Link, bạn cứ làm theo cách này là được nha
