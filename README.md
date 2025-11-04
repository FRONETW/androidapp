#10주차 내용 정리하기
머티리얼 라이브러리:
	-구글의 머티리얼 디자인은 모바일과 데스크톰, 그리고 그 밖에 다양한 장치를 	아우르는 일관된 애플리케이션 디자인 지침
	-구성 요소 중심 설계: Card,Button,TextField 등 모든 UI 컴포넌트를 현대적으로 	재설계함
	-과거: Jetpack Compose 현재: Material Design 3( MateriaTheme 중심 )
		-colorScheme: M3의 동적 색상 시스템 적용(dynamicLightColorScheme)
		-typography: 새로운 Typography 구조(LineHeight, Weight 등)
		-shapes: M3의 곡선 및 둥근 모서리 기준
공통 Caffold
	Scaffold: MD3의 가장 기본적인 화면 구조를 제공하는 컨테이너
		-topbar,bottombar,floatingActionButton, content 등 주요 UI 요소를 
		슬록형태로 제공
		-개발자가 각 영역에 원하는 컴포저블을 쉽게 배치할 수 있도록 돕는다
		-BaseScaffold는 이 Scaffold를 한 번 더 감싸, 우리 앱만의 공통 
		레이아웃 규칙이 적용되도록 한다
		추가내용:
		-modifier는 Jetpack Compose에서 Ui 요소의 외형, 위치, 크기, 동작을 꾸미는 도구이다.modifier: Modifier = Modifier는 기본값이 아무것도 
		적용되지않은 modifer이고 필요하면 호출 시점에서 추가 스타일이나 배치 옵션을 전달할 수 있다는 의미다
		- topBar: @Composable () -> Unit는 topbar라는 피라미터는 인자를 받지 않고(Unit), 아무 값도 반환하지 않는 Conposable 함수를 요구한다는 		뜻(타임만 지정되한 상태)
		-bottomBar: @Composable () -> Unit = {}의 {}는 기본 구현을 뜻함
		그렇기에 사용자가 넘기지 않으면 아무 UI가 안 나오는 바를 기본값으로 선정됨(코틀린에서는 람다 기본값을 지정할때 {}를 사용함 )
