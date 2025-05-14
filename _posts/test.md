> [!NOTE]  
> Highlights information that users should take into account, even when skimming.


> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Crucial information necessary for users to succeed.

> [!WARNING]  
> Critical content demanding immediate user attention due to potential risks.

> [!CAUTION]
> Negative potential consequences of an action.

 개발자가가 잘못 알고있는 성능 지식에 대해서 공유해보려고 합니다.

> [!NOTE] 사전지식
> 기본적인 <b>C++<b>, <b>STL<b> 문법 지식

### O(1)에 대한 오해
개발자들이 흔히 실수할 수 있는 부분 중 하나는 O(1)에 대한 오해를 가지고 있습니다.

> [!NOTE] O(1) 이란
> N개의 원소를 처리하는데 있어 계산의 빈도수가 1이라는것을 의미합니다. <br>

여기서 많은 개발자분들의 오해가 발생하기 시작합니다.

🙋‍♂️ : "십 만개, 백 만개 원소들의 계산 수는 1번이니 빠르겠네?" <br>
🧑‍🏫 : "맞습니다. 대부분의 상황에서는 10만 번 계산하는 것 보다 1 번 계산한는 것이 빠르지요" <br> 

#### 🙃 그럼 반대로 생각해볼까요?

O(1)이라는 말만 듣고 무작정 빠르다고 믿는 건, 사실 위혐할 수도 있습니다.
예를 들어, O(1) 알고리즘이 매우 복잡한 연산을 1번 수해하는 것이라면 어떨까요?

🤔 10만 번의 단순한 연산O(N)이, 1번의 복잡한 연산O(1)보다 빠를 수도 있다는 뜻입니다.

즉, **시간 복잡도는 "입력 크기에 따른 처리 수"** 를 나타내는 이론적 지표이지, 실제 실행 시간의 절대적인 속도 비교 기준은 아닙니다.

> [!WARNING] O(1) ≠ 항상 빠름
> 구현 방식, 연산 내용, 캐시 효율성을 고려하여 성능을 분석해야합니다.

🙋‍♂️ : "저희가 잘못 알고 사용하고 있을 수 있는게 뭐가 있을까요" <br>
🧑‍🏫 : "대표적으로 STL MAP을 가장 잘못된 사용으로 하는 분이 있을 것 같습니다"

MAP은 2가지 종류로 나뉘어 지는데 std::map, std::unordered_map으로 나뉘게 됩니다.<br>

