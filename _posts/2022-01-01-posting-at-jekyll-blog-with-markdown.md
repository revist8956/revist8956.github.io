---
layout: post
title: -[Markdown] Jekyll 블로그에 포스팅 하기
date: 2022-01-01 16:00 +0800
tags: [markdown, tutorial]
categories: github_blog
toc:  true
comments: true
---
## jekyll 블로그에 포스팅을 하려면..
마크다운 문법 형식을 알아야 한다. 다만 본 포스팅에서는 마크다운 문법과 HTML 태그를 혼재하여 사용할 것이다. 순수하게 마크다운 문법을 알고 싶은 사람은 [마크다운 가이드](https://www.markdownguide.org/basic-syntax/)를 참고하자.
<hr>

## 구분선 
구분선은 `<hr>` 로 나타낸다
<hr> <hr> <hr>

## 줄바꿈
1) 줄바꿈을 하고 싶으면 문장 뒤에 스페이스바를 두 번 & 엔터해준다.
```
Revist입니다.  
만나서 반갑습니다.
```
Revist입니다.  
만나서 반갑습니다.

2) HTML 태그로는 `<br>`을 사용할 수 있다.
```
Revist입니다. <br> 만나서 반갑습니다.
```
Revist입니다. <br> 만나서 반갑습니다.
<hr>

## Headings
제목을 표시할 때는 Header를 사용한다. #의 개수로 크기를 설정할 수 있다.
```
# Heading Level 1
## Heading Level 2
### Heading Level 3
#### Heading Level 4
##### Heading Level 5
###### Heading Level 6
```

# Heading Level 1
## Heading Level 2
### Heading Level 3
#### Heading Level 4
##### Heading Level 5
###### Heading Level 6


<br>안타깝게도 Level 7이상은 없다.
<hr>

## Escape Character
`\`를 사용하면 문법이 적용되지 않는다.


\*\*볼드체볼드체**


원래 같으면 볼드체가 적용되어 **볼드체볼드체**로 보일텐데 문법 그대로 보여진다.
<hr>

## 텍스트 강조
### 볼드
```
**볼드체로 쓰려면 이렇게!**
<strong> 볼드체로 쓰려면 이렇게! </strong>
```
- **볼드체로 쓰려면 이렇게**

### 기울임
```
*기울이려면 이렇게!*
<em> 기울이려면 이렇게! </em>
```
- *기울이려면 이렇게!*

### 취소선
```
~~나무위키~~
<del> 나무위키 </del>
```
- ~~나무위키~~

### 밑줄
```
<u>난 경기도 성남의 이재원이다!!</u>
<ins> 난 경기도 성남의 이재원이다!! <ins>
```
- <u>난 경기도 성남의 이재원이다!!</u>

### 하이라이트
```
<mark>난 경기도 성남의 이재원이다!!</mark>
```
- <mark>난 경기도 성남의 이재원이다!!</mark>

### Superscript
```
절대영도<sup>일격필살!!</sup>
```
- 절대영도<sup>일격필살!!</sup>

### Subscript
```
이건 자주 <sub>사용</sub>하진 않을 것 같다.
```
- 이건 자주 <sub>사용</sub>하진 않을 것 같다.

### 글씨 색 변경
```
<span style="color:cornflowerblue;">콘플라워블루 색입니다.</span>
```
- <span style="color:cornflowerblue;">콘플라워블루 색입니다.</span>

### 출처 표기
```
잘 모르고 무식한 사람이 신념을 가지면 무섭습니다. --- <cite> 이경규 </cite>
```
- 잘 모르고 무식한 사람이 신념을 가지면 무섭습니다. --- <cite> 이경규 </cite>
<hr>

## 각주
글자 위 버튼을 누르면 각주로 이동하게 된다. 구문은 다음과 같다.


이재원[^fn-ljw]
```
이재원[^fn-ljw] 
```
모든 각주들은 `^fn-` 형식으로 작성된다. `^fn-`의 뒤에는 단어와 각주를 이어줄 ID를 만들어 작성해주면 된다. 그러면
```
[^fn-ljw]: 병신이다.
```
[^fn-ljw]: 병신이다.
이러한 형태로 사용할 수 있게 된다.
<hr>

## Code block
### 인라인 코드 블록
```
문장 중간에 `코드를 넣고 싶을 때` 사용하면 된다.
```
문장 중간에 `코드를 넣고 싶을 때` 사용하면 된다.

### 코드 블록
    ```언어 이름(소문자)
    적을 코드
    ```

코드 블록은 **스페이스바 4번 또는 Tab 2번**으로도 표현할 수 있다.


언어 이름까지 적으면 색깔 하이라이트가 들어간다!
```python
a = 3
b = 5
def add (x, y):
  return x+y
