# personal-study

Java와 Kotlin의 언어 기능을 개인적으로 학습하기 위한 저장소입니다.

## 학습 목적

Java의 함수형 인터페이스/람다/스트림과 Kotlin의 제네릭/컬렉션/데이터 클래스 등
언어 차원의 기능을 작은 예제로 실습합니다.

## 사용 기술

- Java 17
- Kotlin 1.9.23 (JVM target 17)
- Gradle (Kotlin DSL)
- 의존성: `kotlin-reflect`

> `build.gradle.kts`에 Spring Boot 플러그인(3.2.5)이 선언되어 있으나, 실제로 사용하는 Spring
> 스타터 의존성은 없습니다. 코드 내용상 Spring 프로젝트가 아닌 **순수 Java/Kotlin 언어 학습**
> 프로젝트입니다.

## 다룬 주제 (코드 근거)

### Java
- **람다 / 함수형 인터페이스** (`com.personal.study.lambda`)
  - `MyFunctionalInterface`, `MyFunctionalInterface2`, `MyFunctionalInterface3` 및
    각 사용 예제(`...Example`) — 사용자 정의 함수형 인터페이스와 람다 표현식 실습.
- **Iterator vs Stream** (`com.personal.study.stream.IteratorAndStream`)
  - `Iterator`로 순회하는 방식과 `stream().forEach()`로 순회하는 방식을 비교.

### Kotlin
- **제네릭** (`com.personal.study.generic.GenericStudy`)
  - 제네릭 함수 `<T> printArray(arr: Array<T>)` 실습.
- **컬렉션 / 데이터 클래스** (`com.personal.study.Study1`)
  - `data class Person`, `map`/`average`/`groupBy` 등 컬렉션 고차 함수 실습.

## 프로젝트 구조

```
personal-study/
├── build.gradle.kts
├── settings.gradle.kts
└── src/main
    ├── java/com/personal/study
    │   ├── generic/GenericStudy.kt          # Kotlin 제네릭 (java 디렉터리 하위)
    │   ├── lambda/                          # Java 람다 / 함수형 인터페이스
    │   └── stream/IteratorAndStream.java    # Iterator vs Stream
    └── kotlin/com/personal/study
        └── Study1.kt                        # Kotlin 컬렉션 / 데이터 클래스
```

> 참고: `GenericStudy.kt`는 Kotlin 파일이지만 `src/main/java` 경로 아래에 위치합니다(현재 구조 그대로 기재).
