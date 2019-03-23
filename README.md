# AR名刺API仕様書

# ユーザー

## `POST` api/v1/users

### 新規登録



#### Parameter

```
{
  "id_token": String,
  "name": String,
  "organizer": String,
  "age": String,
  "gender": String
}
```



#### Response

```json
{
	"access_token": "hogehgoehgoheogeafoeiaefwaf"
}
```



## `POST` api/v1/signin

### ログイン



**Parameter**

```
{
  "id_token": string
}
```



**Response**

```json
{
  "access_token": "aegheihgaohgoejofjoejaoafj"
}
```



## `POST` api/v1/users/image_regist

**学習用の画像を登録**



**Parameter**

```
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

```
{
  "id": 1,
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "gender": "man"
}
```



## `PATCH` api/v1/users

**情報の変更**



**Parameter**

```
{
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "gender": "man"
}
```



**Response**

```json
{
  "id": 1,
  "name": "ともき",
  "organizer": "フリーランス",
  "age": "2019/12/12",
  "gender": "man"
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

```
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
  "gender": "man"
}
```
