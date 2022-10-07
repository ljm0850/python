# Requests

```python
# https://requests.readthedocs.io/en/latest/

# 1
r = requests.get('https://api.github.com/user', auth=('user', 'pass'))
# 2
payload = {'key1': 'value1', 'key2': 'value2'}
r = requests.get('https://httpbin.org/get', params=payload)
print(r.url) # https://httpbin.org/get?key2=value2&key1=value1

r.status_code
200
r.headers['content-type']
'application/json; charset=utf8'
r.encoding
'utf-8'
r.text
'{"type":"User"...'
r.json()
{'private_gists': 419, 'total_private_repos': 77, ...}

r = requests.post('https://httpbin.org/post', data={'key': 'value'})
r = requests.put('https://httpbin.org/put', data={'key': 'value'})
r = requests.delete('https://httpbin.org/delete')
r = requests.head('https://httpbin.org/get')
r = requests.options('https://httpbin.org/get')
```

- `requests.get(주소, auth, params)`
  - 주소에 auth, params를 넣어 GET  방식 요청