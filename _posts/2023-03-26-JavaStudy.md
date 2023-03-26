---
published: true
title: "[JAVA를 자바라] 노트정리"
---

# [JAVA를 자바라] 2주차 ✏️

# 2023-03-19 2주차 강의 노트 정리

## 📌남궁성의 자바의 정석 (7-12강)

### 개념정리
**Eclipse, an Integrated Development Environment (IDE)**
이클립스는 자바 개발을 위한 필수 통합 개발 환경이다.
기본 화면 구성은 다음과 같이 이루어져 있다.<br/>
<img width="770" alt="이클립스화면" src="https://user-images.githubusercontent.com/114560119/227774582-a34ccaa3-7b93-4829-93ec-bd20d3227b15.png"><br/>
<u>Perspective</u> - view와 editor를 포함한 이클립스의 윈도우. 나에게 맞게 레이아웃을 조절할 수 있다.<br/>
<u>View</u> - package explorer 같은 기능을 담고 있는 창.<br/>
<u>Editor</u> - 파일의 내용물을 담은 창. 자바 코드 혹은 쿼리문을 수정/개발 할 수 있다.<br/>

**장점**
- 가장 큰 장점으로는 오픈소스 개발환경이라 큰 커뮤니티가 형성 되어있다는 것을 꼽을 수 있다.
- 자동 컴파일이 됨 (build automatically 기능. 껐다 킬수있삼.)

### 이클립스로 개발하기
**자바 프로젝트 생성하기**
1. 프로젝트를 생성한다. 메뉴 File>New>Java Project
2. 클래스를 생성한다. 프로젝트 이름 위에서 우클릭>New>Class
3. 소스파일의 작성 후 저장 (자동 컴파일됨)
4. 실행. 메뉴 Run>Run

**Build 관련 메뉴 설명** </br>
Build란 소스 파일 (.java)로부터 프로그램을 만들어 내는 전 과정
- Build All: workspace의 모든 프로젝트 빌드
- Build Project: 현재 프로젝트를 빌드 (변경된 소스 파일만 새로 컴파일)
- Clean: 이전 빌드의 정보를 모두 삭제(모든 소스 파일을 새로 컴파일)
- Build Automatically: 소스 파일을 변경 후 저장할 때마다 자동 컴파일

**소스 파일들 import&export 하기**
1. 패키지 익스플로럴창에서 리소스를 임포트할 폴더 경로 우클릭
2. import를 클릭후에 File System을 선택. 
3. Next 클릭후에 

### 이클립스 개꿀팁 단축키
제일 마음에 든 강의다.
몇몇개의 단축키는 visual studio code에서도 사용이 가능하다. 진정한 개꿀단축키가 아닐 수 없다!
  > ctrl+shift+L 단축키 전체 목록보기 </br>
  > ctrl+ +,- 폰트 크기 증가/감소 </br>
  > ctrl+D 한 줄 삭제 </br>
  > ctrl+alt+shift+down 행단위 복사</br>
  > alt+Shift+A 멀티컬럼 편집</br>
  > alt+up, down 행단위 이동</br>
  > ctrl+i 자동 들여쓰기</br>
  > ctrl+/ 주석(토글)</br>

### 변수란(Variable)?
변수란 하나의 값(data)을 저장할 수 있는 메모리 공간(램,RAM)이다. 
메모리에 값을 저장하려면, 변수를 선언해야하 한다. 

**변수를 선언하는 방법:**
- 변수타입 변수이름; 
- 아래 예제 코드에서 변수를 선언시 age라는 이름의 저장공간이 생성된다.

**변수에 값 저장하기**
- 그냥 변수 이름 적음 됨 ㅋ. 별거없다.

```java
public class Hello {
    public static void main(String[] args){
         int i=10;
         age =25;
         int age = 25;
         System.out.println(age);
    }
}
```
위의 코드를 작성시 콘솔에 25가 찍힌다.

**변수의 종류**
1. 클래스 변수 (Class Variable)
2. 인스턴스 변수 (Instance Variable)
3. 지역 변수 (Local Variable) - 반드시 초기화 해줘야 함. 그렇지 않으면 컴파일 할때 에러발생. 

**변수의 타입**
1. 변수의 타입은 저장할 값의 타입에 의해 결정된다. 정수면 정수. 실수면 실수끼리~
2. 따라서 저장할 값의 타입과 일치하는 타입으로 변수를 선언해야함

**값(Data)의 타입**
1. 문자: char
2. 숫자
  - 정수: byte, short, int, long
  - 실수: float, double
3. 논리: boolean (true or false)


### 한줄 평
개꿀팁으로 업무시간 단축효과를 기대 해 본다.
개꿀팁으로 업무시간 단축효과를 기대 해 본다.
개꿀팁으로 업무시간 단축효과를 기대 해 본다.

## 📌노마드 코딩 - 실전형 리액트 Hooks (#1 UseState)

### useState
상태(state)를 관리 할 수 있는 훅이다. useState hook을 호출하면, 구조 분해 할당을 통해 반환된 값을 사용할 수 있다.
두가지 요소를 필수로 필요로 하는데, 첫 번째 요소인 state를 통해 동적으로 관리하고자 하는 값을 할당하고, 두 번째 요소인 setState function을 통해 state를 업데이트할 수 있다.

**rules**
1. 기본 Hooks의 법칙은 그대로 따른다. 최상위에서 호출 해야 하고,
2. 또한 반복문, 조건문, 중첩된 함수 내에서는 Hook을 호출하면 안됨. 

### useInput
기본적으로 input을 업데이트 하는 훅이다. 초기값(initialValue)을  셋팅해줘야 함. 

```js
const useInput = (initialValue) => {
  const [value, setValue] = useState(initialValue);
  return {value};
}
const App = () => {
  const name = useInput("Mr.");
  return (
    <div className="App'>
      <h1>Hello</h1>
      <input placeholder="Name" value={name.value} />
     </div>
  );
};
```
useInput는 value를 리턴하고 name은 value의 값을 가지고 value는 name.value의 값을 가지게 됩니다.

### 한줄 평
훅은 짱짱이다. 

## 잡담
일 시작하고 첫 주, 어버버 하고 있던 사이에 동료분들이 도와주셔서 이클립스에 import한 프로젝트들을 어떻게 하는지 다시 되새김질 할 수 있었다. 
