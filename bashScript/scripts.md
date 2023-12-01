# bash скрипты

**задание №1**
```bash
#!/bin/bash

file_name="example.txt" 
file_name1="example1.txt"

file_info=$(ls -l "$file_name")
file_info1=$(ls -l "$file_name1")

echo "Информация о файле $file_name и $file_name1:"
echo "$file_info"
echo "$file_info1"

```



**задание №2**
```bash
#!/bin/bash

read n

for ((i = 1; i <= n; i++)); do
    for ((j = 1; j <= i; j++)); do
        echo -n "$j "
    done
    echo
done
```




**задание №3**
```bash
#!/bin/bash

read n

c=1

for((i = 1; i <= n; i++)); do
    for((j = 1; j <= i; j++)); do
        echo -n "$c "
        ((c++))
    done
    echo
done
```



**задание №4**
```bash
#!/bin/bash
read n
if ((n >= 1600 && n <= 4000)); then
    if ((i % 4 == 0 && i % 100 != 0)) || ((i % 400 == 0)); then
        echo "Год високосный"
    else
        echo "Год невисокосный"
    fi
else
    echo "Год не входит в диапазон"
fi
```




**задание №5**
```bash
#!/bin/bash
for ((i=1; i<=8; i++)); do
        for ((j=1; j<=8; j++)); do
                if (((i + j) % 2 == 0)); then
                        echo -e -n "\e[47m " " "
                else
                        echo -e -n "\e[40m " " "
                fi
        done
        echo -e -n "\e[0m"
        echo
done



```


**задание №6**
```bash
#!/bin/bash

addLetters() {
  if [ "$#" -eq 0 ]; then
    echo 'z'
    return
  fi
  sum=0

  for letter in "$@"; do
    ascii=$(printf "%d" "'$letter")
    sum=$((sum + ascii - 96))
  done

  sum=$(( (sum - 1) % 26 + 1))
  result=$(printf \\$(printf '%03o' $((sum + 96))))

  echo "$result"
}

```



**задание №7**

```bash 
#!/bin/bash
is_valid_() {
    local ip="$1"
    local reg="^([0-9]|[1-9][0-9]|1[0-9]{2}|2[0-4][0-9]|25[0-5])\.([0-9]|[1-9][>

    if [[ $ip =~ $reg ]]; then
        echo "Действительный адрес"
    else
        echo "Недействительный адрес"
    fi
}

ip_="$1"
is_valid_ "$ip_"
```


