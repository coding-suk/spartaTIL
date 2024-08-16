# 스파르타 본캠스 24일차 

##### 회고형 TIL19

오늘은 스프링입문 과제 제출날~ 

정말 힘든 기간이었다. 이렇게 스프링 입문 과제를 하나 했을 뿐인데, 왜이렇게 허덕이는건지,,

다들 어렵다고 하고, 나 또한 스프링을 제대로 배워본적이 없고, 첨이다 보니 그럴수 있다고 하는데
그렇지만,,, 상심이 너무 크게 다가온다... 

<figure>
    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS4uSUXxASXDz6nIF3GA291ZWFYFPRKJ62KSw&s">
</figure>

그치만 좀 꺾인다고 포기하기엔 이르다고 생각한다. 

나에게는 어렵든 쉽든 ***그냥 꾸준히 하는 마음***이다. 결국에는 나한테 살이 되는 양분일 꺼니까 말이다!! 

<figure>
    <img src="https://i.pinimg.com/originals/e9/ff/43/e9ff43d208f2aa03912f5040d6074f7b.jpg">
</figure>

제출하고 나서 다락방이라는 특강프로그램이 있어서 수업을 듣고 수업에 관한 과제가 있어서 마무리 
했다. 

### 과제 

[다락방 과제](file:///C:/Users/ASUS/Downloads/%EB%B0%98%EB%B3%B5%EB%AC%B8,%20%EB%B0%B0%EC%97%B4,%20%EC%BB%AC%EB%A0%89%EC%85%98%20%EA%B3%BC%EC%A0%9C.html)

너무 많아서 과제 보여주겠다! 

마무리로 알고리즘 문제 두 문제 풀고 하루를 마무리한다. 

### 알고리즘

- 문자열 다루기
```
class Solution {
    public boolean solution(String s) {
        boolean answer = true;
        
        if(s.length() == 4 || s.length() == 6) { 
            for (int i = 0; i<s.length(); i++) {  
                if (s.charAt(i) < 48 || s.charAt(i) > 57) { 
                    answer = false;
                } 
                
            }
            return answer;
        }
        
        return answer = false;
    }
}
```

- 행렬의 덧셈
```
class Solution {
    public int[][] solution(int[][] arr1, int[][] arr2) {
        int[][] answer = new int[arr1.length][arr1[0].length];
        
        for(int i = 0; i< arr1.length; i++) {
            for(int j = 0; j<arr1[i].length; j++) {
                answer[i][j] = arr1[i][j] + arr2[i][j];
            }
        }
        return answer;
    }
}
```


## 난 할게 너무 많기 때문에 주저않을 시간이 없다!