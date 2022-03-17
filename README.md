# Bootstrap template Clone coding w/ HTML&CSS

## 담당 section

- eun-ipsam
- skills
- services

![127 0 0 1_5500_arsha html](https://user-images.githubusercontent.com/93528293/155923330-549004c8-2d60-4dd7-8d2a-6a90442d8391.png)
![127 0 0 1_5500_arsha html (1)](https://user-images.githubusercontent.com/93528293/155923524-3a6e2dfa-6f70-40f9-aa3f-8c67aec6e4d2.png)
![127 0 0 1_5500_arsha html (2)](https://user-images.githubusercontent.com/93528293/155923530-5546ff95-94a3-4ec9-86eb-076b3d350f2d.png)

<div align="right">

[click](https://unhyif.github.io/piro16_arsha/arsha.html)

</div>

## TIL

#### 220101

- CSS animations
- `:target` pseudo-class
- Created accordion & card components

https://velog.io/@unhyif/Bootstrap-template-Clone-coding

#### 문제 해결 기록

##### Accordion

`input[type="checkbox"]` 또는 `input[type="radio"]`를 사용하여, `label`인 title이 클릭되면 `input:checked`와 sibling인 content가 display 되는 방식으로 아코디언을 구현하려 했었다.<br>
하지만 다른 아코디언이 open 되면 기존 아코디언이 자동적으로 close 되도록 해야 했기 때문에, 여러 항목의 선택이 가능한 `checkbox`는 적합하지 않았다.<br>
더불어, 아코디언이 open 되어 있을 때 title을 재클릭하면 close 되어야 했기에, `radio`는 현재 선택된 것을 재클릭으로 해제시킬 수 없다는 점에서 사용할 수 없었다.

- 해결 방안: `:target` pseudo-class를 통해 해결할 수 있었다.<br>
  우선 `a` 태그로 open용 title과 close용 title 들을 만들고, open용 title 클릭 시 `href` 속성을 통해 그와 sibling인 `span`을 target 시킬 수 있었다. 그리고나서 `span:target`과 sibling인 content를 display 시켜주었다.<br>
  그리고, close용 title 또는 다른 open용 title을 클릭하면 다른 `span`이 target 되도록 함으로써, 위에서 언급한 기능들을 가진 아코디언을 구현해낼 수 있었다.

---

## Updates

#### 220228

- Removed unused codes
- Set the height of accordion content automatically
- Simplified CSS selectors
