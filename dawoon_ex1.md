#### 하기 문서는 [[Decentralized Identifier](https://www.w3.org/TR/did-core/#introduction)] v1.0 기준으로 작성되었습니다.

<br/>
<br/>
<br/>

# 1. [[Introduction](https://www.w3.org/TR/did-core/#introduction:~:text=1.-,Introduction,-This%20section%20is)]

개인과 조직으로서 많은 사람들이 다양한 환경에서 전 세계적으로 고유한 ID를 사용합니다. 이것들은 통신 주소(전화번호, 이메일 주소, 소셜 미디어의 사용자 이름), 신분증 번호(여권, 운전면허증, 세금 식별 번호, 건강보험), 제품 식별자(일련번호, 바코드, RFIDs)로 사용됩니다. URI(Uniform Resource Identifiers)는 웹에서 리소스를 가리키기 위해 사용되며, 브라우저에서 각 웹 페이지는 전 세계에서 고유한 URL(Uniform Resource Locator)을 갖고 있습니다.

전 세계적으로 고유한 ID 대부분은 우리의 통제 범위를 벗어납니다. 외부 기관에서 발급되며, 누구나 무엇을 의미하는지, 언제 폐기될 수 있는지를 결정합니다. 이러한 ID는 특정한 환경에서만 유용하며 특정 기관에서만 인정됩니다. ID는 운영 기관의 운영 실패로 인해 사라질 수도 있으며, 개인 정보를 불필요하게 노출시킬 수도 있습니다. 많은 경우, 악의적인 제3자가 "신분 도용"과 같은 방법으로 이를 부정하게 복제하고 주장할 수 있습니다.

이 사양서에서 정의된 분산 ID(Decentralized Identifiers, DIDs)는 새로운 유형의 전 세계적으로 고유한 ID입니다. 개인과 조직이 신뢰하는 시스템을 사용하여 자체 ID를 생성할 수 있도록 설계되었습니다. 이러한 새로운 ID는 디지털 서명과 같은 암호학적인 증명을 사용하여 ID를 통제하는 개체가 그 ID에 대한 통제를 입증할 수 있습니다.

DID의 생성과 선언은 운영 주체에 의해 통제되므로, 각 운영 주체는 원하는만큼 많은 DIDs를 가질 수 있어서 신원, 주체 및 상호 작용을 분리하여 유지할 수 있습니다. 이러한 ID의 사용은 다른 사람, 기관 또는 시스템과의 상호 작용에 맞게 적절하게 범위가 지정될 수 있습니다. 그들은 개체가 자신을 식별하거나 제어하는 사물과 상호작용하는 데 필요한 다른 사람, 기관 또는 시스템과의 상호작용을 지원하면서 개인적이거나 비공개 데이터를 얼마나 공개해야 할지에 대한 통제력을 제공합니다. 이 ID의 지속적인 존재를 보장하기 위해 중앙 기관에 의존하지 않습니다. 이러한 아이디어는 DID Use Cases 문서[DID-USE-CASES]에서 탐구됩니다.

이 사양서는 DIDs의 생성, 지속성, 해결, 해석을 위한 특정 기술이나 암호화를 가정하지 않습니다. 예를 들어, implementers는 통합 또는 중앙 집중식 식별 관리 시스템에 등록된 ID를 기반으로 DID를 생성할 수 있습니다. 실제로 거의 모든 유형의 ID 시스템은 DIDs를 지원할 수 있습니다. 이는 중앙 집중식, 연합된 및 DID의 세계 사이의 상호 운용성에 대한 다리를 만듭니다. 이는 implementers가 신뢰하는 컴퓨팅 인프라(분산 원장, 분산 파일 시스템, 분산 데이터베이스, P2P 네트워크 등)와 함께 작동할 수 있는 특정 유형의 DIDs를 설계할 수 있도록 합니다.

이 사양서는 다음과 같은 대상을 위한 것입니다:

- Decentralized Identifiers의 핵심 아키텍처 원칙을 이해하고자 하는 사람들

- Decentralized Identifiers 및 관련 데이터 형식을 생성하고 사용하려는 소프트웨어 개발자들

- 소프트웨어 및 하드웨어 시스템에서 Decentralized Identifiers를 사용하는 방법을 이해하려는 시스템 통합자들

- 이 문서에서 설명하는 생태계에 부합하는 새로운 DID 인프라(이 문서에서는 DID methods로 알려짐)를 생성하려는 명세 작성자들

추가로 이 사양서 외에도, 독자들은 Use Cases and Requirements for Decentralized Identifiers[[DID-USE-CASES](https://www.w3.org/TR/did-core/#bib-did-use-cases)] 문서를 유용하게 찾을 수 있습니다.  
<br/>
<br/>
<br/>

## [[1.1 간단한 예제](https://www.w3.org/TR/did-core/#introduction:~:text=1.1-,A%20Simple%20Example,-This%20section%20is)]

DID는 세 부분의 간단한 문자열로 구성되어 있다.

1. the did URI scheme identifier
2. the identifier for the DID method
3. DID method-specific identifier
   <br/>
   <br/>
   <br/>

![](https://www.w3.org/TR/did-core/diagrams/parts-of-a-did.svg)

<center>그림 1. DID(Decentralized identifier의 간단한 예</center>
