# Tips and useful things for Flutter/mobile developers

**Issue**:

MapBox SDK - методы возвращают Future, но не всегда завершают своё действие, когда Dart метод делает return.

**Solution**

Я вводил искусственые задержки/поллинг нужного параметра, пока тот не изменит своё значение.

**Issue**

`Type 'Null' is not a subtype of type 'InterfaceElement' in type cast [SEVERE] drift_dev on lib/src/*** (cached):`

**Solution**

```
dart run build_runner clean
dart run build_runner build --delete-conflicting-outputs
```

**Issue**

При загрузке иконки svg в мапбокс у неё чёрнный background

**Solution**

Перенести тэг fill в обводку, если это возможно, убрать ненужный rect
