
# Thiết kế ra blog

## Yêu cầu
Tạo ra một blog cá nhân gồm 2 phần chính:
- Ghi nhật ký
- Ghi những bài học học được

## Ý tưởng
- Sẽ có 3 microservice: một microservice quản lí nhật ký, một microservice quản lý bài học, một microservice dành cho admin
- diary-microservice cho nhật ký viết bằng nodejs + mongodb
- lesson-microserivce cho bài học viết bằng golang + mysql

## Sơ đồ network
![Sơ đồ network](https://raw.githubusercontent.com/vuduynewaccount/archive/main/network.drawio.svg)

## Sơ đồ tuần tự 

### admin-microservice
- Admin sẽ có vai trò tạo và xóa bài viết
![Sơ đồ tuần tự admin](https://raw.githubusercontent.com/vuduynewaccount/archive/main/admin-microservice-sd.svg)

### lesson-microservice
- lesson-microservice có vai trò tạo xóa bài viết theo yêu cầu của admin, trả ra bài viết để frontend hiển thị

![Sơ đồ tuần tự lesson](https://raw.githubusercontent.com/vuduynewaccount/archive/main/lesson-ms-sd.svg)

### diary-microservice
- Có tác dụng như lesson, chỉ khác là ngôn ngữ phía backend và database  
![Sơ đồ tuần tự diary](https://raw.githubusercontent.com/vuduynewaccount/archive/main/diary-ms-sd.svg)

## Sơ đồ lớp
- Em đặt tên chung lớp bài viết là post  
![Sơ đồ lớp](https://raw.githubusercontent.com/vuduynewaccount/archive/main/class.svg)

## Database 
Database em sẽ thiết kế giống các thuộc tính của sơ đồ lớp

## Repo
- diary-microservice (Nodejs, Mongodb): 
https://github.com/vuduynewaccount/diary
- lesson-microservice (Golang, MySql):
https://github.com/vuduynewaccount/lesson
