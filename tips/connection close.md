# JAVA connection close
close()  
자원 낭비를 방지, 불필요하게 connection을 잡고 있지 않도록 잘 닫아주자.

##### 순서!
연 순서대로 안쪽부터 순서대로 잘 닫아주자.

#### Exception 주의
execute 또는 try-catch-finally 사용 시 exception으로 튕겨나가 의도치 않게 close가 안 될 수 있으므로 잘 챙겨서 닫아주기.  
```
if(null!=response){
  connection.close();
}
```

### JAVA 7 이상
try-with-resource를 사용하자..! 
java 9 이상부터는 try 블록 밖에서 선언된 객체(자원)도 참조할 수 있다.


#### connection pool 설정
버전에 따라 속성명이 다름  
tomcat9 / redis 2.7.X? (확인필요)  
maxActive -> maxTotal
maxWait -> maxWaitMilles
