# BowlingGame
볼링 점수를 계산하는 프로그램을 작성합니다. :bowling: :chart_with_upwards_trend:

## 기본 요구사항
- 볼링게임(BowlingGame)클래스의 인스턴스를 만들면 새 게임이 시작한 것으로 간주합니다. (명시적인 start는 필요없음)
- 현재 몇번째 프레임의 몇번째 투구(첫번~세번째)를 할 차례인 조회해 볼 수 있어야 합니다. 게임이 끝났으면 `GameOverException`을 던져야합니다. (Frame번호 + 그 프레임의 시도횟수)
- 현재까지 진행된 프레임결과와 각 프레임 점수를 보여줍니다. 확정되지 않은 점수는 표시하지 않아도 됩니다.
- 한번 투구를 하는 메소드(roll)를 만들고 쓰러뜨린 핀의 수를 패러미터로 넘깁니다. 게임이 끝났으면 `GameOverException`을 던져야합니다.
- 볼링 한 게임에 대한 점수판을 구현해야 합니다.

### 추가 요구사항
- 게임을 시작할 때 플레이어 수를 지정할 수 있습니다.
- 각 플레이어 별로 게임 점수를 확인할 수 있습니다.

## 볼링 점수 계산 방법
- Strike인 경우는 해당 프레임의 점수에 다음 두 번 투구해서 얻은 점수를 더합니다. 따라서 이후 두 번 더 투구할 때까지 Strike한 프레임의 점수는 확정되지 않습니다.
- Spare인 경우는 해당 프레임의 점수에 다음 한 번 투구해서 얻은 점수를 더합니다. 따라서 이후 한 번 더 투구할 때까지 Spare한 프레임의 점수는 확정되지 않습니다.
- 마지막 프레임의 경우는 위의 두 가지 조건을 만족하기 위해서 Strike이면 두 번, Spare면 한 번 추가 투구가 가능합니다.

## 입력
| 구분 | 기호 |
|-|-|
| Strike | `X` |
| Spare | `/` |
| Gutter | `-` |
| 그외 | `0, 1, 2, ... , 9` |

## 출력
볼링 게임을 진행한다고 가정하고, 프레임의 점수를 입력하면 다음과 같은 결과 화면을 볼 수 있어야 합니다.
아래 화면은 게임이 끝났을 때의 결과 화면이고, 게임이 진행 중에도 아래와 같은 점수 판을 볼 수 있어야 합니다.

![OutputExample](https://mblogthumb-phinf.pstatic.net/20130630_30/lifesewon_1372584267266CBgk9_JPEG/%BA%BC%B8%B5%C1%A1%BC%F6_%282%29.jpg?type=w2)

(출처 : https://mblogthumb-phinf.pstatic.net/20130630_30/lifesewon_1372584267266CBgk9_JPEG/%BA%BC%B8%B5%C1%A1%BC%F6_%282%29.jpg?type=w2)

## 참고 문서
- 객체 지향 생활체조
    - http://elaia.tistory.com/3
    - 『소트웤스 앤솔러지, 마틴파울러 외 지음, 위키북스』 83~96 페이지
  

## References
https://www.slipp.net/wiki/download/attachments/14909443/%EA%B0%95%EC%9D%98%20%EA%B0%9C%EC%9A%94,%20%EB%A9%94%EC%9D%B4%EB%B8%90,%20TDD.pdf?version=1
