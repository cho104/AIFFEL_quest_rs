# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 이치오
- 리뷰어 : 이호창 


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 프로젝트 1의 회귀모델 예측정확도가 기준 이상 높게 나왔는가?
         - 2795.2935로 3000보다 낮습니다!  
          ![image](https://github.com/user-attachments/assets/e8a16833-5f72-4294-91ac-cec0bbde89f5)  
  
    - 프로젝트 2의 회귀모델 예측정확도가 기준 이상 높게 나왔는가?  
         - 140로 150보다 낮습니다!  
          ![image](https://github.com/user-attachments/assets/959157a1-396e-4142-8a7b-71c3e1c6a928)

    - 시각화 요구사항이 정확하게 이루어졌는가?  
         - 시각화도 모두 잘 이루어져있습니다!  
         ![image](https://github.com/user-attachments/assets/9ebbfdbf-05cb-4515-a8e6-3709209d2d6c)  
         ![image](https://github.com/user-attachments/assets/781ed6de-a684-482b-99eb-4e3eef0fafad)  


    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**  
      - 관련이 없는 `atemp`, `minute`, `second` 변수들까지도 추가적으로 분석하여 drop 해주었습니다.    
          ![image](https://github.com/user-attachments/assets/5d893b87-bf7f-44e0-a2b0-9d02005cd353)  

        
- [ ]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        
- [x]  **5. 코드가 간결하고 효율적인가요?**  
       - `subplot`의 ax의 경우 코드를 여러번 작성하는 것을 적절하게 줄여서 작성하였습니다!   
          ![image](https://github.com/user-attachments/assets/8a9967d8-8238-4420-81f0-b5b4e11fa894)  



# 회고(참고 링크 및 코드 개선)
```
## 회고:
## 중간에 커널 연결에 오류가 있음에도 불구하고 끝까지 코드를 올려주셔서 감사합니다 :)
## 저는 casual 과 registered 변수만 제거하였는데, atemp의 경우 temp와 상관성이 높고
## minute 과 second 변수의 경우 모든 값이 동일해서 함께 제거하신 부분에서 배워가는 것 같습니다. 
## 아래에 함수를 조금 더 간략하게 만들 수 있는 코드를 남겨놓았습니다! 수고 많으셨습니다ㅎㅎ
 

### 치오님의 코드
def model(X, W, b):
    prediction = 0
    for i in range(10):
        prediction += X[:, i] * W[i]
    prediction += b
    return prediction

### 개선되었으면 하는 코드
def my_model(X, W, b): 
    predictions = 0
    predictions = X @ W        ## 수정된 곳 numpy의 경우 간단한 행렬곱 함수
    predictions += b
    return predictions

```
