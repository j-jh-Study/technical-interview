## DI


>Dependency Injection (DI)는 객체지향 프로그래밍에서 사용되는 설계 패턴 중 하나로, 객체 간의 의존성을 느슨하게 만들어주는 기술입니다. DI를 사용하면 코드의 결합도가 낮아져서 코드 유지보수가 용이하고, 유닛 테스트를 쉽게 작성할 수 있습니다.
DI는 객체 간의 의존성을 객체 생성자나 메서드 인자를 통해 외부에서 주입받도록 하는 방법입니다. 이렇게 외부에서 의존성을 주입하면 객체가 직접 의존성을 생성하거나 참조하지 않아도 되므로 코드의 결합도가 낮아집니다.
DI의 장점으로는 다음과 같은 것들이 있습니다:

1. 유지보수가 쉽다: DI를 사용하면 의존성을 주입받는 객체의 변경 없이 의존성을 변경할 수 있습니다. 이렇게 하면 의존성이 변경되는 경우 해당 객체를 수정하지 않아도 되므로 유지보수가 쉬워집니다.

2. 코드의 재사용성이 높아진다: DI를 사용하면 객체가 서로 독립적으로 작동하므로 코드의 재사용성이 높아집니다.

3. 유닛 테스트가 쉽다: DI를 사용하면 테스트할 객체에 대해 의존성을 쉽게 주입할 수 있으므로 유닛 테스트 작성이 쉬워집니다.

4. 코드의 결합도가 낮아진다: DI를 사용하면 객체 간의 결합도가 낮아지므로 코드의 유지보수와 확장성이 좋아집니다.

> DI는 대규모 애플리케이션 개발에서 매우 유용한 기술이며, Spring Framework 등 많은 프레임워크에서 DI를 지원하고 있습니다.

***

[DI 상세](https://velog.io/@gillog/Spring-DIDependency-Injection)
하는이유 ! SOLID 중 open closed principle 지킬려고 .. ! 

스프링부트 DI하는 법  그중 생성자주입이 ocp 지킨다 
1. 필드주입
2. 세터주입
3. 생성자주입

필드주입 -> SRP 위반 ,  의존성이 숨어! , 불변성일 지키기힘들다, 순환의존성 알기 힘들다

세터주입 ->주입이 필요한 객체가 주입이 되지 않아도 얼마든지 객체를 생성할 수 있다는 것이 문제


생성자 주입의 경우 
- null을 주입하지 않는 한 NullPointerException 은 발생하지 않는다.
- final 을 사용할 수 있다.
- 순환 의존성을 알 수 있다.
