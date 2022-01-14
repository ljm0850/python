#웹 페이지 크롤링

- 조직적,자동화된 방법으로 웹 탐색해서 가져오는것



`$ pip install requests`

`$ pip install beautifulsoup4`



```
import requests

requests.get('URL')
a=requests.get('URL').text
b=requests.get('URL').status_code
```

- requests.get('URL').text
  - URL의 text만 받아옴
- request.get('URL').status_code
  - 응답 확인