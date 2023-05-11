## 책임
- 리더는 마스터 브랜치와 개발 브랜치의 관리 및 유지보수 책임을 가집니다.
- 풀러는 개발 브랜치와 기능 브랜치의 관리 및 유지보수 책임을 가집니다.
- 모든 팀 구성원은 성실하게 PR을 올려야 하며 코드리뷰를 반드시 진행해야 합니다.
## 브랜치 관리
- 리더, 풀러, 팔로워는 개발을 할 때 기능 브랜치로부터 개발을 시작합니다.
- 브랜치명은 소문자만 사용합니다. 대문자를 절대! 사용하지 않습니다.
- 기능 브랜치는 개발 브랜치에서 생성합니다.
  - 개발 브랜치는 developed/somename 의 포멧을 준수합니다.
    - somename 부분의 이름은 버전개념을 써도 됩니다.
    - somename 부분의 이름은 적용 대상 기능을 대표하는 이름을 써도 됩니다.
    - somename 부분의 이름은 마스터 브랜치로 PR 하기 위한 목표날짜나 브랜치를 생성한 날짜를 써도 됩니다.
  - 기능 브랜치는 feature/somename 의 포멧을 준수합니다.
    - somename 부분은 반드시 개발 한 기능의 이름을 명시해야 한다. 혹은 기능의 동작을 문장으로 써도 된다.
- 기능 브랜치는 생성하기 전 반드시 개발 브랜치로 체크아웃하여 `git pull`을 통해 브랜치를 최신화 시킨 후 생성해야 합니다.
- 기능 브랜치를 개발 브랜치에 PR 할 때는 반드시 Reviewer와 Assigner를 지정해야 합니다.
  - 리더의 Reviewer는 풀러, Assigner는 팔로워로 지정합니다.
  - 풀러의 Reviewer는 리더, Assigner는 팔로워로 지정합니다.
  - 팔로워의 Reviewer는 풀러, Assigner는 리더로 지정합니다.
  - Reviewer는 최소 한개 이상의 코드리뷰 흔적을 남겨야 합니다.
  - Assigner는 항상 확인해야 하고 체크 이모지 혹은 "확인했습니다" 같은 최소한의 흔적을 남겨야 합니다.
- 마스터 브랜치와 개발 브랜치는 각각 한개씩만 있어야 합니다.
- 기능 브랜치는 항상 리모트 위치의 개발 브랜치를 로컬로 PULL 받은 후에 생성해야 합니다. (=로컬위치의 개발 브랜치를 항상 최신 상태로 유지해야 한다는 의미)
- 마스터 브랜치는 무조건 개발 브랜치에서만 PR을 받습니다.
  - 기능 브랜치에서 마스터 브랜치로 머지하는 경우는 (=PR하는 경우는) 없게 관리 되어야 합니다.
  - 개발 브랜치에서 마스터 브랜치로 바로 머지해선 안되며 반드시 PR을 통해 머지 되도록 관리 되어야 합니다.
- 리더는 이 부분에서의 관리 책임을 가집니다.
## Pull Requests
- PR의 사이즈는 최대한 작게 유지합니다.
- PR은 한번 할 때 마다 가급적이면 변경되는 코드 라인 수는 400줄 이하로 유지 할 수 있도록 의식적으로 노력합니다. (옵션)
- PR을 등록하는 사람은 그 코드의 맥락을 최대한 자세하게 작성합니다.
## 코드리뷰
- 코드리뷰를 진행하고 그 흔적을 깃헙에 남겨야 합니다.
- 내가 개발한 코드에 나 자신을 투영하면 감정이 상할 수 있습니다.
  - 리뷰를 하는 사람도, 받는 사람도 코드 자체에만 집중 할 수 있도록 노력하는 자세가 필요합니다.
  - 처음엔 서운할 수 있겠지만 객관화 할 수 있도록 노력합시다!
    - 내 실력에 대한 좌절감을 느낄 필요가 없습니다.
    - 비판 받는 것 같은 불안감도 느낄 필요가 없습니다.
    - 지적 받는 느낌으로 인해서 불편하고 자존심이 상한다면 그 순간에는 성장에 브레이크가 걸린다고 생각해야 합니다.
  - 코드리뷰를 통해 받은 코멘트는 두 번 실수하지 않도록 학습하는 자세를 보여야 합니다.
    - 같은 내용의 피드백이 여러 PR에서 연속해서 나오면 리뷰어는 힘이 빠져버립니다.
  - 모르는 것을 묻는 것은 부끄러운 일이 아님을 꼭 기억합니다.
- 리뷰어는 꼼꼼하게 코드를 확인해서 코드에서 발생 할 수 있는 문제를 볼 수 있도록 노력해야 합니다. (감정 섞지 않기)
  - 코드리뷰 진행 시 아래 내용은 반드시 확인 할 수 있도록 노력합니다.
    - 기본적인 자바 스타일의 코드 컨벤션을 준수 했는지 확인합니다. (들여쓰기, 괄호 위치, 변수/함수/클래스명 등과 같은 기본적인 컨벤션)
  - 좋은 의도를 전제로 친절하게 ! 리뷰하기
    - 호기심을 가지고 작성자의 의도를 파악하는 자세가 중요합니다.
  - 명확하고 구체적인 피드백을 주어야 합니다.
    - "코드를 뭐 이렇게 짰어요?" > 안됩니다.
    - 친절하게! 이유와 함께! 피드백하기
    - 수정이 필요한 부분은 그 수정이 왜 필요한지에 대한 이유를 기술해줄 수 있도록 노력합니다.
    - "이 부분은 수정이 필요해 보입니다", " 이 함수에서 책임이 두개인데요 하나로 만들어주세요" 같이 피드백 하지 말고 더 구체적으로 피드백합니다.
    - "이 함수는 현재 A라는 기능과 B라는 기능이 같이 있는데요 저 두 가지 기능을 각각의 함수로 빼서 if문 부분의 비즈니스 로직이 좀 더 쉽게 표현 될 수 있도록 구현해보세요! 왜냐하면 객체지향은 단일책임원칙을 준수하기 때문입니다. :활짝_웃는:"
  - 이모지를 섞으면 공격성이 낮아 보입니다. 자주 씁시다. :윙크::미소짓는_상기된_얼굴:
- 코드리뷰는 최대한 빨리 해야 합니다.
  - PR부터 코드리뷰 완료 후 머지까지 하루를 넘기지 않도록 노력합니다.
- 코드리뷰를 받은 사람은 리뷰 받은 내용에 대해 확실하게 리액션 해야 합니다. (=코멘트에 대해서는 명확하게 피드백해야 합니다.)
  - "반영 완료했습니다", "이 부분은 이렇게 하는게 좋을 것 같습니다" 같은 리액션을 확실히 해야합니다.
  - 그냥 Resolve 만 누르는 경우는 없어야 합니다.
- 리뷰어는 리뷰를 남길 때 모든 건마다 얼마나 중요한지 중요성을 명기 할 수 있도록 노력합니다. 그리고 질문인지 요청인지 성격을 명확히 합니다. (질문인지 요청인지, 얼마나 중요한지)
  - "이건 중요해요!"
  - "이건 마이너 한 사항이긴 한데요!~~"
  - "이 부분은 XX함수에서 이미 개발 된 부분이 있습니다. 한번 확인해보시겠어요? :볼을_붉히는_얼굴:"
- 리뷰가 완료 된 경우 상대방에게 꼭 "대화"로 알려줍니다. 너무 늦은 경우 슬랙 멘션이라도 남길 수 있도록 노력합니다._
