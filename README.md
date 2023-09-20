# StudySpringSecurity
SpringSecurity本质上是一个过滤器链
底层就是一系列过滤器链

通过查看 比较典型的过滤器（3个）：
1. FilterSecurityInterceptor 方法级的权限过滤器，基本位于过滤器的最底部
2. ExceptionTranslationFilter 是一个异常过滤器，用来处理认证授权中抛出的异常
3. UsernamePasswordAuthenticationFilter：对login的post请求做拦截，校验表单的用户名密码。