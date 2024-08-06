# TIL작성 13일차 

### 오늘 한것 

- 팀원들과 팀프로젝트 참여
- 알고리즘 풀기

팀 프로젝트 발표를 몇일 남겨두고 팀원들과 함께 프로젝트 완성을 위해 오늘도 열심히 참여를 했다. 
프로젝트를 하면서 참으로 신기하게 생각하는건 문제가 되는걸 해결하고 나면 다른 문제가 생기고 
사슬처럼 끊이지 않고 연쇄적으로 발생되는게 참으로 신기하다

우선 점심쯤 되서야 중복된 결과물이 나오는걸 컬랙션의 Set을 사용하여 해결할수 있었고, 다음 문제는 배열의 객체가 
하나씩 생성되어야 하는데 생성되고 그 밑에 생성되고 이 문제를 해결하기 위해 튜터님께 물어보고 해결을 하게 되었다. 

문제는 객체를 생성할때 static을 사용한게 흠 이었다. 
<figure>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQOf7ltYNyYyy9qVzn1Yx99ctz_UdKnWflpVw&s">
</figure>

이렇게 수정을 거치다보니 시간이 정말 빠르게 흐르드라,,,, 

부트캠프를 진행하고 정말 많이 느끼는건 시간이 너무 빠흐게 흐르는게 아깝고,, 제대로 못 살리는 나 자신이 너무 
후,,,,,,,,,,
---
## 일과가 끝나고 알고리즘

- 없는 숫자 더하기 
```
import java.util.stream.IntStream;

class Solution {
    public int solution(int[] numbers) {
        int[] arr = new int[10]; 
        int answer = 0;
        
        for(int i = 0; i < numbers.length; i++) { // numbers의 길이만큼 반복 
            arr[numbers[i]] = 1; // 선언한 arr의 배열에 numbers[i]의 값이 있으면 
            //1을 입력(true라고 하는 듯함) 예로 arr[numbers[5]] = 1; 이런식 
        }

        for (int i = 0; i<arr.length;i++) { // arr의 길이만큼 반복 0~9
            if(arr[i] == 0) {
                answer += i;
            }
        }
        return answer;
    }
}
```
- 배열과 조건문, 반복문을 사용해서 풀었다, 

이 문제를 풀면서 어렵다고 느끼지는 못했지만 잘 풀지는 못했기 때문에 나중에 다시 풀
어봐야 하는 문제다.
---

# 회고  

## 캠프 내에서 보내는 시간을 쓸대업이 버리지 말고 집중해서 더 챙겨야 할거 같다. 