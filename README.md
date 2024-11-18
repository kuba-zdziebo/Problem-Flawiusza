# Problem Flawiusza
Symulacja problemu Flawiusza
## 1.Kim był Flawiusz?
Józef Flawiusz był rzymsko- żydowskim historykiem żyjącym w I wieku n.e.. 
Miał on zostać wraz z grupą powstańców otoczony w jaskini w trakcie oblężenia Jotopaty. Żołnierze woleli samobójstwo od pojmania, a że żydowskie prawo religijne zabrania odbierania sobie życia, zdecydowali się losować, kto zabije poprzednio wylosowanego, tak długo, dopóki nie pozostanie jeden, który będzie musiał się zabić sam. Gdy, zrządzeniem losu, przy życiu pozostali Flawiusz wraz z jednym z towarzyszy, zdecydowali się oni poddać Rzymianom.
## 2.Historia problemu
Pierwszym, który przekształcił tę historię w problem matematyczny, miał być szesnastowieczny francuski matematyk Claude Gaspard Bachet de Méziriac. Według niego, ustawieni w okrąg żołnierze mieli eliminować co trzeciego spośród siebie. Po Bachecie historia ta była wielokrotnie powtarzana ze zmieniającymi się szczegółami – przykładowo Kaplansky podaje, że powstańców było 40 (wliczając Flawiusza), a eliminowano co siódmego. Flawiusz, postawiony przed problemem, miał szybko policzyć, gdzie musi się ustawić, by przeżyć.
## 3.Jak brzmi problem?
W ogólnej wersji problem brzmi następująco: \
**Na okręgu ustawiamy n obiektów, następnie eliminujemy co k-ty obiekt, tak długo, aż zostanie tylko jeden. Należy wskazać obiekt, który pozostanie.**
## 4.Implementacja problemu w pythonie

### Rekurencyjnie
```python
def flavius_recursively(n,k):
    if n==1:
        return 0
    else:
        return (flavius_recursively(n - 1, k) + k)%n +1
```
### Iteracyjnie
```python
def flavius_iteratively(n, k):
    survivor  = 0
    for i in range(2,n+1):
        survivor =(survivor + k)%i
    return survivor+1
```


