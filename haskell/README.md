# IUK5_M_3_TERM_KHROMOV

## Задача 1.1. Посчитайте в GHCi: 2123.

```
ghci> 2^123
10633823966279326983230456482242756608
```

## Задача 1.2. Измените код каждой из функций в файле first_prog.hs, тестируя их в GHCi в процессе модификации, а затем скомпилируйте новую версию программы для генерации шаблонов электронных писем, указав email в качестве имени исполняемого файла

```hs
toPart recipient = "Дорогой " ++ recipient ++ "!\n"

bodyPart bookTitle = "Спасибо за то, что купили \"" ++ bookTitle ++ "\"!\n"

fromPart author = "С уважением,\n" ++ author

createEmail recipient bookTitle author = toPart recipient ++ bodyPart bookTitle ++ fromPart author

main = do
  putStrLn "Кто получатель этого письма?"
  recipient <- getLine
  putStrLn "Название книги:"
  title <- getLine
  putStrLn "Кто автор этого письма?"
  author <- getLine
  putStrLn (createEmail recipient title author)
```

```
ghc .\task1_2.hs -o email.exe
[1 of 2] Compiling Main             ( task1_2.hs, task1_2.o )
[2 of 2] Linking email.exe
```
