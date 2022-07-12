****
### Terms
- False positive & false negative
- Confusion Matrix
- Accuracy paradox
- CAP curve

# 분류 모델 성능 평가

## False positive & false negative
![image](https://user-images.githubusercontent.com/39285147/178429660-ef6c4623-c5d4-4d43-8117-da577939d3fb.png)
- **False Positive**: 무언가 일어난다 했는데 실제로는 일어나지 않음 (i.e., 지진이 난다고 예측했는데 실제로는 일어나지 않음)
- **False Negative**: 무언가 일어났는데 일어나지 않았다고 예측함 (i.e., 지진이 났는데 안 났다고 오류를 범함)

## Confusion Matrix
![image](https://user-images.githubusercontent.com/39285147/178430495-399adb81-b6a4-4f91-bde7-cd10ce939406.png)

### Calculate two rates
1. **Accuracy Rate(AR)** = Correct / Total AR (i.e., 85/100 = 85%)
2. **Error Rate(ER)** = Wrong / Total (i.e., 15/100 = 15%)

## Accuracy paradox
![image](https://user-images.githubusercontent.com/39285147/178431036-5e3c816c-55f9-46ce-ad7c-5f34b6e9c215.png)

한 모델에 기반해서 정확도를 추측한 결과가 **절대적으로** 옳지 않음을 증명한다. 그래서, 다양한 방법들로 모형을 분석할 필요가 있다 (i.e., CAP Curve).

## CAP curve
![image](https://user-images.githubusercontent.com/39285147/178433420-25feefc5-a1db-4877-b6a9-580ce6f28411.png)

A cumulative accuracy profile can be used to evaluate a model by comparing the current curve to both the *'perfect'* and a *randomized* curve

### Analysis 1
![image](https://user-images.githubusercontent.com/39285147/178435253-75d9bd8b-9c93-4d68-88d5-a9d819046a28.png)

### Analysis 2 (preferred)
![image](https://user-images.githubusercontent.com/39285147/178434879-8b5c9c8f-e5d5-40fe-b60c-de9810a1eef1.png)

# Note
~~Receiver Operating Characteristic(ROC)~~
