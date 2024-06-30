---

title: "Làm Quen Với Git Phần 3"
date: 2024-04-19T11:11:12.821Z
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
* Là một lập trình viên bạn thường xuyên nhận được các yêu cầu tư đơn vị là tải mã nguồn về, hoặc kéo code từ Github về máy để chạy đi.
* Hoặc bạn thường xuyên nhận được các yêu cầu từ cấp trên là bạn hãy đẩy mã nguồn, đẩy source code lên Github đi để team cùng làm việc.

## 2. Chuẩn bị
- Tạo một tài khoản Github cá nhân
- Đã cài đặt Git trên máy tính cá nhân

### 1.2. Phân biệt Git và Github
- Git là công cụ/phần mềm cài đặt và chạy trên máy tính cá nhân (Local)
- Github là nền tảng đám mây dùng để lưu trữ code và quản lý code (Cloud)


## 2. Cài đặt Git
Để cài đặt Git chúng ta thực hiện các bước sau:
1. Mở công cụ CMD gõ Git --version 
  ![alt](../../img/step1.png "step1")
  Nếu màn trả về kết quả như hình trên có nghĩa là máy bạn chưa cài công cụ Git

2.  Mở trình duyệt **Microsoft Edge** > truy cập địa chỉ sau https://git-scm.com/downloads ![alt text](../img/step2.png)
3. Tại màn hình **Git Download** > chọn hệ điều hành tương ứng
- *Ở ví dụ này mình sẽ chọn hệ điều hành Windows*
4. Tại màn hình **Download For Windows** > chọn edition tương ứng tại mục **Standalone Installer**
- *Ở đây mình sẽ chọn edition 64bit*
5. Sau khi đã download thành công > tiến hành mở file cài đặt ![alt text](../img/step6.png)
6. Xuất hiện màn hình **User Account Control** > chọn Yes ![alt text](../img/step7.png)
7. Tại cửa sổ **Git Setup** > chọn Next ![alt text](images/git_coban/bai1/step8.png)
8. Tại màn hình **Select Destination Location** > mặc định chọn Next ![alt text](../../img/step9.png)
9.  Tại màn hình **Select Components** > mặc định chọn Next ![alt text](images/gitcoban/bai1/step10.png)
10.  Tại màn hình **Slect Start Menu Folder** > mặc định chọn Next ![alt text](../../img/step11.png)
11. Tại màn hình **Choosing the default editor used by Git** > mặc định chọn Next ![alt text](../../img/step12.png)
12. Tại màn hình **Adjust the name of the intial branch in new repositoroes** > mặc định chọn Next ![alt text](images/git_coban/bai1/step13.png)
13. Tại màn hình **Adjusting your PATH environment** > chọn mặc định Option 2
- Nếu các bạn chọn option 3: thì các bạn có thể gõ lệnh Git trực tiếp trong cửa sổ CMD của Windows nha![alt text](images/git_coban/bai1/step14.png)
14.  Tại màn hình **Chosossing the SSH executable** > mặc định chọn Next ![alt text](images/git_coban/bai1/step15.png)
2.  Tại màn hình ***Choosing HTTPS transport backed** > mặc định chọn Next ![alt text](images/git_coban/bai1/step16.png)
3.  Tại màn hình **Configureing the line ending conversions** > mặc định chọn Next![](images/git_coban/bai1/step17.png)
4.  Tại màn hình **Configuring the terminal  emulator to use with Git Bash** > mặc định chọn Next ![](images/git_coban/bai1/step18.png)
5.  Tại màn hình **Choose the default behavior of 'git pull'** > mặc định chọn Next ![](images/git_coban/bai1/step19.png)
6.  Tại màn hình **Choose a credential helper** > mặc định chọn Next![](images/git_coban/bai1/step20.png)
7.  Tại màn hình **Configuring extra options** > mặc định chọn Next![](images/git_coban/bai1/step21.png)
8.  Tại màn hình **Configuring experimental options** mặc định chọn không chọn gì cả > Install ![](images/git_coban/bai1/step22.png)
9.  Tại màn hình install > chờ đợi thiết đặt hoàn tất ![](images/git_coban/bai1/step23.png)
10. Xuất màn hình **Completing the Gi Setup Wizard** > uncheck các lựa chọn và click Finish ![](images/git_coban/bai1/step24.png)
11. Phải chuột trên màn hình **Desktop** >  đảm bảo xuất hiện lựa chọn **Open Git Bash here** ![](images/git_coban/bai1/step25.png)
>Vậy là quá trình cài đặt Git đã hoàn tất"

## 3. Thiết đặt user/namepassword

``` diff {hl_lines=[4,"6-7"]}
*** /path/to/original	''timestamp''
--- /path/to/new	''timestamp''
***************
*** 1 ****
! This is a line.
--- 1 ---
! This is a replacement line.
It is important to spell
-removed line
+new line
```

```diff {hl_lines=[4,"6-7"], linenos=false}
*** /path/to/original	''timestamp''
--- /path/to/new	''timestamp''
***************
*** 1 ****
! This is a line.
--- 1 ---
! This is a replacement line.
It is important to spell
-removed line
+new line
```

### 3.0.1. Makefile

``` makefile {linenos=false}
CC=gcc
CFLAGS=-I.

hellomake: hellomake.o hellofunc.o
     $(CC) -o hellomake hellomake.o hellofunc.o -I.
```

``` makefile
CC=gcc
CFLAGS=-I.

hellomake: hellomake.o hellofunc.o
     $(CC) -o hellomake hellomake.o hellofunc.o -I.
```

### 3.0.2. JSON

``` json
{"employees":[
    {"firstName":"John", "lastName":"Doe"},
]}
```

### 3.0.3. Markdown

``` markdown
**bold** 
*italics* 
[link](www.example.com)
```

### 3.0.4. JavaScript

``` javascript
document.write('Hello, world!');
```

### 3.0.5. CSS

``` css
body {
    background-color: red;
}
```

### 3.0.6. Objective C

``` objectivec
#import <stdio.h>

int main (void)
{
	printf ("Hello world!\n");
}
```

### 3.0.7. Python

``` python
print "Hello, world!"
```

### 3.0.8. XML

``` xml
<employees>
    <employee>
        <firstName>John</firstName> <lastName>Doe</lastName>
    </employee>
</employees>
```

### 3.0.9. Perl

``` perl
print "Hello, World!\n";
```

### 3.0.10. Bash

``` bash
echo "Hello World"
```

### 3.0.11. PHP

``` php
 <?php echo '<p>Hello World</p>'; ?> 
```

### 3.0.12. CoffeeScript

``` coffeescript
console.log(“Hello world!”);
```

### 3.0.13. C#

``` cs
using System;
class Program
{
    public static void Main(string[] args)
    {
        Console.WriteLine("Hello, world!");
    }
}
```

### 3.0.14. C++

