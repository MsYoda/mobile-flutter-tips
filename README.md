# Tips and useful things for Flutter/mobile developers

MapBox SDK - методы возвращают Future, но не всегда завершают своё действие, когда Dart метод делает return.
Я вводил искусственые задержки/поллинг нужного параметра, пока тот не изменит своё значение.
