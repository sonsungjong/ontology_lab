https://data.seoul.go.kr 의 서울시 실시간 인구데이터
jdk 21 이상
https://jena.apache.org
fuseki-server --mem /fc


[Linux test]
curl -NsS http://sonsungjong.iptime.org:30000/v1/chat/completions \
  -H 'Content-Type: application/json' \
  -H 'Authorization: Bearer qwen38' \
  -d \
  '{
  "model": "qwen38-flash",
  "messages": [
    {
      "role": "user",
      "content": "안녕"
    }
  ],
  "stream": false,
  "max_tokens": 4096,
  "chat_template_kwargs": {
    "enable_thinking": false
  }
}'

[Windows cmd test]
curl.exe -N -sS http://sonsungjong.iptime.org:30000/v1/chat/completions -H "Content-Type: application/json" -H "Authorization: Bearer qwen38" --data-binary "{\"model\":\"qwen38-flash\",\"messages\":[{\"role\":\"user\", \"content\":\"Hello. Answer the korean.\"}],\"stream\":false, \"max_tokens\":4096,\"chat_template_kwargs\":{\"enable_thinking\":false}}"