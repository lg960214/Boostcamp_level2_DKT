# Deep Knowledge Tracing LGBM 설명

- LGBM 모델 사용
- Train용 데이터 : Train 데이터셋 전체, Test 데이터셋 중 유저 별 마지막 2 번째 ~ 마지막 문제 제외한 데이터들
- Val 용 데이터 : Test 데이터셋 중 유저 별 마지막에서 2 번째 문제
- 제출 용 데이터 : Test 데이터셋 중 유저 별 마지막 문제 

# 현재까지 성능 개선에 도움이 된 Feature들
1. seconds : 이전 문제와의 시간 차이 (780초 이상은 780초로 변환 - 아래 그래프 문제 푼 minute 평균 참고)![문제 푼 minutes](https://user-images.githubusercontent.com/86274940/167414013-b880013d-5c9d-4537-a0a5-43ea9dc9f2fc.PNG)
2. user_correct_answer : 유저 별 정답 누적 합
3. user_total_answer : 유저 별 푼 문제 수 누적 합
4. before_correct(n) : 직전 n번째 문제 맞췄는지 여부
5. rolling_(n) : 현재로부터 직전 n번째 문제까지의 정답 합
6. seconds_mean : Test 별 소요 시간 평균
7. user_acc : 유저 별 정답률 평균
8. tag_mean : tag 별 정답률 평균
9. test_mean : test 별 정답률 평균
10. test_sum : test 별 정답 수
11. sort_assess : assessment(각 문제)의 번호
12. ass_mean : 각 문제 별 정답률 평균
13. u_mean : 유저 별 정답률 평균
14. u_sum : 유저 별 정답 수
