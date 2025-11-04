<h1>10주차 내용 정리</h1>

<ol>
  <li>머티리얼 라이브러리
    <ol>
      <li>
        구글의 머티리얼 디자인은 모바일과 데스크톱, 다양한 장치를 아우르는 일관된 애플리케이션 디자인 지침
      </li>
      <li>
        구성 요소 중심 설계: Card, Button, TextField 등 모든 UI 컴포넌트를 현대적으로 재설계
      </li>
      <li>
        과거: Jetpack Compose 현재: Material Design 3 (MaterialTheme 중심)
      </li>
      <li>
        <strong>Material Design 3 주요 속성</strong>:
        <ol>
          <li><strong>colorScheme</strong>: M3 동적 색상 시스템 적용 (<code>dynamicLightColorScheme</code>)</li>
          <li><strong>typography</strong>: 새로운 Typography 구조 (LineHeight, Weight 등)</li>
          <li><strong>shapes</strong>: M3의 곡선 및 둥근 모서리 기준</li>
        </ol>
      </li>
    </ol>
  </li>

  <li>공통 Scaffold
    <ol>
      <li>
        <strong>Scaffold</strong>: MD3의 가장 기본적인 화면 구조를 제공하는 컨테이너
      </li>
      <li>
        topBar, bottomBar, floatingActionButton, content 등 주요 UI 요소를 슬롯 형태로 제공
      </li>
      <li>
        개발자가 각 영역에 원하는 Composable을 쉽게 배치할 수 있도록 돕는다
      </li>
      <li>
        <strong>BaseScaffold</strong>는 Scaffold를 한 번 더 감싸, 앱만의 공통 레이아웃 규칙 적용
      </li>
      <li>
        <strong>추가 내용</strong>:
        <ol>
          <li>
            <strong>modifier</strong>: Compose에서 UI 요소의 외형, 위치, 크기, 동작을 꾸미는 도구  
            예: <code>modifier: Modifier = Modifier</code> → 기본값은 아무것도 적용되지 않음. 필요하면 호출 시점에서 스타일이나 배치 옵션 추가 가능
          </li>
          <li>
            <strong>topBar</strong>: <code>@Composable () -> Unit</code>  
            → 인자를 받지 않고(Unit), 반환 값 없는 Composable 함수 요구
          </li>
          <li>
            <strong>bottomBar</strong>: <code>@Composable () -> Unit = {}</code>  
            → 기본 구현이 비어있음. 사용자가 넘기지 않으면 UI가 나타나지 않음
          </li>
