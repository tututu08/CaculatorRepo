# 🎯 Swift 사칙연산 계산기 (Object-Oriented Calculator)

## 🏆 **프로젝트 개요**
이 프로젝트는 **Swift로 구현된 객체지향 기반의 사칙연산 계산기**입니다.  
각 연산을 독립적인 클래스로 분리하고, **추상화(Protocol)**을 적용하여 확장성을 극대화하였습니다.

---

## 🔥 **주요 기능**
- 🎯 **기본 연산 지원**: 덧셈, 뺄셈, 곱셈, 나눗셈, 나머지 연산
- 💡 **예외 처리**: 0으로 나누는 경우 `"undefined"` 반환
- 🚀 **확장 가능**: `Calculator` 수정 없이 새로운 연산(예: `제곱 연산`) 추가 가능
- 🔗 **객체지향 설계 적용**: OCP(개방-폐쇄 원칙) 준수
## 📚 **사용 방법**
📌 **Xcode에서 "Command Line Tool" 프로젝트를 생성한 후 실행**  
📌 **연산 클래스를 활용하여 다양한 연산 수행 가능**  

```swift
import Foundation

let calculator = Calculator()

print("🛠️ [사칙연산 테스트]")

// ➕ 덧셈 테스트
print("10 + 5 =", calculator.calculate(AddOperation(), 10, 5))  // "15.0"

// ➖ 뺄셈 테스트
print("20 - 8 =", calculator.calculate(SubtractOperation(), 20, 8))  // "12.0"

// ✖️ 곱셈 테스트
print("3 × 7 =", calculator.calculate(MultiplyOperation(), 3, 7))  // "21.0"

// ➗ 나눗셈 테스트 (정상)
print("100 ÷ 4 =", calculator.calculate(DivideOperation(), 100, 4))  // "25.0"

// ⚠️ 나눗셈 테스트 (0으로 나누기 예외 처리)
print("10 ÷ 0 =", calculator.calculate(DivideOperation(), 10, 0))  // "undefined"

// 🏁 나머지 연산 테스트
print("10 % 3 =", calculator.calculate(RemainderOperation(), 10, 3))  // "1.0"

// 💡 제곱 연산 테스트 (새로운 연산 추가)
print("2 ^ 3 =", calculator.calculate(PowerOperation(), 2, 3))  // "8.0"
