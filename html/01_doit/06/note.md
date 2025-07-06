# 1. 스타일 시트를 html 문서에 삽입하는 3가지 방법

## 1.1. Inline (인라인)

> 태그에 속성으로 작성

```
<a href="#" style="color:red">link</a>
```
---
## 1.2. Internal (내부스타일)

```
...중략

<head>
    <style>
        a{color:red}
    </style>
</head>
<body>
    <a href="#">link</a>

...중략
```
---
## 1.3. link (외부스타일)
> **웹표준**

**index.html**
```
...중략

<head>
    <link rel="stylesheet" href="style.css" />
</head>
<body>
    <a href="#">link</a>

```
**style.css**
```
a{color:red;}
```
---
# 2. 선택자의 종류

## 2.1. * (애스터리스크, 유니버셜: universal)

> 전체 선택자
>
> 태그를 모두 선택

`
*{margin:0px;}
`

---

## 2.2. element (요소/태그선택자)

> 태그 선택
>
```
태그이름{color:red;}

h1{color:red;}
```

---

## 2.3. 태그에 별명을 붙이는 선택자

### 2.3.1. `.` class

- html 문서에서 중복 사용 가능 


**index.html**
```
 <a href="#" class="myclass">link</a>
 <p class="myclass">paragraph</p>
```
**style.css**
```
.myclass{color:red;}
```

### 2.3.2. `#` id

- html 문서에 중복 사용 불가능 

**index.html**
```
 <a href="#" id="myid">link</a>
```
**style.css**
```
#myclass{color:red;}
```