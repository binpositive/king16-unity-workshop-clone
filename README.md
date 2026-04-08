## 👑 유니티 속성 워크숍 가이드

**1. 깃허브 가이드**
1. 레포지토리 세팅
* 프로그래머 팀장이 레포지토리를 **Fork**합니다.
* 포크한 레포지토리의 `Settings > Collaborators` 탭에서 팀원의 깃허브 계정을 **Add** 합니다.
* 팀장의 레포지토리를 로컬 PC로 **Clone**합니다.
2. 결과물 제출 방법
* 모든 스테이지 요소는 기본으로 제공되는 Room 오브젝트의 하위에 배치합니다.
* 작업이 완료된 Room 오브젝트를 RoomN **프리팹(Prefab)**으로 만들어 커밋합니다.
  * 기존 Room 프리팹을 수정하는 것이 아닌, 새 RoomN 프리팹을 생성 후 커밋합니다.
* 팀의 레포지토리에서 스테이지 작업 후 원본 레포지토지의 main 브랜치로 **Pull Request** 합니다.
> PR 제목 양식: **[TeamN] N스테이지 완성**

**2. 유니티 가이드**
깃 충돌 방지를 위해 아래의 규칙을 지켜주세요.
* 모든 팀 에셋(스크립트, 프리팹 등)은 반드시 **팀 폴더**(`Assets/TeamN/`) 내에서 관리합니다.
* Game 탭의 해상도는 **QHD**(`2560 x 1440`)로 통일합니다.
* 기본으로 제공되는 리소스는 수정하지 않습니다.
* `Scene`을 커밋하지 않습니다. 최상위 Room 오브젝트 외의 참조가 필요한 상황이라면 `FindObjectOfType<T>()`를 적극 활용합니다. (ex. `Player` 스크립트)
* `Canvas`를 사용해야 하는 상황이라면 Render Mode를 `World Space`로 설정합니다.
* 팀이 새로 생성한 모든 스크립트에는 아래와 같이 `namespace`를 적용합니다.
```csharp
namespace TeamN {
    public class NewScript : MonoBehaviour { ... }
}
```
