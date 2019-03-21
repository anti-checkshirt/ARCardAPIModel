# AR名刺API仕様書

# ユーザー

## `POST` api/v1/users

### 新規登録



#### Parameter

```json
{
  "id_token": String,
  "name": String,
  "organizer": String,
  "age": String,
  "sex": String
}
```



#### Response

```
{
	"access_token": String
}
```



## `POST` api/v1/signin

### ログイン



**Parameter**

```json
{
  "id_token": string
}
```



**Response**

```json
{
  "access_token": string
}
```



## `POST` api/v1/users/image_regist

**学習用の画像を登録**



**Parameter**

```json
{
	"image1": Data,
	"image2": Data,
	....
}
```



**Response**

```json
{
  "code": 200,
  "message": "OK"
}
```





## `GET` api/v1/users

### 自分の情報取得



**Response**

```json
{
  "id": 1,
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "sex": "man"
}
```



## `PATCH` api/v1/users

**情報の変更**



**Parameter**

```json
{
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "sex": "man"
}
```



**Response**

```json
{
  "id": 1,
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "sex": "man"
}
```



## `DELETE` api/v1/users

**退会**



**Response**

```json
{
  "code": 200,
  "message": "OK"
}
```



#  Judgment

## `POST` api/v1/Judgment

**画像からユーザーを判定する**



**Parameter**

```json
{
  "image": Data
}
```



**Response**

```json
{
  "id": 1,
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "sex": "man"
}
```