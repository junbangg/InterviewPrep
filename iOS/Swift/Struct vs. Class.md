# Swift 
작성일: 2021년 9월 7일

## Struct vs Class
  > 둘중에 뭘 언제 써야하는게 맞을까??

## Struct 과 Class 의 공통점
  - 둘다 속성을 이용해서 값을 저장 할 수 있다
  - 둘다 subscript 를 사용 할 수 있다
  - 둘다 생성자가 있다 
  - 둘다 확장이 가능하다 (extension)
  - 둘다 프로토콜(protocol)을 사용할 수 있다
  - 둘다 제네릭(generic) 을 사용할 수 있다
  
# Class
  - Struct 과는 다르게 상속이 가능하다
  - deinit() 이 가능하다
  - 클래스는 참조형이다
  
# 언제 Struct 를 사용해야될까?
  - Apple에서는 default로 struct 를 사용하라고 한다
  - Simple Data Type (Task, User, Item) 일때 구조체 사용하는게 더 편하다
  - Thread Safety
    - 멀티쓰레드 환경에서는 구조체가 쓰레드 간에 복사가 가능하기 때문에 더 안전하다.
    - 클래스를 멀티쓰레드 환경에서 썼다가는 race condition, deadlock 위험이 있다.
    - 클래스는 쓰레드에 대한 고려를 따로 해서 구현해야된다. 구조체는 기본적으로 thread safety 가 제공됨
  - Struct 에 내용물, 즉 속성들이 대부분 참조 type (String, Int..) 일때는, 클래스말고 구조체로 쌓아서 쓰는게 좋다
  - 상속이 필요없을때
# Struct 를 쓸때의 장점
  - Value type 이라서 코드 다른 곳에서 바뀔 일이 없다
  - 따라서 디버깅도 더 쉬울것 같다.
# Struct 는 언제 써야할까?
  > 애플 가이드라인에서 다음 조건 중 하나 이상에 해단되면 Struct를 사용하라고 한다.
  - 연관된 간단한 값의 집합을 갭슐화 하는 것만이 목적일때
  - 캡슐화된 값이 참조되는 것보다 복사되는 것이 합당할 때
  - 구조체에 저장된 프로퍼티가 값 타입이며 참조되는 것보다 복사되는 것이 합당할 때
  - 상속이 필요없을때
  
  
# 그럼 Class는 언제 써야할까?
  > 클래스는 구조체 이상의 무언가가 필요할때 쓰는게 맞다. 그래서 struct 가 default 고, class 는 쫌 더 특별한 상황에서 쓰이는것 같다
  - 상속이 필요할때
  - deinit 이 필요할때
  - identity가 필요할때.
  - objective-c 와 함께 사용이 필요할때
  - 인스턴스끼리 비교나 복사가 필요 없을때..즉, Window, UIViewController 처럼 한개만 필요하고 복사가 필요 없을때. UIViewController를 보통 새로 만들지, 복사를 하지않는다
  - 인스턴스의 lifetime 이 외부에 의존할때. 파일이나, 데이터베이스랑 연결이 되었을때는 그걸 복사 할 필요가 없지

# 한마디로 정리하자면!?!
  > Class 만 제공해주는 기능이 필요할때는 Class를 사용하고, 그게 아니면 Struct 를 쓰자. 그래서 default 라고 하는건가보다
  
  
  