print(add (a, b))
```
<hr>

## 인용문
인용문을 만들기 위해서는 문단 앞에 `>`를 넣어주면 된다.
```
> 다만 마시로의 표정에 괴로움은 보이지 않는다. 살짝 뺨을 붉히고 어쩐지 쑥스러워하는 듯한 느낌이다.
--- <cite> 사쿠라장의 애완그녀 7 </cite>
```
> 다만 마시로의 표정에 괴로움은 보이지 않는다. 살짝 뺨을 붉히고 어쩐지 쑥스러워하는 듯한 느낌이다. <br>
--- <cite> 사쿠라장의 애완그녀 7 </cite>

<br>
많은 문단을 인용할 경우 문단 사이에 `>`를 넣어주면 된다.

```
> "지금 내가 그리고 싶은 건 소라타뿐이야."
>
> 시호를 포함한 네 학생의 손은 깔끔하게 멈춰버렸다. <br>
--- <cite> 사쿠라장의 애완그녀 7 </cite>
```

> "지금 내가 그리고 싶은 건 소라타뿐이야."
>
> 시호를 포함한 네 학생의 손은 깔끔하게 멈춰버렸다. <br>
--- <cite> 사쿠라장의 애완그녀 7 </cite>

<br>
인용문 안에 다시 인용문을 넣을 수도 있다. `>>`를 사용해주자.

```
> "설령 소라타가 나나미를 좋아한다고 해도, 난 소라타가 좋아."
>
>> 이재원이 생일선물로 사준, --- <cite> 사쿠라장의 애완그녀 7 </cite>
```
> "설령 소라타가 나나미를 좋아한다고 해도, 난 소라타가 좋아."
>
>> 이재원이 생일선물로 사준, --- <cite> 사쿠라장의 애완그녀 7 </cite>
<hr>

## 리스트
### Ordered Lists
```
1. 순서가
2. 있는
3. 리스트
    1. 중간에           # 4칸 스페이스 or 2 tab
    2. 항목을
    3. 더 넣어도
4. 된다!!
```
1. 순서가
2. 있는
3. 리스트
    1. 중간에
    2. 항목을
    3. 더 넣어도
4. 된다!!

### Unordered Lists
```
- 이렇게 쓰나
* 저렇게 쓰나
+ 전부 다 똑같이 나온다
  - 물론 항목을 더 넣을 수 있다.      # 2칸 스테이스 or 1 tab
  - 순서가 없는 리스트!
```
- 이렇게 쓰나
* 저렇게 쓰나
+ 전부 다 똑같이 나온다
  - 물론 항목을 더 넣을 수도 있다.
  - 순서가 없는 리스트!
<hr>

## 체크 리스트
```
- [ ] &nbsp;체크 안 됨
- [x] &nbsp;체크 됨
```
- [ ] &nbsp;체크 안 됨
- [x] &nbsp;체크 됨
<hr>

## 표 그리기
```
<table>
  <thead>         ## 표의 머리
    <tr>
      <th>다음에 만날 곳은?</th>
      <th>잠실</th>
      <th>평촌</th>
      <th>판교</th>
    </tr>
  </thead>
  <tfoot>         ## 표 결과
    <tr>
      <td>Total</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
    </tr>
  </tfoot>
  <tbody>         ## 표 내용
    <tr>
      <td>준성</td>
      <td>*</td>
      <td> </td>
      <td> </td>
    </tr>
    <tr>
      <td>수민</td>
      <td> </td>
      <td>*</td>
      <td> </td>
    </tr>
    <tr>
      <td>재원</td>
      <td> </td>
      <td>*</td>
      <td> </td>
    </tr>
  </tbody>
</table>

```
<table>
  <thead>
    <tr>
      <th>다음에 만날 곳은?</th>
      <th>잠실</th>
      <th>평촌</th>
      <th>판교</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Total</td>
      <td>1</td>
      <td>2</td>
      <td>0</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>준성</td>
      <td>*</td>
      <td> </td>
      <td> </td>
    </tr>
    <tr>
      <td>수민</td>
      <td> </td>
      <td>*</td>
      <td> </td>
    </tr>
    <tr>
      <td>재원</td>
      <td> </td>
      <td>*</td>
      <td> </td>
    </tr>
  </tbody>
</table>

<hr>

## 링크
### 설명 없는 그냥 링크
\<링크 주소\>
```
<https://instagram.com/n_s_ideology>
```
<https://instagram.com/n_s_ideology>

### 설명 있는 링크 주소
\[링크 설명\]\(링크 주소\)
```
[연세대학교의 자랑 20학번 이재원 인스타그램](https://instagram.com/n_s_ideology)
```
[연세대학교의 자랑 20학번 이재원 인스타그램](https://instagram.com/n_s_ideology)

<hr>

## 이미지 삽입
\!\[이미지 이름\]\(이미지 주소\)
```
![이재원 강림](/assets/ww.jpg)
```
![이재원 강림](/assets/ww.jpg)

### 이미지 크기 변경
```
<img src="/assets/ww.jpg" width="200" height="400">
```
<img src="/assets/ww.jpg" width="200" height="400">

### 그림 자체에 링크 걸기
```
[![이미지 이름](이미지 주소)](이동하려는 링크 주소)


또는


<a href="링크 주소"> <img scr="이미지 경로.jpg" width="~" heigth="~"></a> 
```
<a href="https://instagram.com/n_s_ideology"> <img src="/assets/ww.jpg" width="200" height="400"></a>
<hr>

## 토글 리스트 (접기/펼치기)
<u> 식빵맘님의 블로그를 참고했습니다. </u> &nbsp;&nbsp;&nbsp; [바로가기](https://ansohxxn.github.io/blog/markdown/)

```
<details>
<summary>여기를 눌러주세요</summary>
<div markdown="1">

<span style="color:rosybrown;">에헤헤</span>

</div>
</details>
```
<details>
<summary>여기를 눌러주세요</summary>
<div markdown="1">

<span style="color:rosybrown;">에헤헤</span>

</div>
</details>

<hr>

## 버튼
```
[맨 위로](#){: .btn .btn--primary }
```
[맨 위로](#){: .btn .btn--primary }

<hr>
