## hackerrand with Ruby

루비 연습겸 해커랭크에서 하루 1문제 풀기.


1. Simple Array Sum

   가장 처음 접근한 방법

   ```rb
    def simpleArrSum(ar)
      sum = 0;
      ar.each{ |x| sum += x }
      return sum
    end
   ```

  루비의 도큐먼트를 찾아보고 알게된 방법

  ```rb
  def simpleArrSum(ar)
    # 1. reduce와 심볼을 사용한 방법
    ar.reduce(:+)
    # 2. inject와 block을 사용
    ar.inject { |sum,n| sum + n }
    # 3. array의 method인 `.sum`을 사용한 방법
    ar.sum
  end
  ```


  `.inject`에 대해 루비 도큐먼트에서는 다음과 같이 설명한다. - Combines all elements of enum by applying a binary operation, specified by a block or a symbol that namew a method or operator.
  The `inject`and `reduce` methods are **aliases**. There is no performance benefit to either.

  `inject(initial, sym)` → obj click to toggle source
  `inject(sym)` → obj
  `inject(initial) { |memo, obj| block }` → obj
  `inject { |memo, obj| block }` → obj

  두번째처럼 `ar.inject { |sum,n| sum + n }` 블럭을 지정하게되면 배열의 각각의 요소는 accumulator value(memo)-지금 케이스에서는 `sum` 그리고 각각의 요소를 나타내는 `n`으로 넘겨진다. 따라서 sum은 축적되는 값이고 n은 배열의 각각의 요소가 차례대로 넘겨지게 된다. 블럭안에 `sum + n`을 통해 요소들이 더해져서 총 합을 구할 수 있게된다.




---


루비 공부 2일째, 그동안 자바스크립트만 하다가 새로운 언어를 배우니 너무 재밌다. 기본 개념은 무리없이 이해할 수 있었는데 `symbol`을 이해하기가 참 쉽지 않다.
