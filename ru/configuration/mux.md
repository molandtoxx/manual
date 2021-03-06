---
refcn: chapter_02/mux
refen: configuration/mux
---

# Мультиплексирование

Мультиплексирование или Mux - это использование одного физического TCP-соединения для нескольких виртуальных TCP-соединений.

Мультиплексирование предназначено для уменьшения задержек при установлении соединения (handshake) TCP. Это НЕ повышает пропускную способность. При загрузке больших файлов или измерении скорости, Mux обычно медленнее, чем обычное TCP-подключение.

## MuxObject

```javascript
{
  "enabled": false,
  "concurrency": 8
}
```

> `enabled`: true | false

Включать или нет Mux для исходящих соединений.

> `concurrency`: number

Максимальное количество мультиплексированных соединений, которые может одновременно обрабатывать одно физическое соединение. Максимум: `1024`, минимум: `1`, по умолчанию: `8`.