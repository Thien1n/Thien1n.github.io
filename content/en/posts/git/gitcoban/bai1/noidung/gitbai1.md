---

title: "Làm Quen Với Git Phần 1"
date: 2024-04-19T11:11:12.821Z
description: "Git siêu cơ bản"
draft: false
hideToc: false
enableToc: true
enableTocContent: true
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

## 1. Tổng quan về Git
###    1.1. Tại sao cần sử dụng Git
Git là một công cụ được cài đặt trên máy tính cá nhân sử dụng với mục đích quản lý mã nguồn (source code) một cách hiệu quả hơn

Các tính năng mà chúng ta thường sử dụng trên Git có thể kể đến như: 
- Kiểm tra lịch sử mã nguồn 
- Kiểm tra và truy vấn sự thay đổi mã nguồn
- Quản lý phiên bản mã nguồn,...


### 1.2. Phân biệt Git và Github
- Git là công cụ/phần mềm được cài đặt và chạy trên máy tính cá nhân (Local)
- Github là nền tảng lưu trữ mã nguồn trực tuyến trên đám mây (Cloud)


## 2. Cài đặt Git
Để cài đặt Git chúng ta thực hiện các bước sau:
1. Mở công cụ CMD gõ ***Git --version***
  ![alt](../../img/step1.png "step1")
  Nếu màn trả về kết quả như hình trên có nghĩa là máy bạn chưa cài công cụ Git

2.  Mở trình duyệt **Microsoft Edge** > truy cập địa chỉ sau https://git-scm.com/downloads ![alt text](../../img/step2.png)
3. Tại màn hình **Git Download** > chọn hệ điều hành tương ứng
- *Ở ví dụ này mình sẽ chọn hệ điều hành Windows*
4. Tại màn hình **Download For Windows** > chọn edition tương ứng tại mục **Standalone Installer**
- *Ở đây mình sẽ chọn edition 64bit*
5. Sau khi đã download thành công > tiến hành mở file cài đặt ![alt text](../../img/step6.png)
6. Xuất hiện màn hình **User Account Control** > chọn Yes ![alt text](../../img/step7.png)
7. Tại cửa sổ **Git Setup** > chọn Next ![alt text](../../img/step8.png)
8. Tại màn hình **Select Destination Location** > mặc định chọn Next ![alt text](../../img/step9.png)
9.  Tại màn hình **Select Components** > mặc định chọn Next ![alt text](../../img/step10.png)
10.  Tại màn hình **Slect Start Menu Folder** > mặc định chọn Next ![alt text](../../img/step11.png)
11. Tại màn hình **Choosing the default editor used by Git** > mặc định chọn Next ![alt text](../../img/step12.png)
12. Tại màn hình **Adjust the name of the intial branch in new repositoroes** > mặc định chọn Next ![alt text](../../img/step13.png)
13. Tại màn hình **Adjusting your PATH environment** > chọn mặc định Option 2
- Nếu các bạn chọn option 3: thì các bạn có thể gõ lệnh Git trực tiếp trong cửa sổ CMD của Windows nha![alt text](../../img/step14.png)
14.  Tại màn hình **Chosossing the SSH executable** > mặc định chọn Next ![alt text](../../img/step15.png)
2.  Tại màn hình ***Choosing HTTPS transport backed** > mặc định chọn Next ![alt text](../../img/step16.png)
3.  Tại màn hình **Configureing the line ending conversions** > mặc định chọn Next![alt text](../../img/step17.png)
4.  Tại màn hình **Configuring the terminal  emulator to use with Git Bash** > mặc định chọn Next ![alt text](../../img/step18.png)
5.  Tại màn hình **Choose the default behavior of 'git pull'** > mặc định chọn Next ![alt text](../../img/step19.png)
6.  Tại màn hình **Choose a credential helper** > mặc định chọn Next![alt text](../../img/step20.png)
7.  Tại màn hình **Configuring extra options** > mặc định chọn Next![alt text](../../img/step21.png)
8.  Tại màn hình **Configuring experimental options** mặc định chọn không chọn gì cả > Install ![alt text](../../img/step22.png)
9.  Tại màn hình install > chờ đợi thiết đặt hoàn tất ![alt text](../../img/step23.png)
10. Xuất màn hình **Completing the Gi Setup Wizard** > uncheck các lựa chọn và click Finish ![alt text](../../img/step24.png)
11. Phải chuột trên màn hình **Desktop** >  đảm bảo xuất hiện lựa chọn **Open Git Bash here** ![alt text](../../img/step25.png)
>Vậy là quá trình cài đặt Git trên máy tính cá nhân đã hoàn tất"

## 3. Thiết đặt username/email cho Git
### 3.1. Tại sao cần khai báo username/email cho Git
Để kết nối Git với nền tảng lưu trữ mã nguồn trực tuyến như Github thì chúng cần thiết lập khai báo username hoặc email cho Git
Từ đó Git có thể định danh người đang tương tác với mã nguồn trên hệ thống local là ai và thông qua địa chỉ email thì Github có thể xác định bạn là ai
- Trong đó:
  - Email là địa chỉ bạn đã sử dụng để đăng ký GitHub
  - Username là tên đăng nhập vào GitHub của các bạn

### 3.2. Lệnh cấu hình
```git
git config --global user.name "Your Github Username"
git config --global user.email "Your Email Address"
```

### 3.3. Cài đặt
1. Tại màn hình **Desktop** > phải chuột chọn **Open Git Bash here** ![alt text](../../img/step25.png)
2. Tại màn hình Git command > nhập git config --list ![alt text](../../img/step31.png)
3. Tiếp tục nhập **git config --global user.name "Your Github Username"** > Enter
*Tại ví dụ này mình sẽ nhập username của mình là Thien1n* ![alt text](../../img/step32.png)
4. Tiếp tục nhập **git config --global user.email "Your Email Address"**
*Tại ví dụ này mình sẽ nhập username của mình là trinhthanhthien6.it@gmail.com* ![alt text](../../img/step33.png)
6. Chúng ta sẽ nhập **git config --list** để kiểm tra lại kết quả đã khai báo > đảm bảo thông tin của chúng ta đã được hiển thị trong danh sách ![alt text](../../img/step34.png)
>Vậy là chúng ta đã khai báo thông tin username/Email cho git thành công

### 3.4. Tham khảo
* https://docs.github.com/en/get-started/getting-started-with-git/setting-your-username-in-git
* https://linuxize.com/post/how-to-configure-git-username-and-email/
* https://stackoverflow.com/questions/35853986/git-easiest-way-to-reset-git-config-file

