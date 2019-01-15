# 정렬 > 가장 큰 수
```java
/*문자열로 비교  a+b    
1. 자리수 같을때 
2. 다를 때: 합해서
*/
import java.util.*;

class Solution {
    public String solution(int[] numbers) {
        String answer = "";
        Strnng[] nums = new String[numbers.length]; //String배열 준비
        
        for(int i=0; i<num.length; i++){
            nums[i] = String.valueOf(numbers[i]);
        }//문자열로 바꿔서 넣기
        
        Arrays.sort(nums, new Mycomp());
        if(num[0].equals("0"))
            answer +="0"; //????? 
        else{
            for(int j=0; j<num.length; j++){ answer += num[j];}
        }
        return answer;
    }
}


class Mycomp implements Compartor<String>{
        public int compare(String o1,String o2){
                return (o2+o1).compareTo(o1+o2);
        }
} //비교 ->정렬 (큰 수 부터 넣기위해..)



```


```java
//List, 람다로 풀기
List<Integer> list = new ArrayList<>(); for(int i = 0; i < numbers.length; i++) {   list.add(numbers[i]);
        } // 리스트에 입력배열 넣기


 Collections.sort(list, (a, b) -> {
     String as = String.valueOf(a), bs = String.valueOf(b); //모두문자열로..
      return -Integer.compare(Integer.parseInt(as + bs), Integer.parseInt(bs + as));
        });  //문자열 더해서, 정수값으로 비교.. 


StringBuilder sb = new StringBuilder(); //스트링빌더=class임 등장...? 문자열인데 가변크기, 이 안에서 다 해결 
    for(Integer i : list) {
         sb.append(i);   //스트링빌더에 리스트값을 다 넣기..
         
          answer = sb.toString();  //답은 스트링빌더값을 string으로 
          
          
          
 if(answer.charAt(0) == '0') {
            return "0";   //만약 답이 0이면, 0리턴

     }else {
            return answer;  //아니면 스트링빌더로 만든 answer 값 리턴 
        }
```

        

compare : 기본 정렬
**comparator : 외 다른 기준 정렬**

_ _ _









