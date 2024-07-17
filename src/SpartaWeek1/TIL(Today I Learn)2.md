# 스파르타 코딩 2일차 
오전에 어제 다 못들은 웹개발(프론트)을 다 들었다. 남은 강의 수가 몇 없어서 다행히 금방 끝날수 있었다. 
오전에 남은 시간은 프로그래머스의 알고리즘 문제들을 풀었다. 

-오늘 공부한것
1. 웹강의 4주차, 5주차 마져 듣기
2. 알고리즘 풀기
3. 웹강의 2회독하기
---
### 알고리즘 문제 7~ 12
- 7번 문제 두수의 나눗셈 
```
class Solution {
    public int solution(int num1, int num2) {
        int answer = 0;
        
        double num3 = ((double)num1/num2);
        answer = (int)(num3*1000);
        
        return answer;
    }
}
```
- 8번 문제 각도기
```
class Solution {
    public int solution(int angle) {
        int answer = 0;
        
        if(0<angle && 90>angle) {
            answer = 1;
        }else if (90 == angle) {
            answer = 2;
        }else if (90 < angle && 180 > angle) {
            answer = 3;
        }else
            answer = 4;
        
        return answer;
    }
}
```

-9번 문제 짝수의 합
```
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for (int i = 0; i <= n; i++) {
            if (i % 2 == 0) {
                answer += i;
            }
        }
        return answer;
    }
}
```

-10번 문제 배열의 평균값
```
class Solution {
    public double solution(int[] numbers) {
        double answer = 0;
        
        for (int i=0; i< numbers.length; i++){
            answer += numbers[i];
            }
        
        return answer/numbers.length;
    }
}
```

-11번 문제 짝수 홀수
```
class Solution {
    public String solution(int num) {
        String answer = "";
        
        if(num == 0 || num % 2 == 0) {
            answer = "Even";
        } else {
            answer = "Odd";
        }
        
        return answer;
    }
}
```

-12번 문제 평균 구하기
```
class Solution {
    public double solution(int[] arr) {
        double answer = 0;
        
        for(int i = 0; i<arr.length; i++) {
            answer += arr[i];
        }

        return answer/arr.length;
    }
}
```
###### 느낀점 - 문제 자체로는 어렵게 다가오지 않았지만, 막상 풀려고 하면 잔실수가 너무 많아 틀리는 경우가 많다. 문법을 알고 있다고 하더라도, 활용을 하거나 세세하게 알지 못한다고 느꼈기 때문에 2주차부터 배울 문법을 복습을 한다고 생각하면서 임하더라도 대충으로 임하지 말고 제대로 임해야 겠다고 느낌. 

---

### 웹개발 1회독
목표는 5주차까지 쭉 달리는 것이지만,,,,,, 2주차 까지 강의 들음,,, 
한번 들었던 거라 속도가 붙을줄 알았것만,,, 그래도 얼추 비슷하게 흉내정도는 낼수 있을거 같다.. 
앞으로 배울 JQuer등 빠르게 달리데 너무 세부적으로 하지말고 그렇다고 대충하지말고 해야할듯 하다

