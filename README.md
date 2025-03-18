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

При загрузке иконки svg в мапбокс у неё чёрный background

**Solution**

Перенести тэг fill в обводку, если это возможно, убрать ненужный rect

**Issue**

Необходимо сверстать экран с камерой с помощью пакета camera

**Solution**

Стэк: превью камеры на фоне, поверх рисовать UI

**Issue**

Persinstent bottom sheet не учитывает Safe Area внутри себя, так как сбрасывает MediaQuery.padding

**Solution**

Можно получить эти переменные глобально, с помощью View.of(context)

