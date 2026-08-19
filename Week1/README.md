# 1일차 실습-1 : 영화 추천 시스템

## 실습 목적

영화 목록을 벡터화하여 사용자와의 거리 계산(유클리드, 코사인)을 통해 사용자의 데이터와 유사한 영화를 찾는다.

## 전체 흐름

1. 데이터 벡터화 : 문자는 원핫인코딩으로 따로 처리해야 나머지와 합친다 + 나머지 정규화 (df)
2. to_numpy해서 한 번에 거리 계산 후 원래 df에 붙임
3. dot해서 크기로 나눠서 코사인 유사도 계산 -> 코사인 거리 계산 후 원래 df에 합
4. 거리 기준 정렬 (sort_values)

## 주요 개념

- DataFrame
- One-hot Encoding
- Feature Scaling
- Vector Representation
- Euclidean Distance, Cosine Distance
- NumPy Broadcasting
- loc, iloc

## 배운 것

- 서로 다른 범위의 수치 데이터를 비교할 땐 Scaling한다
- 문자 데이터는 원핫인코딩으로 베터로 표현한다
- Series를 to_numpy해서(ndarray로) 벡터 연산한다
- Euclidean distance와 cosine distance로 벡터의 유사도를 비교한다
- for문으로 하나씩 계산 ㄱㄴ but broadcasting으로 여러 벡터의 거리 한번에 계산 ㄱㄴ하다
