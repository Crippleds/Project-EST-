# URL 기반 게시글 관리 프로그램

이 프로그램은 URL을 포함한 게시글을 관리할 수 있는 Java 콘솔 애플리케이션입니다. MVC (Model-View-Controller) 아키텍처 패턴을 사용하여 구현되었으며, 프로그램 실행 중에만 게시글이 유지되는 임시 저장 시스템입니다.

## 목차
1. [프로젝트 구조](#프로젝트-구조)
2. [기능](#기능)
3. [설치 방법](#설치-방법)
4. [사용 방법](#사용-방법)
5. [기술 스택](#기술-스택)
6. [주요 컴포넌트](#주요-컴포넌트)

## 프로젝트 구조
```
src/
├── model/
│   ├── Post.java
│   └── PostRepository.java
├── view/
│   └── PostView.java
├── controller/
│   └── PostController.java
└── Main.java
```

## 기능
- 게시글 작성 (제목, 내용, URL 포함)
- 게시글 삭제
- 게시글 목록 조회
- 프로그램 종료 시 데이터 자동 삭제

## 설치 방법

### 요구사항
- Java Development Kit (JDK) 8 이상
- Java IDE (Eclipse, IntelliJ IDEA 등) 또는 텍스트 에디터

### 설치 단계
1. 프로젝트 클론 또는 다운로드
```bash
git clone [repository-url]
```

2. 프로젝트 디렉토리로 이동
```bash
cd [project-directory]
```

3. Java 파일 컴파일
```bash
javac Main.java
```

4. 프로그램 실행
```bash
java Main
```

## 사용 방법

### 메인 메뉴
프로그램을 실행하면 다음과 같은 메뉴가 표시됩니다:
```
1. Add Post
2. Delete Post
3. List Posts
4. Exit
```

### 게시글 작성
1. 메인 메뉴에서 `1` 선택
2. 제목 입력
3. 내용 입력
4. URL 입력 (유효한 URL 형식이어야 함)

### 게시글 삭제
1. 메인 메뉴에서 `2` 선택
2. 삭제할 게시글의 인덱스 번호 입력

### 게시글 목록 조회
- 메인 메뉴에서 `3` 선택

### 프로그램 종료
- 메인 메뉴에서 `4` 선택

## 기술 스택
- Java
- MVC 아키텍처 패턴
- Java Collection Framework
- Java URL 클래스

## 주요 컴포넌트

### Model
- **Post.java**: 게시글 데이터 구조 정의
  - 제목, 내용, URL 정보 저장
  - getter 메서드와 toString 메서드 제공

- **PostRepository.java**: 게시글 데이터 관리
  - 게시글 추가, 삭제, 조회 기능
  - ArrayList를 사용한 데이터 저장

### View
- **PostView.java**: 사용자 인터페이스 담당
  - 메뉴 표시
  - 사용자 입력 처리
  - 결과 출력
  - 에러 메시지 표시

### Controller
- **PostController.java**: 비즈니스 로직 처리
  - Model과 View 연동
  - 사용자 입력에 따른 작업 처리
  - 예외 처리

## 주의사항
- 프로그램은 실행 중에만 데이터를 유지합니다.
- 프로그램 종료 시 모든 게시글이 삭제됩니다.
- URL은 유효한 형식이어야 합니다.
