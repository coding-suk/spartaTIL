# 스파르타 코딩 3일차 
### 오늘의 목표! 

- 알고리즘 5문제 풀기
- 웹 개발 1회독 마무리
- sql영상 다 듣기




## 알고리즘 문제 

*자릿수 더하기

- 수정전
``` 
import java.util.*;

public class Solution {
    public int solution(int n) {
        int answer = 0;
        ArrayList<Integer> arrN = new ArrayList<>();
        
        while(n > 0) {
            arrN.add(n % 10);
            n /= 10;
        }       
        for(int i = 0; i < arrN.length; i++){
            answer += arrN[i];
            }
        return answer;
    }
} 
```
- 수정후
```
import java.util.*;

public class Solution {
    public int solution(int n) {
        int answer = 0;
        ArrayList<Integer> arrN = new ArrayList<>();
        
        while(n > 0) {
            arrN.add(n % 10);
            n /= 10;
        }
        
        for(int i = 0; i < arrN.size(); i++){
            answer += arrN.get(i);
            }
    
        return answer;
    }
}
```
---

* 약수의 합
```
import java.util.*;
class Solution {
    public int solution(int n) {
        int answer = 0;
        ArrayList<Integer> arr = new ArrayList<>();
        
        if (n < 3000) {
        for (int i = 1; i<=n; i++) {
            if (n % i == 0) { 
                arr.add(i);
            }
        }
        
        for (int j = 0; j < arr.size();j++) {
            answer += arr.get(j);
        }
        }
        
        return answer;
    }
}
```
---
* 나머지가 1이 되는 수 찾기
```
class Solution {
    public int solution(int n) {
        int answer = 0;
        
        for (int i = 1; i <= n; i++) {
            if (n % i == 1) {
                answer = i;
                 return answer;
            }
        }
    }
}
```
---

* x만큼 간격이 있는 n개의 숫자
```
class Solution {
    public long[] solution(int x, int n) {
        long[] answer = new long[n];
        
        for (int i=0; i<n; i++) {
            answer[i] = (long)(i+1) * x;
        }
        return answer;
    }
    
}
```
- 피드백
    - ArrayList와 배열의 구분이 부족했고, 그러다보니 ArrayList에서는 size대신 length를 사용했다.
    - 문법적인 지식을 더 쌓아야 할거 같다

---
## 다짐
내가 속한 조는 늦게 사전강의를 시작해서 사전의 먼저 들어야 하다보니,,, 자습조로 빠져서 진행했다.
그러다 보니 시간적으로 시간이 남아서 강의도 한번 듣고 끝이라기보다 남는 시간을 활용하자라는 생각으로, 몇번 회독을 하고,
목요일이 끝나가는 시점에서 이렇게 끝나는게 너무 아쉬우니 나 혼자서 간단하게나마 페이지를 만들어 보려고 한다. 


## 개인 프로젝트

- 웹 개발 강의에서 배운걸 바탕으로 간단한 소개 페이지?, 또는 블로그 페이지를 제작
    - 댓글 다는거나, 로그인등은 넣지 않을것, 
    - 생각하고 있는건 자동차 드라이브 페이지를 생각중


# 하루를 마무리 하며 
오늘 내가 계획한 1. sql강의 듣기, 2. 알고리즘 풀기, 3. 웹강의 회독중 
알고리즘문제는 5문제로 많이 부족하게 했으며, 강의 회독은 이루어 냈다. 
회독을 하고나니 자신감이 생겨, 이 마음을 바탕으로 작게나마 개인 프로젝트를 만들 생각이며, 
알고리즘 문제는 너무 적게 풀었다는게 상당히 좋지 못한 결과이다. 
무엇보다 sql강의를 시작하지 못했기 때문에 100% 목표를 다 채우지를 못했다. 

3개중 2개를 해냈으니 좀 달성률은 70% 이상이긴 하지만, 좀 더 계획을 세부적으로 세울줄 알아야 하고, 
달성률 또한 100%를 향해 달려가야 할거 같다. 