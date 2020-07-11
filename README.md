
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
