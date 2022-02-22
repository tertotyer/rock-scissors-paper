# rock-scissors-paper
Универсальная игра камень-ножницы-бумага.

### Описание программы: 
1) В функцию Main от пользователя поступают наименования элементов, учавствующих в данной игре (минимум 3 элемента, должно быть нечетное количество элементов).
2) Происходит генерация и вывод пользователю HMAC ключа, чтобы в дальнейшем пользователю можно было проверить честность данной игры.
3) Происходит ход компьютера, после чего генерируетсся сам HMAC (SHA256) на основе ключа и хода компьютера (ход комьютера пользователю не выводится)
4) После ходит уже сам пользователь.
5) После этих действий выводится сообщение о победе, ничье, либо поражении. Вместе с этим выводится HMAC, что гарантирует честность игры.

### Правила игры: 
  Победным для пользователя считается половина элементов, которые идут после выбранного им элемента (работает по кругу). Соответственно половина перед этим элементом будет считаться победной для системы.

### Пример игры: 
1) Элементы: **rock, scissors, paper, lisard, spoke**
2) Случайным образом система выбирает элемент (допустим это scissors)
3) Пользователь выбирает **rock**

Победными для него будут считаться элементы:  *lisard, spoke*.

Пользователь проиграет, если комьютер выбрал элементы: *scissors, paper*.

В данном случае пользователь проигрывает.