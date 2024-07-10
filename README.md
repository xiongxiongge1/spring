1. 登录
  验证密码时 需要使用md5把传输过来的密码加密后与数据库比较 
 password = DigestUtils.md5DigestAsHex(password.getBytes());

2.异常
  （1） 定义一个基础异常类BaseException继承RuntimeException
  （2） 其他的登录异常 密码错误异常等 继承BaseException
  （3） 在GlobalExceptionHandler中 定义处理捕获到异常的方法 利用多态性质
![image](https://github.com/xiongxiongge1/spring/assets/64593161/2351a263-fc48-4239-bce9-e51edf2f6307)

