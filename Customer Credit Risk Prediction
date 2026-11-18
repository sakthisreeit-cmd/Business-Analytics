# Ex 9 Customer Credit Risk Prediction
data <- read.csv("customer_credit_risk.csv")
data$Credit_Risk <- as.factor(data$Credit_Risk)
model <- glm(Credit_Risk ~ Credit_Score + Debt,
             data = data,
             family = binomial)
print(model)
new_customer <- data.frame( Credit_Score = 600, Debt = 12000)
probability <- predict(model,new_customer,type = "response")
print(probability)
if(probability >= 0.5) {
  print("High Risk")
} else {
  print("Low Risk")
}
