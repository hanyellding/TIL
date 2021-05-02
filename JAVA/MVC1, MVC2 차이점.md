# MVC1, MVC2 차이점

## **MVC 패턴은 무엇인가?**

---

MVC 패턴은 소프트웨어 공학에서 사용하는 디자인 패턴 중 하나로 Model, View, Controller의 앞 글자를 따서 만든 디자인 패턴이다.

---

**Model**      : 백그라운드에서 동작하며, 사용자가 원하는 데이터나 정보를 제공한다.

**View**        : 사용자의 요청을 화면으로 출력한다.

**Controller** : 사용자의 요청을 처리하고, 그 요청에 따른 전체적인 흐름을 제어한다.

---

사용자는 **얻고자 하는 정보나 기능**을 **컨트롤러**에게 요청한다.

**컨트롤러**는 사용자의 요청을 수신하고 그에 맞는 **비즈니스 로직을 수행**한다.

비즈니스 로직을 수행하면서 **컨트롤러**는 필요에 따라 **모델을 호출하여 데이터를 요청**한다.

요청을 모두 처리하면 **뷰**를 통해 사용자가 원하는 정보를 **시각적으로 보여준다**. (화면으로 출력)

MVC 패턴은 크게 MVC 모델1, MVC 모델2로 나뉜다.

### **MVC 모델 1**

---

MVC 모델 1은 뷰와 컨트롤러의 역할이 합쳐져 있다.

흔히 웹 개발을 하면 Jsp가 뷰 역할을 하는데, MVC 1에서 JSP는 뷰와 컨트롤러의 역할을 모두 감당한다.

![https://blog.kakaocdn.net/dn/I1UUx/btqEZ0IhZ6O/qzvwssYAAkEltNqYd3Kpik/img.png](https://blog.kakaocdn.net/dn/I1UUx/btqEZ0IhZ6O/qzvwssYAAkEltNqYd3Kpik/img.png)

위와 같이 JSP가 뷰와 컨트롤러 역할을 모두 수행하면, JSP에 Java 코드와 HTML, CSS 등의 코드가 섞여 있어, 소스가 복잡해지고 읽기가 어려워져 유지보수가 힘들어 진다.

하지만 상대적으로 설계가 간단하여 개발 속도가 빠르고 작은 프로젝트에 알맞다.

### **MVC 모델 2**

---

MVC 모델 2는 모델 1에서 유지보수가 힘들다는 단점을 보완하기 위해 나온 모델이다.

기존에 뷰와 컨트롤러의 역할을 모두 수행하던 JSP는 뷰의 역할만 하게 하고, 대신 컨트롤러 역할을 Servlet이 수행한다.

모델은 기존 MVC 1 방식과 동일하다.

![https://blog.kakaocdn.net/dn/bgbhsb/btqE0BOnWqs/GhoRjVi90P1dYSBjRHSo91/img.png](https://blog.kakaocdn.net/dn/bgbhsb/btqE0BOnWqs/GhoRjVi90P1dYSBjRHSo91/img.png)

MVC 1에서는 JSP가 사용자의 호출을 받아줬는데 MVC 2에서는 컨트롤러 역할을 수행하는 Servlet이 요청을 받아준다.

Servlet이 비즈니스 로직을 수행하며 모델을 호출하여 데이터를 요청하며, 최종적으로 뷰 역할인 JSP를 제어하여 화면을 출력한다.

MVC 2로 개발하게 되면 HTML과 Java 코드가 분리되어 확장에 용이하고 유지보수가 수월해진다.

JSP는 Java 코드를 안 쓰는 대신 JSTL을 사용하여 결과 화면을 보여준다.

하지만 초기 설계단계에 비용이 많이 들어 개발 시간이 오래 걸린다는 단점이 있다.

### 요약

**MVC 패턴**은 **Model, View, Controller**를 사용하는 디자인 패턴 중 하나이다.

MVC 패턴은 **MVC 모델 1**과 **MVC 모델 2**가 있다.

**MVC 1**은 설계가 간단하여 **작은 프로젝트**에 어울리며, **개발 속도가 빠른** 대신 소스가 복잡해져 **유지보수가 어렵다**.

**MVC 2**는 소스가 복잡하다는 MVC 1의 단점을 보완하기 위해 탄생했으며, 

비교적 **큰 프로젝트**에 어울리고

설계 단계에서 비용이 많이 들어 **개발 속도가 느리다**는 단점이 있지만, 

**확장에 용이**하고 **유지보수가 수월**하다는 것은 매우 큰 메리트가 될 수 있다.

출처 : https://onejuny.tistory.com/entry/JavaJsp-MVC-1-MVC-2-%EC%B0%A8%EC%9D%B4-%EB%B0%8F-%EC%9E%A5%EB%8B%A8%EC%A0%90
