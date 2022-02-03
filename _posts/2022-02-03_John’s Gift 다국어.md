# John’s Gift 다국어

> ![img](https://d2gd6pc034wcta.cloudfront.net/tier/18.svg) 

| 시간 제한               | 메모리 제한 | 제출 | 정답 | 맞힌 사람 | 정답 비율 |
| :---------------------- | :---------- | :--- | :--- | :-------- | :-------- |
| 1.2 초 (추가 시간 없음) | 1024 MB     | 177  | 52   | 42        | 30.216%   |

## 문제



매일 아침, 가게 주인인 존은 서로 다른 가격의 $n$개의 상품과 $n$개의 가격표를 받습니다. 존은 가능한 한 많은 상품을 팔고 싶어하기 때문에 상품과 가격표를 일치시켜 두 쌍의 최대 차이(요컨대 최대 차이)를 최소화하며, 서로 다른 상품이 서로 다른 가격표를 맞춰야 합니다. 예를 들어, John이 $10$, $30$의 두 상품과 $10$, $20$ 가격의 두 가격 태그를 가지고 있는 경우, $(10, 10)$와 $(30, 20)$를 일치시켜 최대 차이를 $10$로 최소화할 수 있습니다. 이렇게 가장 작은 최대 차이를 일치 점수라고 합니다.

오늘, 존의 친구인 제인은 생일 파티를 하고 존은 그의 물건에서 생일 선물을 고르기로 결심합니다. 제품을 선택할 때 너무 많은 이익을 잃고 싶지 않으므로 제품을 제거하면 나머지 $n-1$ 제품에 대해 원래 $n$ 가격 태그와 일치하는 점수가 가장 작은 제품을 선택하려고 합니다. 그나저나 $n-1$ 상품을 매칭할 때, 존은 적절한 매칭을 위해 가격표 하나를 짝을 이루지 않고 둡니다.

예를 들어, John은 각각 $10$과 $30$인 상품 $G_1$과 $G_2$와 $10$와 $G_1$와 $G_2$. 그가 선물로 $G_1$를 선택한 경우 $G_2$의 가능한 가격은 $10$ 또는 $20$입니다. 그러면 $G_2$의 가격이 $20$일 때 일치하는 점수는 $10$입니다. 반면에 선물용으로 $G_2$를 선택하면 $G_1$의 가격이 $10$일 때 일치 점수는 0이 됩니다. 따라서 John은 가장 작은 일치 점수를 얻기 위해 $G_2$를 선물로 선택합니다. 즉, $n$ 상품 중 John은 선물로 어떤 상품이라도 선택할 수 있으며, 이것은 원래의 $n$ 가격 태그에 대한 나머지 $n-1$ 상품 간의 새로운 일치 점수를 정의합니다. $n$개의 가능한 선물 선택 항목 중에서 존은 제품을 제거하면 일치하는 점수가 가장 작은 상품을 찾고자 합니다.

$n$개의 좋은 값과 $n$개의 가격 태그를 고려하여 나머지 $n-1$개의 상품과 $n$개의 가격 태그 간에 가장 작은 일치 점수를 산출하기 위해 John이 선택해야 하는 선물 상품의 값을 인쇄하는 프로그램을 작성합니다. 선택할 수 있는 후보 상품이 두 개 이상 있는 경우 후보 상품의 최소 값을 인쇄합니다.



## 입력

Your program is to read from standard input. The input starts with a line containing an integer n$n$ (2≤n≤106$2 ≤ n ≤ 10^6$), where n$n$ is the number of goods and the number of price tags. The following line contains n$n$ positive and distinct integers that represent the values of n$n$ goods. The third line contains n$n$ positive and distinct integers that represent n$n$ price tags. The good values and the tag prices are no more than 109$10^9$.

## 출력

Your program is to write to standard output. Print exactly one line. The line should contain the value of the good that John picks for Jane’s birthday gift such that its removal produces the smallest matching score in the remaining n−1$n - 1$ goods. If there are multiple candidate goods, print the smallest value among the candidate goods.