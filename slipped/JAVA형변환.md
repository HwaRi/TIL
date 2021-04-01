# JAVA의 자료형 간 변환

#### String -> char
- charAt(idx): 특정 위치의 char를 가져올 때  
idx는 0부터
```
String s = "This is String";
char c = s.charAt({index});
```
- toCharArray(): string 전체를 char Array로 가져올 때
```
String s = "This is String";
char[] charArr = s.toCharArray();
```

#### char -> String
- String.valueOf()
```
char c = 'c';
String s1 = String.valueOf(c);

char[] charArr = {'c','h','a','r'};
String s2 = String.valueOf(charArr);
```
- toString()
```
char c = 'c';
String s = Character.toString(c);
```
- +""
```
char c = 'c';
String s = c+"";
```

###### valueof vs toString vs ""
https://docs.oracle.com/javase/8/docs/api/java/lang/String.html#valueOf-java.lang.Object-

- null (추가 확인 필요)
  - valueOf -> "null"
  - toString -> NPE
- 성능
