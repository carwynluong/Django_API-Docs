# TUTORIAL

## USER

### CREATE USER
![Alt text](image-1.png)

- Example:
```
{
  "email": "kayle@example.com",
  "password": "123456",
  "name": "kayle"
}
```

- Succesful:
![Alt text](image-2.png)


### GET TOKEN
![Alt text](image-3.png)

- Example:
```
{
  "email": "kayle@example.com",
  "password": "123456",
}
```

- Successful:
![Alt text](image-4.png)
> Token sẽ được sử dụng để đăng nhập


### Authorize
![Alt text](image-5.png)

- Dán vào tokenAuth theo cú pháp
> mã code là token của tài khoản kayle@example.com
![Alt text](image-6.png)
```
    token c07efcd0e11f296e925d4d23a4d74be54c032bf0
```
> mã code là token của tài khoản kayle@example.com

- Khi thành công:
![Alt text](image-7.png)

## RECIPE

### CREATE RECIPE
![Alt text](image-8.png)

- Example:
```
{
  "title": "coconut cake",
  "time_minutes": 10,
  "price": "8.5",
  "link": "coconut_cake@example.com",
  "tags": [
    {
      "name": "cake"
    }
  ],
  "ingredients": [
    {
      "name": "coconut"
    },
    {
      "name": "eggs"
    },
    {
      "name": "milk"
    }
  ]
}
```

- Successful:
![Alt text](image-9.png)


### READ RECIPE
![Alt text](image-10.png)
> Có thể lọc theo ingredients hoặc tags hoặc bỏ trống để hiển thị toàn bộ

> Lọc theo "id" của các ingredients và tags chứ không phải "name"

- Example:
![Alt text](image-11.png)
  > Ví dụ hiển thị toàn bộ

- Example:
![Alt text](image-12.png)
  > Ví dụ filter by ingredient id = 4 (Không có id = 4 trong database)

### UPDATE RECIPE
![Alt text](image-13.png)
> Update RECIPE sẽ có 2 method "PUT" và "PATCH"

> "PUT" sử dụng cập nhật toàn bộ

> "PATCH" chỉ cập một phần cụ thể

- Example:
```
{
  "time_minutes": 25,
  "price": "10.5"
}
```
> Cập nhật lại giá và thời gian cho recipe có id = 1

- Successful:
![Alt text](image-14.png)

## DELETE RECIPE
![Alt text](image-15.png)

- Example:
![Alt text](image-16.png)
> Điền id của recipe muốn xóa là done

- Successful:
![Alt text](image-17.png)
