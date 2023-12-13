# bash скрипты

**задание №1**
```bash
if [ -z "$1" ]; then
    echo "Usage: $0 <num>"
    exit 1
fi

num=$1

sum=0

for ((i = 1; i <= num; i++)); do
    sum=$((sum + i))
done

echo "Суммирование от 1 до $num: $sum"
```


**задание №2**
```bash
unique_chars() {

    result=$(echo -n "$1$2" | grep -o . | sort -u | tr -d '\n')


    echo "$result"
}

a="xyaabbbccccdefww"
b="xxxxyyyyabklmopq"
result1=$(unique_chars "$a" "$b")
echo "unique_chars(a, b) -> \"$result1\""

a="abcdefghijklmnopqrstuvwxyz"
result2=$(unique_chars "$a" "$a")
echo "unique_chars(a, a) -> \"$result2\""

```

**задание №3**
```bash
s="Ann:Russel;John:Gates;Paul:Wahl;Alex:Tolkien;Ann:Bell;Lewis:Kern;Sarah:Rudd;Sydney:Korn;Madison:Meta"

s_uppercase=$(echo "$s" | tr 'a-z' 'A-Z' | tr ';' ' ')

pairs=($s_uppercase)

sorted_pairs=($(for pair in "${pairs[@]}"; do echo "$pair"; done | sort -t':' -k2,2 -k1,1))

result=""
for pair in "${sorted_pairs[@]}"; do
    result+="(${pair//:/: })"
done
```