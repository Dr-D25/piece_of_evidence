# 10. Информационные запросы / сканирование (не атаки)

### Запрос 1
```http
?tree=_class,jobs[name,url,builds[number,result,artifacts[fileName,relativePath]]{0,5},jobs[name,url,builds[number,result,artifacts[fileName,relativePath]]{0,5},jobs[name,url,builds[number,result,artifacts[fileName,relativePath]]{0,5}]{0,250}]{0,250}]{0,250}
```
Действие: запрос к Jenkins API для получения структуры сборок (информационный).

### Запрос 2
```http
graphql?query=%7Bversion+repositoriesOrError%7B__typename+...+on+RepositoryConnection%7Bnodes%7Bname+location%7Bname%7D+pipelines%7Bname%7D%7D%7D%7D%7D
```
Действие: GraphQL-запрос для получения версии и репозиториев.

### Запрос 3
```http
/autodiscover.json?@zdi/Powershell
```
Действие: тестовый запрос (возможно, сканирование).

### Запрос 4
```http
/%3Cpath-to-image%3E
```
Действие: запрос с плейсхолдером.

### Запрос 5
```http
/autodiscover.json?@test.com/owa/?&Email=autodiscover/autodiscover.json%3F@test.com
```
Действие: попытка обхода или сканирования autodiscover.

### Запрос 6
```http
/?command=getUserList&serverGroup=MainUsers&c2f=2620
```
Действие: запрос списка пользователей (возможно, легитимный или разведывательный).

### Запрос 7
```http
/model-versions/get-artifact?path=random&name=UGomSw&version=2
```
Действие: запрос артефакта модели (информационный).

### Запрос 8
```http
/fp30reg.dll?XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```
Действие: переполнение буфера / DoS-тест, либо сканирование.

### Запрос 9
```http
/shaper_helix3/js/%27+l+%27
```
Действие: возможная XSS-инъекция (маловероятная атака).

### Запрос 10
```http
/rest/xxxxxxxxxxxxxxx/xxxxxxx?executeAsync
```
Действие: вызов асинхронного REST-метода (неясно).

### Запрос 11
```http
/media/mod_gtranslate/js/%27+get_flag_src(current_lang)+%27
```
Действие: вероятная XSS.
