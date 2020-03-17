Markdown 사용법
============
# 1. Markdown에 관해서
## 1.1. Markdown이란?
마크다운(markdown)은 일반 텍스트 문서의 양식을 편집하는 문법이다. README 파일이나 온라인 문서, 혹은 일반 텍스트 편집기로 문서 양식을 편집할 때 쓰인다. 마크다운을 이용해 작성된 문서는 쉽게 HTML 등 다른 문서형태로 변환이 가능하다.   
## 1.2. Markdown의 장/단점
### 1.2.1. 장점
```
1. 간결하다.
2. 별도의 도구없이 작성가능하다.
3. 다양한 형태로 변환이 가능하다.
3. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
4. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
5. 지원하는 프로그램과 플랫폼이 다양하다.
```
### 1.2.2. 단점
```
1. 표준이 없다.
2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
3. 모든 HTML 마크업을 대신하지 못한다.
```
# 2. Markdown 사용법
## 2.1. 제목
#을 붙일수록 크기가 줄어든다. `h1`부터 `h6`까지만 가능하다.   
ex)
# 제목 1
## 제목 2
### 제목 3
#### 제목 4
##### 제목 5
###### 제목 6
```
# 제목 1
## 제목 2
### 제목 3
#### 제목 4
##### 제목 5
###### 제목 6
```
   
## 2.2. 강조
* 이탤릭체: `*`나 `_` 1개로 강조하고 싶은 부분을 감싸면 된다.   
ex) *code*, _code_
```
*code*
_code_
```
* 볼드체: `*`나 `_` 2개로 강조하고 싶은 부분을 감싸면 된다.   
ex) **code**, __code__
```
**code**
__code__
```
* 취소선: `~`2개로 강조하고 싶은 부분을 감싸면 된다.   
ex) ~~code~~
```
~~code~~
```

## 2.3. 목록
* 순서있는 목록
순서 있는 목록은 숫자와 점을 사용한다.   
ex)
1. 첫 번째
2. 두 번째
3. 세 번째
```
1. 첫 번째
2. 두 번째
3. 세 번째
```
현재까지는 어떤 숫자를 입력하든지 내림차순으로 숫자가 바뀐다.   
ex)
1. 첫 번째
3. 세 번째
2. 두 번째
```
1. 첫 번째
3. 세 번째
2. 두 번째
```

* 순서없는 목록
`*`, `+`, `-` 3가지 모두 사용가능하다. 혼용도 가능하다.   
ex)
* 목록 1
    * 목록 2
        * 목록 3
+ 목록 1
    + 목록 2
        + 목록 3
- 목록 1
    - 목록 2
        - 목록 3
* 목록 1
    + 목록 2
        - 목록 3
```
* 목록 1
    * 목록 2
        * 목록 3
+ 목록 1
    + 목록 2
        + 목록 3
- 목록 1
    - 목록 2
        - 목록 3
* 목록 1
    + 목록 2
        - 목록 3
```

## 2.4. BlockQuote
이메일에서 사용하는 `>` 블럭인용문자를 이용한다.   
ex)
> 첫 번째 BlockQuote.
>    > 두 번째 BlockQuote.
>    >    > 세 번째 BlockQuote.
```
> 첫 번째 BlockQuote.
>    > 두 번째 BlockQuote.
>    >    > 세 번째 BlockQuote.
```
BlockQuote안에 다른 마크다운 요소를 포함할 수 있다.   
ex)
> ```code```
>    > * 목록 마크다운 사용
>    >    > **볼드체 사용**

```
> ```code```
>    > * 목록 마크다운 사용
>    >    > **볼드체 사용**
```

## 2.5. 코드
4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.
### 2.5.1. 들여쓰기
한 줄을 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생한다.   
ex)   
Hello world!   
    Hello world!   
Hello world!
```
Hello world!
    Hello world!
Hello world!
```
   
ex)   
Hello world!

    Hello world!

