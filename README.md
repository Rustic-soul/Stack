# "Stack" 
Проект Stack предназначен для знакомства с типом данных "стек" (stack) и некоторыми инструментами для защиты данных.
Автор: Шляпин Илья ([Rustic-soul](https://github.conm/Rustic-soul))

## Основная информация по проекту:
1. Язык программирования C
2. Автоматизация создания статической библиотеки с помощью bash script

## Методы защиты данных:
В данной реализации стека были использованы следующие методы обеспечения целостности данных:
1. Хеширование хранимых данных: Для контроля за целостностью данных мы применяем хеширование. Каждый элемент, добавляемый в стек, хешируется, и хеш сохраняется вместе с данными. При извлечении элемента из стека мы снова вычисляем хеш и сравниваем его с сохраненным. Если хеши не совпадают, это может указывать на повреждение данных.

2. "Канарейки": Для дополнительной защиты мы используем так называемые "канарейки". Это специальные значения, которые размещаются по краям хранимых данных. Если "канарейка" изменяется (например, из-за переполнения или другой ошибки), это может служить сигналом о проблеме.

3. Хеширование самих "канареек": Для обеспечения целостности "канареек" мы также хешируем их значения. Это позволяет обнаруживать даже скрытые изменения.

4. Дамп данных: В случае порчи данных предусмотрен дамп. Дамп собирает всю информацию о возникших ошибках и предоставляет ее пользователю. Это помогает быстро выявить и исправить проблемы.

## Установка:
1. Склонируйте репозиторий:
   ```sh
   git clone https://github.com/Rustic-soul/Stack.git
   ```
3. Перейдите в директорию проекта:
   ```sh
   cd Stack
   ```
5. Соберите проект
6. Запустите тесты

## Использование:
Скоро!

## Планируется добавить:
1. Сборку с помощью CMake
2. Тестирование с помощью Criterion 

## Внимание:
Этот проект создан в образовательных целях. Не используйте его в критических системах без дополнительного тестирования и анализа безопасности.