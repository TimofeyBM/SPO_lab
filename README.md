# Команды в командной строке

## 1. `grep` команды:

### a) `grep -v '/bin/bash$' /etc/passwd`

Команда `grep -v '/bin/bash$' /etc/passwd` используется для поиска строк в файле `/etc/passwd`, которые **не** оканчиваются на `/bin/bash`. Это полезно для фильтрации пользователей, использующих не оболочку `/bin/bash`.

### b) `netstat -tanpl | grep 'LISTEN'`

Команда `netstat -tanpl | grep 'LISTEN'` используется для отображения всех сетевых портов, на которых серверы ожидают входящих подключений (слушают порты) на вашей системе.

### c) `grep 'an' file1.txt`

Команда `grep 'an' file1.txt` используется для поиска строк в файле `file1.txt`, которые содержат последовательность символов "an".

## 2. `grep` и `sed` команды:

### a) `grep -w 'do' sample.txt`

Команда `grep -w 'do' sample.txt` ищет слово "do" с точным совпадением в файле `sample.txt`.

### b) `grep -i 'he' sample2.txt | grep -E 'Hi|World'`

Команда `grep -i 'he' sample2.txt | grep -E 'Hi|World'` выполняет два поиска в файле `sample2.txt`, фильтруя строки, содержащие "he" и затем ищет "Hi" или "World" в отфильтрованных результатах.

### c) `grep -F 'Fruit[3' code.txt`

Команда `grep -F 'Fruit[3' code.txt` ищет строку 'Fruit[3' в файле `code.txt` без интерпретации `[` как специального символа.

## 3. `sed` команды:

### a) `sed -i 's/5/five/'`

Команда `sed -i 's/5/five/'` использует утилиту `sed` для замены всех вхождений символа '5' на слово 'five' в файле.

### b) `sed -i 's/0xA0/0x50/g; s/0xFF/0x7F/g' hex.txt`

Команда `sed -i 's/0xA0/0x50/g; s/0xFF/0x7F/g' hex.txt` выполняет замену '0xA0' на '0x50' и '0xFF' на '0x7F' в файле `hex.txt`.

### c) `sed 'y/aeiou/AEIOU/' file.txt`

Команда `sed 'y/aeiou/AEIOU/' file.txt` транслитерирует строчные гласные (aeiou) в заглавные (AEIOU) в файле `file.txt`.