Hello world!
```
Hello world!

    Hello world!

Hello world!
```
### 2.5.2. 코드블럭
코드블럭은 2가지 방식이 있다.
* `<pre><code>{code}</code></pre>`   
ex)
<pre>
<code>
num = int(input())
print(num)
</code>
</pre>
```
<pre>
<code>
num = int(input())
print(num)
</code>
</pre>
```
* 코드블록코드\`\`\`code\`\`\`을 이용하는 방법   
ex)
```
num = int(input())
print(num)

```
<pre>
<code>
```
num = int(input())
print(num)
```
</code>
</pre>

## 2.6. 수평선
아래의 코드는 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 **페이지 나누기** 용도로 많이 사용한다.   
ex)
* * *
***
*****
- - -
------------------------------
```
* * *
***
*****
- - -
------------------------------
```

## 2.7. 링크
* 참조링크   
ex)

Link: [Naver][naverlink]

[naverlink]: https://www.naver.com "naver"
```
// form
[link keyword][id]

[id]: URL "Optional Title"

// code
Link: [Naver][naverlink]

[naverlink]: https://www.naver.com "naver"
```

* 외부링크   
ex)
Link: [Naver](https://www.naver.com, "naver link")
```
사용문법: [Title](link)
적용예: [Naver](https://www.naver.com, "naver link")
```
* 자동연결   
ex)

외부링크: <https://www.naver.com/>
이메일링크: <kangtak6291@naver.com>

```
일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

외부링크: <https://www.naver.com/>
이메일링크: <kangtak6291@naver.com>
```
## 2.8. 이미지
앞에 !와 [대체텍스트]를 붙인다.   
ex)
![토토로](http://blog.jinbo.net/attach/615/200937431.jpg)
```
![토토로](http://blog.jinbo.net/attach/615/200937431.jpg)
```
사이즈 조절 기능은 없기 때문에 ```<img width="" height=""></img>```를 이용한다.   
ex)
<img src="http://blog.jinbo.net/attach/615/200937431.jpg" width="450px" height="300px"></img>
```
<img src="http://blog.jinbo.net/attach/615/200937431.jpg" width="450px" height="300px"></img>
```
* 이미지 링크
꺾쇠[]안에 이미지를 넣고 뒤 괄호 ()안에 이동할 주소 링크를 넣는다.   
ex) [![갈매기](http://www.futurekorea.co.kr/news/photo/200604/12476_8716_5000.JPG)](https://namu.wiki/w/%EA%B0%88%EB%A7%A4%EA%B8%B0)
```
[![갈매기](http://www.futurekorea.co.kr/news/photo/200604/12476_8716_5000.JPG)](https://namu.wiki/w/%EA%B0%88%EB%A7%A4%EA%B8%B0)
```

## 2.9. 줄바꿈
3칸 이상 띄어쓰기를 하면 줄이 바뀐다.   
ex)
* 줄 바꿈을 하려면 줄 바꿈을 하고 싶은 위치에서    3칸이상을 띄어쓰기해야 한다.
```
* 줄 바꿈을 하려면 줄 바꿈을 하고 싶은 위치에서    3칸이상을 띄어쓰기해야 한다.
```

## 2.10. 테이블
헤더 셀을 구분할 때 3개 이상의 -(hyphen/dash) 기호를 쓴다.
헤더 셀을 구분하면서 :(Colons) 기호로 셀(열/칸) 안에 내용을 정렬할 수 있다.
가장 좌측과 가장 우측에 있는 |(vertical bar) 기호는 생략 가능하다.   
ex)
| 학번 | 이름 | 전화번호 |
|---|:---:|---:|
| `2012104089` | 트와이스 | `01012341234` |
| `2015104029` | 아이즈원 | '01011112222' |
| `2019105029` | 소녀시대 | '01033334444' |

```
 학번 | 이름 | 전화번호 
---|:---:|---:
 `2012104089` | 트와이스 | `01012341234` 
 `2015104029` | 아이즈원 | '01011112222' 
 `2019105029` | 소녀시대 | '01033334444' 
```
# 3. 참고문서
* https://gist.github.com/ihoneymon/652be052a0727ad59601
* https://velog.io/@bboding/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4MarkDown-%EC%82%AC%EC%9A%A9%EB%B2%95
* https://ko.wikipedia.org/wiki/%EB%A7%88%ED%81%AC%EB%8B%A4%EC%9A%B4