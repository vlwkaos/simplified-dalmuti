
## Simplified Dalmuti (Card game)

  직업이 없는 간소화된 온라인 달무티

---

### 소개

node.js의 socket.io를 이용하면 실시간 웹 애플리케이션을 쉽게 만들 수 있다고 들어서 간단한 온라인 카드 게임을 만들어 보려고 했다. html을 수작업으로 만들고 jQuery를 이용했다..(?). 여기에는 개인적 사정이 있다. 또 당시 매우 금방 만들 수 있을 거로 생각하고 막 코딩을 하는 바람에 코드 상태가 조악하다. 그나마 나은 점은 서버에서 처리해야 할 부분과 클라이언트에서 처리해야 할 부분을 구분하고, 소통간 발생할 수 있는 예외적 상황을 고려하여 만들었다는 점이다. 

### 구현

- 클라이언트 쪽에는 대체로 무언가를 표시하는 기능만 넣었다. 
- 클라이언트간 소통이 필요한 정보의 경우 서버에서 만들어서 전파했다. 
- 클라이언트에서 서버로 정보를 보내는 경우 받는 정보가 유효한지 확인했다.
  - 게임 법칙에 위배되는 정보 (예: 자기 차례가 아닌데 패를 내는 상황, 손에 없는 패를 내는 상황)
- 언제 클라이언트 쪽 정보가 갱신되어야 하는지 고려했다.
- 게임 방 기능, 각 방 채팅, 게임
- 각 방의 게임 시작 상태에 따라 참가자를 관전자로 입장시킬 수 있다.
- 인원 초과의 경우 입장 불가 메세지를 띄웠다.
- 유저가 접속을 끊는 경우에도 게임이 지속된다.
- 조커카드 13을 구현했다. 



