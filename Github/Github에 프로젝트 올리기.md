# Github에 프로젝트 올리기

Github에 가입이 되어있는 상태라는 가정 하에 방법을 작성하겠습니다. 

---

### **1. Git(깃)을 설치** OS에 맞는 것으로 설치해주면 됩니다.

윈도우라면, 설정>시스템>정보>'시스템 종류'에서 32bit인지 64bit인지 확인 가능!

 {: target="https://git-scm.com/downloads"}

### **2. github에서 new repository(새 저장소)를 생성해줍니다.**

**repository**는 프로젝트별로 관리할 수 있는 box라고 생각하면 됩니다.

오른쪽 상단에 '+'표시>New repository 클릭 → repository name, description 입력 하고 버튼 클릭

![1](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/1.jpg)

![2](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/2.jpg)

### **3. 생성된 repository의 저장소를 복사합니다.**

HTTPS/SSH 오른쪽의 주소를 복사해둡니다.

![3](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/3.jpg)

### **4. 로컬로 돌아와서, 프로젝트를 업로드하고싶은 폴더 우클릭> Git Bash Here**

![4](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/4.jpg)

### **5. Git cmd창이 뜨면, 초기 설정을 진행해줍니다.**

" "내부에 본인의 깃헙 user name이랑 email 입력해주면 됩니다. 

![5](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/5.jpg)

### **6.**

![6](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/6.jpg)

![9](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/9.png)

```
**1)**.git 파일 생성
$ git init

**2)**선택한 프로젝트 폴더 내의 **모든** 파일 버전 관리 
(만약, 특정파일만 하고 싶다면 git add a.py 형식으로 써도 무방하다.)
$ git add .

**3)**버전 관리 tracking. 업그레이드 된 것은 untracking이라고 빨간 글씨로 뜸
$ git status

**4)**커밋
$ git commit -m "주석"
```

### **7.**

![7](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/7.jpg)

```
**1)**$ git remote add origin 복사했던 repository 주소

**2)**github에 push(업로드)
$ git push -u origin master

※error: remote origin already exists.
다음과 같은 에러메시지가 뜰 경우
$ git remote rm origin 입력 후 (삭제)
$ git remote add origin 복사했던 repository 주소 재입력
```

### **8. 프로젝트 업로드 완료**

![8](https://github.com/hanyellding/TIL/blob/main/Github/Github%EC%97%90%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%EC%98%AC%EB%A6%AC%EA%B8%B0_images/8.jpg)

출처: [https://2hyes.tistory.com/91](https://2hyes.tistory.com/91)
