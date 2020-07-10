
![](https://images.velog.io/images/doomchit_3/post/7594b4c3-9429-4e70-a2d5-045db4f37aad/image.png)

# 🧣 List

## ① 순서없는 목록 (Unordered List)
- 기본 순서없는 목록
```

      <ul>
      <li>cat</li>
      <li>dog</li>
      <li>rabbit</li>
      </ul>
```
## ② 순서있는 목록 (Ordered List)
- 기본 순서있는 목록
```
      <ol>
      <li>cat</li>
      <li>dog</li>
      <li>rabbit</li>
      </ol>
```
- `type 어트리뷰트` 를 사용하여 순서를 나타내는 문자를 지정할 수 있다.

```
      <ol type="I">
        <li value="2">cat</li>
        <li value="4">dog</li>
        <li>rabbit</li>
      </ol>
```
- `start 어트리뷰트` 로 리스트의 시작값을 지정할 수 있다.
```
      <ol start="3">
        <li>cat</li>
        <li>dog</li>
        <li>rabbit</li>
      </ol>
```
- `reversed 어트리뷰트` 를 지정하면 리스트의 순서값을 역으로 표현한다.

```
      <ol reversed>
        <li>cat</li>
        <li>dog</li>
        <li>rabbit</li>
      </ol>
```


### ③ 중첩 목록
- 목록을 중첩하여 사용할 수 있다.
```
 <h2>중첩목록</h2>
    <ul>
      <li>cat</li>
      <li>dog</li>
        <ol>
          <li>snoop dog</li>
          <li>crazy dog</li>
        </ol>
      </li>
      <li>rabbit</li>
    </ul>
```


<br/>
<br/>

# 🧮 Table
`표(table)` 를 만들 때 사용하는 태그이다. 과거에는 테이블 태그를 사용하여 레이아웃을 구성하기도 하였으나 모던 웹에서는 주로 공간 분할 태그인 div 태그를 사용하여 레이아웃을 구성한다.

- table
표를 감싸는 태그
- tr
표 내부의 행 (table row)
- th	
행 내부의 제목 셀 (table heading)
- td
행 내부의 일반 셀 (table data)

![](https://images.velog.io/images/doomchit_3/post/e1ea25aa-4aa0-4e12-bc64-19c17107c14b/image.png)


테이블 태그의 어트리뷰트는 아래와 같다.

- border
표 테두리 두께 지정. (CSS border property를 사용하는 것이 더 나은 방법이다.)
- rowspan
해당 셀이 점유하는 행의 수 지정
- colspan
해당 셀이 점유하는 열의 수 지정

```
<h2>2개의 culumn을 span</h2>
    <table>
      <tr>
        <th>Name</th>
        <th colspan="2">Telephone</th>
      </tr>
      <tr>
        <td>최준영</td>
        <td>010 **** 8137</td>
        <td>010 **** 8137</td>
      </tr>
    </table>

    <h2>2개의 row를 span</h2>
    <table>
      <tr>
        <th>Name:</th>
        <td>최준영</td>
      </tr>
      <tr>
        <th rowspan="2">Telephone:</th>
        <td>010 **** 8137</td>
      </tr>
      <tr>
        <td>010 **** 8137</td>
      </tr>
    </table>
```

<br/>
<br/>

# 참고📚
[mozilla](https://developer.mozilla.org/ko/docs/Web/HTML)
[poiemaweb](https://poiemaweb.com/html5-semantic-web)