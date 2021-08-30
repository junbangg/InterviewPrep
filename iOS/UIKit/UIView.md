# UIKit

## UIView
  > 화면에 있는 직사각형 영역의 내용을 관리하는 객체. 앱의 유저 인터페이스를 이루는 단위.
* UIView의 책임
  * 그리기 / 애니메이션
  * 레이아웃 / 서브뷰 관리
  * 이벤트 관리
> 뷰 안에 뷰를 넣어서 뷰 계층 구조를 형성 할 수 있다.
  - 이러면 뷰와 서브뷰 간의 부모-자식 관계가 생긴다.
  - 부모-자식 뷰 관계는 1:다 이다
> 뷰 생성(프로그래밍)
  - 초기 사이즈와 위치를 부모뷰(superview)에 relative 하게 설정한다
  - subview를 view에 추가할때 addSubview() 를 사용한다
    - 새로운 뷰를 추가하면 다른 서브뷰(sibling) 위에 올려진다.
    - insertSubview:aboveSubview()
    - insertSubview:bewlowSubview: 등을 사용해서 z-order 를 수정할 수 있다.

* View Programming Guide for iOS https://developer.apple.com/library/archive/documentation/WindowsViews/Conceptual/ViewPG_iPhoneOS/CreatingViews/CreatingViews.html#//apple_ref/doc/uid/TP40009503-CH5-SW1
