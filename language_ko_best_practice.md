---
title: 쿠버네티스 한글화 모범 사례
content_type: concept
---
<!-- overview -->

이 문서는 쿠버네티스 공식 문서를 한국어로 번역할 때 흔히 나타날 수 있는 사례와 그에 대한 권장 예시를 정리한 것이다.
여러 기여자와 리뷰어들이 함께 살펴본 내용을 모아 정리했으며, 새로운 기여자들도 한눈에 참고할 수 있는 가이드를 확인할 수 있도록 작성했다.

아래 항목들은 실제 리뷰에서 발췌한 예시, 설명, 그리고 참고할 수 있는 리뷰 링크로 구성되어 있다.
한글화에 기여하는 누구나 참고하고, 필요하면 업데이트할 수 있다.

<!-- body -->

## 카테고리

보다 빠른 이해를 위해 모범 사례를 카테고리로 구분한다. 필요 시 추가할 수 있다

| 구분     | 설명                                         |
|----------|----------------------------------------------|
| 이슈     | 한글화 팀 내에서 진행된 논의 및 이슈          |
| 언어     | 한국어 문체 및 표현 관련 사항                 |
| 원문     | 영어 원문 유지 관련                          |
| 용어     | 주요 용어에 대한 번역 방식                    |
| 프로세스 | 기여 프로세스 관련                           |
| 형식     | 문서 형식 관련 규칙                          |



## 예시 탬플릿

```md
### 가이드
[(카테고리)] (내용 작성)

### 예시
* 해당하는 경우에만 작성
**영어 원문**
(내용 작성)
**권장 번역**
(내용 작성)

### 설명
(내용 작성)

### 참고 링크
(링크)

---
```

## 기여 지침

- 새로운 항목을 작성할 때는 위의 예시 템플릿을 따른다.
- 추가되는 사례는 반드시 한글화 팀 내 논의나 리뷰어의 검토 등 근거가 확인된 내용이어야 한다.

## 모범 사례
### 가이드
[프로세스] 리뷰 반영 중에는 amend/squash 대신 추가 커밋을 작성한다.

### 예시

### 설명
- 기여자가 리뷰 반영 과정에서 amend/squash 후 force-push를 하게 되면, 기존 리뷰 코멘트가 파일 뷰 라인에 유지되지 않는 문제가 발생한다.
- 그 결과, 리뷰어가 코멘트 위치를 다시 찾아가며 확인해야 하는 어려움이 있다.
- 따라서 **리뷰 도중에는 커밋을 누적**하여 변경 의도를 투명하게 보여 주고, **최종 승인 직전**에만 정리(squash)하는 것이 바람직하다.

### 참고 링크
- https://github.com/kubernetes/website/pull/51845#issuecomment-3213296290

---

### 가이드
[원문] 가급적 원문을 준수한다.

### 예시
```md
**영어 원문**
If you want to use minikube again to learn more about Kubernetes, you don't need to delete it.

**권장 번역**
쿠버네티스를 더 배우기 위해 minikube를 다시 사용할 계획이라면, 굳이 삭제하지 않아도 된다.
```
### 설명
-  한글화 가이드에서는 가급적 원문을 준수하면서 자연스럽게 번역하는 것을 원칙으로 한다.
-  심지어 영어 원문에 오류가 있다 하더라도 임의로 수정하지 않고 원문을 따른다.
-  원문에 포함되지 않는 내용은 추가하지 않는다.
-  보기 좋도록 토글 등을 사용해 수정하지 않는다.

### 참고 링크
- https://github.com/kubernetes/website/pull/51845#discussion_r2265583071
- https://github.com/kubernetes/website/pull/51871#discussion_r2292977719
- https://github.com/kubernetes/website/pull/51856#discussion_r2265640994
- https://github.com/kubernetes/website/pull/51864#discussion_r2265211848

---

### 가이드
[원문] 영어 원문과 유사하게 개행하여 총 라인 수를 같게 한다.

### 예시
```md
**영어 원문**
Create a namespace so that the resources you create in this exercise are
isolated from the rest of your cluster.

**권장 번역**
이 실습에서 생성하는 리소스가 클러스터의 다른 리소스와
격리되도록 네임스페이스를 생성한다.
```

### 설명
- 한글화 된 문서의 유지보수 및 리뷰의 효율을 위해 한글화 팀에서 유지하고 있는 규칙이다.
- 영어와 한국어의 문장 구조 차이로 인해 개행 위치가 애매한 경우에도 적절히 판단하여 개행한다.
- 결과적으로 영어 원문과 한국어 번역의 총 라인 수가 같아야 한다.

### 참고 링크
- https://github.com/kubernetes/website/pull/51858#discussion_r2281064968
- https://github.com/kubernetes/website/pull/51856#discussion_r2265622453
- https://github.com/kubernetes/website/pull/51864#discussion_r2265212235
