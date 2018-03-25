## Ответ на 27 задачу по R:
```R
a <- c(0, NA, NaN, Inf, -Inf)
is.finite(a)          вернет:  TRUE FALSE FALSE FALSE FALSE
!is.infinite(a)       вернет:  TRUE  TRUE  TRUE FALSE FALSE
```
в 27 ожидаемо is.finite и is.infinite дают FALSE для Not-A-Number

## Ответ на 28 задачу по R:
Эта функция позволяет осуществлять "безопасное" сравнение двух Float-значений. Может принимать допустимую погрешность в качестве третьего необязательного параметра.

## Ответ на 29 задачу по R:

mean(is.na(x)) 
логично, что эта вещь вернет долю Not-A-Number значений:
```R
a <- c(0, NA, NaN, Inf, -Inf)
mean(is.na(a))
вернет:  0.4
```

sum(!is.finite(a)) 
вернет количество значений, которые дали TRUE при вызове !is.finite(a):
```R
a <- c(0, NA, NaN, Inf, -Inf)
sum(!is.finite(a)) 
вернет:  4
```

## Ответ на 30 задачу по R:
```R
x <- c(-Inf, -1, 0, 1, Inf, NA, NaN)

x[-which(x > 0)]
 вернет:  -Inf   -1    0   NA  NaN
 
x[x <= 0]
 вернет:  -Inf   -1    0   NA  NA
```

## Ответ на 31 задачу по R:
```
1 - получим NA
2 - наверно вылетит Exception
```
