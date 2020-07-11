
## Description

"앵귤러 마스터북"을 학습하며 배운 내용을 정리합니다.

### 1.9.3 템플릿 변수, 이벤트 바인딩

아래와 같이 템플릿 변수(#titleElt)를 선언하여 변수로 사용할 수 있습니다.
템플릿 변수는 이벤트 바인딩할 때 변수로 넘겨줄 수 있습니다.

``` bash
// titleElt는 HTMLInputElement이기 때문에 컴포넌트에서 값에 접근하기 위해서는 titleElt.value로 접근해야 합니다.
<input name="title" #titleElt>
<button (click)="addTitle(titleElt)">
```

### 1.9.4 HostBinging, a 태그 특징

###### 1) HostBinging
컴포넌트 클래스 내에서 아래와 같이 호스트의 attribute를 설정할 수 있습니다.
```bash
@HostBinding('attr.class') cssClass = 'row';
```
이 예제의 경우, list item 컴포넌트에 class="row" 속성을 주고 싶은데, 직접 selector 태그에 속성을 지정하지 않고 컴포넌트 내에서 위와 같이 설정해줌으로써 부모뷰의 마크업으로부터 캡슐화할 수 있습니다.

###### 2) a 태그 특징
```bash
<a href (click)="voteUp()">
```
자바스크립트는 기본적으로 click 이벤트를 모든 부모 컴포넌트에게 전달하기 때문에, 클릭하게 되면 브라우저가 빈 링크를 따라 가려고 하다가 리로드 되어 의도했던 대로 동작하지 않게 됩니다.
이를 방지하기 위한 방법으로는 이벤트 핸들러가 false를 리턴하게 하는 방법이 있습니다.
