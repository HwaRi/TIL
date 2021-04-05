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

#### String -> Int, Double, Float, Long, Short
```
String s = "100";

int i1 = Integer.parseInt(s);
int i2 = Integer.valueOf(s);
double d = Double.valueOf(s);
float f = Float.valueOf(s);
long l = Long.parseLong(s);
short sh = Short.parseShort(s);
```

#### Int, Double, Float, Long, Short -> String
```
int i = 100;

String si1 = String.valueOf(i);
String si2 = Integer.toString(i);
String si3 = i+"";

float f = 10.0;

String sf1 = String.valueOf(f);
String sf2 = Float.toString(f);

double d = 10.0;

String sd1 = String.valueOf(d);
String sd2 = Double.toString(d);
```

#### Double, Float, Int
({int, double, float}) <- 캐스팅으로 가능  
int로 캐스탕할 경우 소수점 버림

