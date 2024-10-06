- `date created:` 2023-09-12 11:52
- `date modified:` `=dateformat(this.file.mtime, "yyyy-MM-dd HH:mm")`
- `tags:` #Strong-Fact 
- `parents:` [[Strong facts]]

***

> [!tip] Fact
>  Grouping elements by 3 or 4 elements is optimal in terms of information finding speed.

***

# Dirlam, 1972

David K. Dirlam calculated how many chunks in memory would be optimal for the fastest information retrieval. We can compare this to folders on a computer and the situation where we need to find a file but have no idea where it is located.

## Numerical Example

For example, if we have 64 elements (files) in memory and all of them are in one "folder," then <span style="color: #F84;"><b>on average</b></span> (statistically), we would have to read $\frac{1 + 64}{2} = 32.5$ file names to find the correct file, and <span style="color: #F33;"><b>at most</b></span> 64 file names.

If we were to divide these 64 files into 2 levels of 8 files each, we would have 8 subfolders with 8 files each. Then, <span style="color: #F84;"><b>on average</b></span> we would need to read $\frac{1+8}{2} + \frac{1+8}{2} = 9$ file or folder names, and <span style="color: #F33;"><b>at most</b></span> $8 + 8 = 16$, which is already much less.

If we go even further and divide these files into 3 levels of 4 elements each, we have 4 folders, each containing 4 subfolders, which in turn contain 4 files each ($4^3=64$). Then, <span style="color: #F84;"><b>on average</b></span> we would need to read $\frac{1+4}{2} + \frac{1+4}{2} + \frac{1+4}{2} = 7.5$ file names, and <span style="color: #F33;"><b>at most</b></span> $4 + 4 + 4 = 12$, so again, even better than with 2 levels.

Let’s go even further and divide it into 6 levels of 2 elements each ($2^6=64$). Then, <span style="color: #F84;"><b>on average</b></span> we would need to read $\frac{1+2}{2} \cdot 6 = 9$ file names, and <span style="color: #F33;"><b>at most</b></span> $2 \cdot 6 = 12$, so this time, the <span style="color: #F84;"><b>average</b></span> number of file names to read is worse than with the division into 4 elements, but the <span style="color: #F33;"><b>maximum</b></span> number of files to read is just as good.

This simple numerical example has demonstrated that there is some optimal way of organising files in folders if our goal is to find the needed file as quickly as possible. Since files and folders are just one example of a place where data is organised, this will be relevant in very many other areas. This might not be so important when one person is looking for one file on his computer, but if **a million** people are looking for concrete information a couple of times a day in a large body of knowledge, it becomes **extremely important** to have this body of knowledge organised as optimally as possible.

## Disclaimer

In terms of memory, if we have 64 files and place them in folders, we end up with more things to remember than before. For example, if we divide these 64 files into 8 folders with 8 files each, we now have 64 files and 8 folder names to remember.

This raises the question: should we count these 8 additional folder names in the pool of things to remember or not?

Dirlam referenced other research and concluded that we should not count these folder names in the pool of things to remember, but he wasn't fully convinced and left the topic somewhat unfinished, subjectively speaking.

His argument for not counting them is: "folders" are like mnemonic devices (memory tricks) that bring order from chaos and improve learning speed and effectiveness, so their impact can be overlooked.

It's hard to agree with that. You could say that remembering various additional things helps in recalling the things we are interested in (advantage), but the need to dedicate more memory is still there (disadvantage). Folders do not really resemble mnemonic devices that much. A simple example of a mnemonic device is a technique that helps you remember long sequences of numbers, such as phone numbers or bank account numbers. In the simplest version, you imagine 3 things for each digit from zero to nine: a person, an action, and an object. Let's assume that:
- zero - Einstein, reading, book
- one - Napoleon, setting fire, cannon
- two - Shrek, hitting, club
- and so on.

When you get a string of numbers, for example, 012 121 201, you group the digits into three-element chunks and get strange scenes:
- 012 - Einstein sets fire to a club
- 121 - Napoleon hits a cannon
- 201 - Shrek reads some text on a cannon

Remembering three weird scenes is much easier than remembering nine digits, and the more digits there are, the easier it is to remember the scenes compared to the numbers.

Additionally, if someone places these scenes in order in a memory palace (another mnemonic technique), they can remember really long sequences of numbers. Masters have memorized three characters, actions, and objects not for each digit, but for each number from zero to 999. This allows them to memorize ridiculously long numbers, like a few thousand digits of pi.

But back to the topic—folder names do not seem to be "like mnemonic devices." If we move away from the analogy of files and folders towards small elements in human memory, such as specific words when learning a new language, a "folder" may take up a similar "amount" of memory as a "word."

We can look at this from another angle, which Dirlam did not address in his publication. In our question, we don't focus on whether version A requires memorizing more elements than version B. The question is solely about the speed of finding information. One possible answer is:

"The fewer chunks memory is divided into, down to a certain minimum (e.g., the number 4):
- the faster information retrieval is <span style="color: #9D5;"><b>(advantage)</b></span>
- but the more additional elements need to be remembered <span style="color: #F33;"><b>(disadvantage)</b></span>."

We are not claiming here that 3 or 4 chunks are always 100% the ideal, best choice. We simply found one specific application where 3 or 4 chunks are the best choice. There may be other applications or aspects where 3 or 4 chunks are not the best choice. To generally determine what number of chunks is best for the human brain, all of these applications or aspects would need to be tested, and weights would have to be assigned depending on the importance of each application, and then the weighted average would need to be checked. This would be interesting and difficult, and especially difficult, because some applications are more important to some people, so the weights could not be truly objective.

Nevertheless, out of curiosity, we also checked what number of chunks is optimal for search speed if category names or "folders" can also be something we are looking for.

One more thought worth considering—regardless of whether we want to include category or "folder" names in the pool of things to remember, the shape of the memory tree is exactly the same. Put another way, using our example—if we have 64 files and place them in 8 subfolders, we have 8 folder names to remember, but it's not like there are suddenly 64 + 8 = 72 elements on the last level of the tree. On the last level, there are still only 64 elements. If we are searching for a folder, not a file, we will statistically find it faster because it is on a higher level of the tree.

## Purely mathematical results

Purely mathematical results refer to answering the question: *"If we determine the function of the average or maximum number of checks depending on how many chunks the memory is divided into, at what chunk size will the function reach its minimum?"*. Here, the result can be a non-integer number, while in the practical results section, the results will concern only integers, as you cannot have memory divided into, for example, 3 and a half elements.

- if <span style="color: #9D5;"><b>additional elements</b></span> (categories - "folders") <span style="color: #9D5;"><b>can be omitted</b></span>
	- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at <span style="color: #69F;"><b>3.59 elements</b></span>
	- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at <span style="color: #69F;"><b>2.72 elements</b></span>
- if <span style="color: #E8F;"><b>additional elements cannot be omitted</b></span>
	- the lowest <span style="color: #F84;"><b>average</b></span> number of checks occurs at <span style="color: #69F;"><b>2.72 elements</b></span>
	- the lowest <span style="color: #F33;"><b>maximum</b></span> number of checks occurs at <span style="color: #69F;"><b>2.72 elements</b></span>

## Wyniki praktyczne

- jeśli <span style="color: #9D5;"><b>dodatkowe elementy</b></span> (kategorie - "foldery") <span style="color: #9D5;"><b>mogą być pominięte</b></span>
	- najniższa <span style="color: #F84;"><b>średnia</b></span> liczba sprawdzeń występuje przy <span style="color: #69F;"><b>4 elementach</b></span>
		- 1 miejsce - <span style="color: #69F;"><b>4 elementy</b></span>
		- 2 miejsce - 3 elementy - 0,9% więcej sprawdzeń
		- 3 miejsce - 5 elementów - 3,4% więcej sprawdzeń
		- 4 miejsce - 6 elementów - 8,3% więcej sprawdzeń
		- 5 miejsce - 7 elementów - 14,0% więcej sprawdzeń
		- 6 miejsce - 2 elementy i 8 elementów - 20,0% więcej sprawdzeń
	- najniższa <span style="color: #F33;"><b>maksymalna</b></span> liczba sprawdzeń występuje przy <span style="color: #69F;"><b>3 elementach</b></span>
		- 1 miejsce - <span style="color: #69F;"><b>3 elementy</b></span>
		- 2 miejsce - 2 elementy i 4 elementy - 5,7% więcej sprawdzeń
		- 4 miejsce - 5 elementów - 13,8% więcej sprawdzeń
		- 5 miejsce - 6 elementów - 22,6% więcej sprawdzeń
		- 6 miejsce - 7 elementów - 31,7% więcej sprawdzeń
- jeśli <span style="color: #E8F;"><b>dodatkowe elementy nie mogą być pominięte</b></span>
	- najniższa <span style="color: #F84;"><b>średnia</b></span> liczba sprawdzeń występuje przy <span style="color: #69F;"><b>3 elementach</b></span>
		- 1 miejsce - <span style="color: #69F;"><b>3 elementy</b></span>
		- 2 miejsce - 2 elementy i 4 elementy - od 4,9% (dla $n = 10$) do 5,6% (dla $n = 10^{12}$) więcej sprawdzeń
		- 4 miejsce - 5 elementów - od 11,9% (dla $n = 10$) do 13,6% (dla $n = 10^{12}$) więcej sprawdzeń
		- 5 miejsce - 6 elementów - od 19,5% (dla $n = 10$) do 22,3% (dla $n = 10^{12}$) więcej sprawdzeń
		- 6 miejsce - 7 elementów - od 27,4% (dla $n = 10$) do 31,3% (dla $n = 10^{12}$) więcej sprawdzeń
	- najniższa <span style="color: #F33;"><b>maksymalna</b></span> liczba sprawdzeń występuje przy <span style="color: #69F;"><b>3 elementach</b></span> - jako że znalezienie nazwy folderu oznaczałoby wykonanie mniejszej liczby sprawdzeń niż maksymalna, to wyniki są tutaj identyczne jak w przypadku, gdy możemy pominąć dodatkowe elementy (kategorie - "foldery")

Otrzymaliśmy 4 różne kategorie wyników, gdzie w trzech wygrał podział na 3 elementy, a w jednej podział na 4 elementy. Najważniejsze kategorie to moim zdaniem te, które dotyczą <span style="color: #F84;"><b>średniej</b></span> liczby sprawdzeń, ponieważ optymalizacja <span style="color: #F84;"><b>średniego</b></span> czasu wyszukiwania oznacza najmniej straconego czasu w życiu czy też np. czasu procesora.

Są zastosowania, gdzie <span style="color: #F33;"><b>maksymalna</b></span> ścieżka mogłaby być najbardziej kluczowa, jeśli np. proces wyszukiwania musi się koniecznie zmieścić w jakimś określonym przedziale czasu, ale to są wyjątkowe przypadki. Jeden, który mam w głowie, to taki, gdzie serwer ma określoną ilość czasu na odesłanie odpowiedzi na zapytanie, bo jeśli tego nie zrobi, to system wyrzuci błąd np. z połączeniem.

W jednej ze <span style="color: #F84;"><b>średnich</b></span> kategorii wygrał podział na 3 (zdecydowanie, bo o około 5%) , a w drugiej podział na 4 (minimalnie, bo o 0,9%). Która z tych dwóch kategorii jest ważniejsza? Nie wiem, być może zależy od konkretnego zastosowania. W przypadku folderów i plików na komputerze normalna jest sytuacja, że w danym folderze np. znajduje się jeden plik (element końcowy) i dwa podfoldery. Tylko w takim niejednorodnym "drzewie" która kategoria wygrywa? Jeśli zawsze interesuje nas plik końcowy, to chyba wygrywa podział na 4. Czasem jednak chcemy znaleźć folder, żeby go np. spakować i wysłać komuś - jeśli ktoś to często robi to wtedy mógłby wygrać podział na 3. Normalnie jednak jest to stosunkowo rzadziej występująca sytuacja niż szukanie pliku, żeby coś z nim zrobić, więc osobiście stawiałbym na podział na 4.

Jako że nie da się w praktyce wprowadzić zasady, że każdy folder musi mieć dokładnie 4 elementy, to jako najlepszą praktyczną zasadę można chyba przyjąć, że folder może mieć maksymalnie 4 elementy (z dopuszczalnymi określonymi wyjątkami - patrz [[Grouping by 3-4 elements = fastest search#Dodatkowe wnioski|Dodatkowe wnioski]]). Jeśli ma 3 elementy to też super. Nawet jeśli ma dwa to już co prawda mniej optymalnie, ale też całkiem dobrze. Jeśli ma jeden to wydaje się bez sensu na pierwszy rzut oka, ale da się wymyślić logiczne uzasadnienie, np. dostaliśmy plik, którego nazwy nie wolno nam zmienić, ale ta nazwa jest myląca lub ciężka do zidentyfikowania co jest wewnątrz pliku. Wtedy możemy sensownie nazwać folder, w którym będzie umieszczony ten jeden plik.

## Matematyka wyników czysto matematycznych

Niech:
- $y_n, y_m$ - <span style="color: #F84;"><b>średnia</b></span> liczba sprawdzonych elementów aż do znalezienia szukanego elementu odpowiednio <span style="color: #9D5;"><b>nie licząc kategorii</b></span> oraz <span style="color: #E8F;"><b>licząc również kategorie</b></span>
- $z_n, z_m$ - <span style="color: #F33;"><b>maksymalna</b></span> liczba sprawdzonych elementów aż do znalezienia szukanego elementu odpowiednio <span style="color: #9D5;"><b>nie licząc kategorii</b></span> oraz <span style="color: #E8F;"><b>licząc również kategorie</b></span>
- $x$ - liczba kawałków, na które się dzieli jeden kawałek - "rodzic"
- $u$ - liczba poziomów pamięci - np. liczba poziomów folderów
- $n$ - całkowita liczba elementów do zapamiętania <span style="color: #9D5;"><b>nie licząc kategorii</b></span> ("nazw folderów")
- $m$ - całkowita liczba elementów do zapamiętania <span style="color: #E8F;"><b>licząc również kategorie</b></span> ("nazwy folderów")
- rodzic - element-rodzic w pamięci - coś jak folder na komputerze, w którym umieszczamy elementy-dzieci, czyli inne foldery lub pliki
- dziecko - element-dziecko w pamięci - coś jak folder lub plik na komputerze, który jest umieszczony w folderze nadrzędnym, który jest elementem-rodzicem

Założenia:
- Elementy w pamięci nie są uporządkowane, więc nie da się przewidzieć, czy na danym poziomie np. pierwszy element to ten, którego szukamy, czy ostatni, czy np. któryś w środku. Jeśli w przypadku folderów i plików, foldery są posegregowane datami w formacie ISO (czyli "YYYY-MM-DD"), to można byłoby szybciej odnajdywać właściwy folder niż czytając nazwy folderów od góry do dołu. Pamięć na ogół jednak tak nie działa, więc musimy założyć, że elementy nie są uporządkowane i szukanie elementu ma charakter losowy, tzn. każdy element ma takie samo prawdopodobieństwo bycia tym właściwym.

### Krok 1 - policzenie $y_n$

Jeśli $x = 4$, czyli jeden rodzic ma 4 dzieci, to <span style="color: #F84;"><b>średnio</b></span> potrzeba 2,5 sprawdzeń, żeby wybrać szukane dziecko. Jest to po prostu średnia arytmetyczna z możliwych liczb sprawdzeń, tzn. może trafimy za pierwszym strzałem, może za drugim itd. ($\frac{1+2+3+4}{4}$). Jako że jest tak na każdym poziomie pamięci, możemy napisać wzór funkcji:
$$ y = \frac{1+x}{2} \cdot u $$
Nie chcielibyśmy jednak, żeby wynik funkcji był zależny od $u$, bo wartość $u$ jest zależna od $x$. Wynik funkcji może jednak być zależny od całkowitej liczby elementów w pamięci, bo ona nie zależy od $x$. 
$$ n = x^u \implies \log_x(n) = u \implies u = \frac{\ln(n)}{\ln(x)} $$
Podstawiając:
$$ y_n = \frac{1+x}{2} \cdot \frac{\ln(n)}{\ln(x)} = \frac{\ln(n)}{2} \cdot \frac{1+x}{\ln(x)} $$
Przyjmując, że $n$ nie jest zmienną, załóżmy $n=64$, żeby sprawdzić jak wygląda wykres tej funkcji:

![[Pasted image 20230823120429.png|300]] ![[Pasted image 20230823120502.png|300]]

Sytuacja, gdzie $x<1$ nas nie interesuje, bo pamięć nie może być mniej niż 1-kawałkowa. Dla $x>1$ widzimy, że wykres $y_n(x)$ ma jedno minimum globalne, czyli dokładnie to, co chcemy znaleźć, albo konkretniej dla jakiego $x$ występuje to minimum globalne.

Aby znaleźć ten $x$, musimy znaleźć miejsce, gdzie pochodna $y_n$ wynosi 0:
$$ (y_n)' = \frac{\ln(n)}{2} \cdot (\frac{1+x}{\ln(x)})' = \frac{\ln(n)}{2} \cdot \frac{1\cdot\ln(x) - (1+x)\cdot\frac{1}{x}}{\ln^2(x)} = $$
$$ = \frac{\ln(n)}{2} \cdot \frac{\ln(x) - (\frac{1}{x}+1)}{\ln^2(x)} $$
$$ (y_n)' = 0 \iff \ln(x) - (\frac{1}{x}+1) = 0 \implies \ln(x) = \frac{1}{x} + 1 $$
Z tego równania nie jest łatwo wyliczyć $x$, ale znając wykresy obu stron równania wiemy, że dla $x>1$ wykresy te się przetną w jakimś punkcie.

![[Pasted image 20230823122627.png|450]]

Idąc na łatwiznę strona wolframalpha.com podaje nam wynik tego równania wynoszący w przybliżeniu 3,59112:
![[Pasted image 20230823122945.png|400]]

Nie idąc na łatwiznę najłatwiej byłoby to programistycznie sprawdzić, tzn. zwiększając $x$ np. co 0,01, sprawdzić gdzie różnica pomiędzy wartościami tych funkcji jest najmniejsza - wyjdzie wtedy 3,59.

Output mojej funkcji:
```
x: 3.57  |  ln(x) = 1.27257  |  1 + 1/x = 1.28011  |  diff = 0.00754
x: 3.58  |  ln(x) = 1.27536  |  1 + 1/x = 1.27933  |  diff = 0.00397
x: 3.59  |  ln(x) = 1.27815  |  1 + 1/x = 1.27855  |  diff = 0.00040
x: 3.60  |  ln(x) = 1.28093  |  1 + 1/x = 1.27778  |  diff = 0.00315
x: 3.61  |  ln(x) = 1.28371  |  1 + 1/x = 1.27701  |  diff = 0.00670
x: 3.62  |  ln(x) = 1.28647  |  1 + 1/x = 1.27624  |  diff = 0.01023
```

### Krok 2 - policzenie $z_n$

Jeśli $x = 4$, czyli jeden rodzic ma 4 dzieci, to <span style="color: #F33;"><b>maksymalnie</b></span> potrzeba 4 sprawdzeń, żeby wybrać szukane dziecko. Jako że jest tak na każdym poziomie pamięci, możemy napisać wzór funkcji:
$$ z = x \cdot u $$
Żeby wynik funkcji nie był zależny od $u$, zmienimy $u$ na $x$ i $n$ tak jak w kroku 1:
$$ n = x^u \implies \log_x(n) = u \implies u = \frac{\ln(n)}{\ln(x)} $$
Podstawiając:
$$ z_n = x \cdot \frac{\ln(n)}{\ln(x)} = \ln(n) \cdot \frac{x}{\ln(x)} $$
Przyjmując, że $n$ nie jest zmienną, załóżmy $n=64$, żeby sprawdzić jak wygląda wykres tej funkcji:

![[Pasted image 20230824112810.png|300]] ![[Pasted image 20230824112841.png|300]]

Sytuacja, gdzie $x<1$ nas nie interesuje, bo pamięć nie może być mniej niż 1-kawałkowa. Dla $x>1$ widzimy, że wykres $z_n(x)$ ma jedno minimum globalne.

Aby znaleźć szukany $x$, musimy znaleźć miejsce, gdzie pochodna $z_n$ wynosi 0:
$$ (z_n)' = \ln(n) \cdot (\frac{x}{\ln(x)})' = \ln(n) \cdot \frac{1\cdot\ln(x) - x \cdot \frac{1}{x}}{\ln^2(x)} = $$
$$ = \ln(n) \cdot \frac{\ln(x) - 1}{\ln^2(x)} $$
$$ (z_n)' = 0 \iff \ln(x) - 1 = 0 \implies \ln(x) = 1 \implies x = e \approx 2,72$$
### Krok 3 - policzenie $y_m$

Aby uwzględnić zapamiętanie kategorii, zmienia się już pierwszy wzór. Żeby wyjaśnić jak to trzeba policzyć, weźmy znowu na przykład $n = 64$ i $x = 4$. Wtedy mamy $u = 3$ poziomy. Jeśli szukamy akurat kategorii, a nie końcowego elementu, to nasze szukanie skończy się wcześniej, np. już na pierwszym poziomie. Dla wizualnego wsparcia spójrzmy na poniższą strukturę pamięci:

```
1
    11
        111
        112
        113
        114
    12
        ...
    13
	    ...
    14
	    ...
2 ...
3 ...
4 ...
```

Na pierwszym poziomie wciąż mamy 4 opcje, czyli średnia liczba wyszukań to podobnie jak wcześniej $\frac{1+4}{2} = 2,5$. Na drugim poziomie mamy 4 standardowe opcje (na powyższym przykładzie np. 11, 12, 13, 14) plus piątą opcję "zero". Opcja "zero" oznacza, że szukaliśmy "folderu, do którego weszliśmy", czyli w powyższym przykładzie element "1". Innymi słowy, wchodząc do folderu o jeden poziom głębiej jedną z możliwych opcji jest zero wyszukań. Wtedy średnia liczba wyszukań na danym poziomie jest średnią arytmetyczną z 0, 1, 2, 3, 4, czyli wynosi 2. Jest tak na wszystkich kolejnych poziomach poza poziomem pierwszym. Wzór na średnią liczbę wyszukań wynosi więc:
$$ y_m = \frac{1+x}{2} + \frac{0 + x}{2} * (u - 1) = \frac{1 + x + xu - x}{2} = \frac{1}{2} + \frac{u}{2} x$$
Tak jak w kroku 1 wzór na $u$ to:
$$ u = \frac{\ln(n)}{\ln(x)} $$
Po podstawieniu:
$$ y_m = \frac{\ln(n)}{2} \cdot \frac{x}{\ln(x)} + \frac{1}{2} $$
Wykres funkcji dla $n = 64$ wygląda następująco:

![[Pasted image 20230825150122.png|300]] ![[Pasted image 20230825150136.png|309]]

Sytuacja, gdzie $x<1$ nas nie interesuje, bo pamięć nie może być mniej niż 1-kawałkowa. Dla $x>1$ widzimy, że wykres $y_n(x)$ ma jedno minimum globalne, czyli dokładnie to, co chcemy znaleźć, albo konkretniej dla jakiego $x$ występuje to minimum globalne.

Aby znaleźć ten $x$, musimy znaleźć miejsce, gdzie pochodna $y_m$ wynosi 0:
$$ (y_n)' = \frac{\ln(n)}{2} \cdot (\frac{x}{\ln(x)})' + (\frac{1}{2})' = \frac{\ln(n)}{2} \cdot \frac{\ln(x) - 1}{\ln^2(x)} $$
$$ (y_m)' = 0 \iff \ln(x) - 1 = 0 \implies \ln(x) = 1 \implies x = e \approx 2,72 $$

### Krok 4 - policzenie $z_m$

To jest najprostsza część. Skoro szukamy <span style="color: #F33;"><b>maksymalnej</b></span> liczby sprawdzonych elementów, to jest ona taka sama jak w kroku 2. Nazwy kategorii znaleźlibyśmy "po drodze", więc nie byłaby to najdłuższa droga przez drzewo możliwości. Wobec tego $z_m = z_n$, a najmniejszą wartość $z_m$ osiągamy dla $x = e \approx 2,72$.

## Matematyka wyników praktycznych

### Krok 1 - optymalizacja $y_n$

Potrzebny jest nam wzór wyznaczony w [[Grouping by 3-4 elements = fastest search### Krok 1 - policzenie $y_n$|kroku 1 wyników czysto matematycznych]], czyli:
$$ y_n = \frac{\ln(n)}{2} \cdot \frac{1+x}{\ln(x)} $$
Podstawiając liczby naturalne od 2 do 9 możemy sprawdzić który realny podział jest najbardziej optymalny. Interesujące jest też jak te wyniki zmieniają się dla różnych wartości $n$, dlatego dla wygody skorzystałem z programowania. Poniższy kod:

```python
from math import log
import pandas as pd


def calculate_chunk_score(n, x):
    score = log(n)/2 * (x + 1)/log(x)
    return f"${score:.2f}$"


interesting_n = [64, 100, 10**4, 10**6, 10**9, 10**12]
interesting_x = list(range(2, 10))
results = []
for x in interesting_x:
    chunk_results = [calculate_chunk_score(n, x)
                     for n in interesting_n]
    results.append(chunk_results)
headers = [f"$n={n}$"
		   for n in r"64 100 10^4 10^6 10^9 10^{12}".split()]
indices = [f"$x={x}$" for x in interesting_x]
print(pd.DataFrame(results,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

generuje taką tabelkę wartości $y_n(x)$:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                        $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                          $9.00$ |                                          $9.97$ |                                          $19.93$ |                                          $29.90$ |                                          $44.85$ |                                          $59.79$ |
|                                          $x=3$ |                                          $7.57$ |                                          $8.38$ |                                          $16.77$ |                                          $25.15$ |                                          $37.73$ |                                          $50.30$ |
| <span style="color: #9D5;"><b>$x=4$</b></span> | <span style="color: #9D5;"><b>$7.50$</b></span> | <span style="color: #9D5;"><b>$8.30$</b></span> | <span style="color: #9D5;"><b>$16.61$</b></span> | <span style="color: #9D5;"><b>$24.91$</b></span> | <span style="color: #9D5;"><b>$37.37$</b></span> | <span style="color: #9D5;"><b>$49.83$</b></span> |
|                                          $x=5$ |                                          $7.75$ |                                          $8.58$ |                                          $17.17$ |                                          $25.75$ |                                          $38.63$ |                                          $51.50$ |
|                                          $x=6$ |                                          $8.12$ |                                          $9.00$ |                                          $17.99$ |                                          $26.99$ |                                          $40.48$ |                                          $53.97$ |
|                                          $x=7$ |                                          $8.55$ |                                          $9.47$ |                                          $18.93$ |                                          $28.40$ |                                          $42.60$ |                                          $56.80$ |
|                                          $x=8$ |                                          $9.00$ |                                          $9.97$ |                                          $19.93$ |                                          $29.90$ |                                          $44.85$ |                                          $59.79$ |
|                                          $x=9$ |                                          $9.46$ |                                         $10.48$ |                                          $20.96$ |                                          $31.44$ |                                          $47.16$ |                                          $62.88$ |

z której dobrze widać jakie wartości $x$ są najbardziej optymalne. Wyznaczmy wzór na wartość o ile procent więcej sprawdzeń wymaga $x_2$ w porównaniu do $x_1$:
$$ \frac{y_{n}(x_2)}{y_{n}(x_1)} \cdot 100\% - 100\% = \frac{\frac{\ln(n)}{2} \cdot \frac{1+x_2}{\ln(x_2)}} {\frac{\ln(n)}{2} \cdot \frac{1+x_1}{\ln(x_1)}} \cdot 100\% - 100\% = $$
$$ = \frac{\ln(x_1)}{\ln(x_2)} \cdot \frac{1+x_2}{1+x_1} \cdot 100\% - 100\% $$
Jak widać $n$ nie wpływa zupełnie na ten procent. Dodając poniższy kawałek kodu:

```python
def calculate_percent_difference(x1, x2):
    # x2 should be worse than x1
    percent = log(x1)/log(x2) * (1+x2)/(1+x1) * 100 - 100
    return f"$+{percent:.1f}\%$"


non_winning_x = [2, 3, 5, 6, 7, 8, 9]
results2 = []
for x in non_winning_x:
    chunk_results = [calculate_percent_difference(4, x)
                     for n in interesting_n]
    results2.append(chunk_results)

results2[2:2] = [results[2]]
print(pd.DataFrame(results2,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

otrzymujemy następującą tabelkę:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                       $+20.0\%$ |                                       $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |
|                                          $x=3$ |                                        $+0.9\%$ |                                        $+0.9\%$ |                                         $+0.9\%$ |                                         $+0.9\%$ |                                         $+0.9\%$ |                                         $+0.9\%$ |
| <span style="color: #9D5;"><b>$x=4$</b></span> | <span style="color: #9D5;"><b>$7.50$</b></span> | <span style="color: #9D5;"><b>$8.30$</b></span> | <span style="color: #9D5;"><b>$16.61$</b></span> | <span style="color: #9D5;"><b>$24.91$</b></span> | <span style="color: #9D5;"><b>$37.37$</b></span> | <span style="color: #9D5;"><b>$49.83$</b></span> |
|                                          $x=5$ |                                        $+3.4\%$ |                                        $+3.4\%$ |                                         $+3.4\%$ |                                         $+3.4\%$ |                                         $+3.4\%$ |                                         $+3.4\%$ |
|                                          $x=6$ |                                        $+8.3\%$ |                                        $+8.3\%$ |                                         $+8.3\%$ |                                         $+8.3\%$ |                                         $+8.3\%$ |                                         $+8.3\%$ |
|                                          $x=7$ |                                       $+14.0\%$ |                                       $+14.0\%$ |                                        $+14.0\%$ |                                        $+14.0\%$ |                                        $+14.0\%$ |                                        $+14.0\%$ |
|                                          $x=8$ |                                       $+20.0\%$ |                                       $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |                                        $+20.0\%$ |
|                                          $x=9$ |                                       $+26.2\%$ |                                       $+26.2\%$ |                                        $+26.2\%$ |                                        $+26.2\%$ |                                        $+26.2\%$ |                                        $+26.2\%$ |

### Krok 2 - optymalizacja $z_n$

Tym razem potrzebny jest nam wzór wyznaczony w [[Grouping by 3-4 elements = fastest search### Krok 2 - policzenie $z_n$|kroku 2 wyników czysto matematycznych]], czyli:
$$ z_n = \ln(n) \cdot \frac{x}{\ln(x)} $$
Mając ten wzór wygenerujemy tabelkę interesujących wyników $z_n(x)$. Możemy użyć tego samego kodu co w kroku 1, zmieniając tylko definicję funkcji:

```python
def calculate_chunk_score(n, x):
    score = log(n) * x/log(x)
    return f"${score:.2f}$"
```

|                                                |                                           $n=64$ |                                          $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                          $12.00$ |                                          $13.29$ |                                          $26.58$ |                                          $39.86$ |                                          $59.79$ |                                          $79.73$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$11.36$</b></span> | <span style="color: #9D5;"><b>$12.58$</b></span> | <span style="color: #9D5;"><b>$25.15$</b></span> | <span style="color: #9D5;"><b>$37.73$</b></span> | <span style="color: #9D5;"><b>$56.59$</b></span> | <span style="color: #9D5;"><b>$75.45$</b></span> |
|                                          $x=4$ |                                          $12.00$ |                                          $13.29$ |                                          $26.58$ |                                          $39.86$ |                                          $59.79$ |                                          $79.73$ |
|                                          $x=5$ |                                          $12.92$ |                                          $14.31$ |                                          $28.61$ |                                          $42.92$ |                                          $64.38$ |                                          $85.84$ |
|                                          $x=6$ |                                          $13.93$ |                                          $15.42$ |                                          $30.84$ |                                          $46.26$ |                                          $69.40$ |                                          $92.53$ |
|                                          $x=7$ |                                          $14.96$ |                                          $16.57$ |                                          $33.13$ |                                          $49.70$ |                                          $74.55$ |                                          $99.40$ |
|                                          $x=8$ |                                          $16.00$ |                                          $17.72$ |                                          $35.43$ |                                          $53.15$ |                                          $79.73$ |                                         $106.30$ |
|                                          $x=9$ |                                          $17.04$ |                                          $18.86$ |                                          $37.73$ |                                          $56.59$ |                                          $84.88$ |                                         $113.18$ |

Wzór na wartość o ile procent więcej sprawdzeń wymaga $x_2$ w porównaniu do $x_1$:
$$ \frac{z_{n}(x_2)}{z_{n}(x_1)} \cdot 100\% - 100\% = \frac{\ln(n) \cdot \frac{x_2}{\ln(x_2)}} {\ln(n) \cdot \frac{x_1}{\ln(x_1)}} \cdot 100\% - 100\% = $$
$$ = \frac{\ln(x_1)}{\ln(x_2)} \cdot \frac{x_2}{x_1} \cdot 100\% - 100\% $$

W tym przypadku $n$ też nie wpływa na procent. Jako że tutaj wygrał podział na 3, konieczna jest zmiana większego kawałka kodu:

```python
def calculate_percent_difference(x1, x2):
    # x2 should be worse than x1
    percent = log(x1)/log(x2) * x2/x1 * 100 - 100
    return f"$+{percent:.1f}\%$"


non_winning_x = [2, 4, 5, 6, 7, 8, 9]
results2 = []
for x in non_winning_x:
    chunk_results = [calculate_percent_difference(3, x)
                     for n in interesting_n]
    results2.append(chunk_results)

results2[1:1] = [results[1]]
print(pd.DataFrame(results2,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

aby otrzymać interesującą nas tabelkę:

|                                                |                                           $n=64$ |                                          $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$11.36$</b></span> | <span style="color: #9D5;"><b>$12.58$</b></span> | <span style="color: #9D5;"><b>$25.15$</b></span> | <span style="color: #9D5;"><b>$37.73$</b></span> | <span style="color: #9D5;"><b>$56.59$</b></span> | <span style="color: #9D5;"><b>$75.45$</b></span> |
|                                          $x=4$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |                                         $+5.7\%$ |
|                                          $x=5$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |                                        $+13.8\%$ |
|                                          $x=6$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |                                        $+22.6\%$ |
|                                          $x=7$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |                                        $+31.7\%$ |
|                                          $x=8$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |                                        $+40.9\%$ |
|                                          $x=9$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |                                        $+50.0\%$ |

### Krok 3 - optymalizacja $y_m$

Wzór wyznaczony w [[Grouping by 3-4 elements = fastest search### Krok 3 - policzenie $y_m$|kroku 3 wyników czysto matematycznych]], czyli:
$$ y_m = \frac{\ln(n)}{2} \cdot \frac{x}{\ln(x)} + \frac{1}{2} $$

Podobnie jak w kroku 2 tutaj również możemy użyć kodu z kroku 1, zmieniając jedynie definicję funkcji:

```python
def calculate_chunk_score(n, x):
    score = log(n)/2 * x/log(x) + 0.5
    return f"${score:.2f}$"
```

i otrzymujemy następującą tabelkę:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                          $6.50$ |                                          $7.14$ |                                          $13.79$ |                                          $20.43$ |                                          $30.40$ |                                          $40.36$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$6.18$</b></span> | <span style="color: #9D5;"><b>$6.79$</b></span> | <span style="color: #9D5;"><b>$13.08$</b></span> | <span style="color: #9D5;"><b>$19.36$</b></span> | <span style="color: #9D5;"><b>$28.79$</b></span> | <span style="color: #9D5;"><b>$38.23$</b></span> |
|                                          $x=4$ |                                          $6.50$ |                                          $7.14$ |                                          $13.79$ |                                          $20.43$ |                                          $30.40$ |                                          $40.36$ |
|                                          $x=5$ |                                          $6.96$ |                                          $7.65$ |                                          $14.81$ |                                          $21.96$ |                                          $32.69$ |                                          $43.42$ |
|                                          $x=6$ |                                          $7.46$ |                                          $8.21$ |                                          $15.92$ |                                          $23.63$ |                                          $35.20$ |                                          $46.76$ |
|                                          $x=7$ |                                          $7.98$ |                                          $8.78$ |                                          $17.07$ |                                          $25.35$ |                                          $37.77$ |                                          $50.20$ |
|                                          $x=8$ |                                          $8.50$ |                                          $9.36$ |                                          $18.22$ |                                          $27.08$ |                                          $40.36$ |                                          $53.65$ |
|                                          $x=9$ |                                          $9.02$ |                                          $9.93$ |                                          $19.36$ |                                          $28.79$ |                                          $42.94$ |                                          $57.09$ |

Wzór na wartość o ile procent więcej sprawdzeń wymaga $x_2$ w porównaniu do $x_1$:
$$ \frac{y_{m}(x_2)}{y_{m}(x_1)} \cdot 100\% - 100\% = \frac{\frac{\ln(n)}{2} \cdot \frac{x_2}{\ln(x_2)} + \frac{1}{2}} {\frac{\ln(n)}{2} \cdot \frac{x_1}{\ln(x_1)} + \frac{1}{2}} \cdot 100\% - 100\% $$

W tym przypadku $n$ wpływa na wynik. Kod do wygenerowania drugiej tabelki jest następujący:

```python
def calculate_percent_difference(n, x1, x2):
    # x2 should be worse than x1
    score1 = log(n)/2 * x1/log(x1) + 0.5
    score2 = log(n)/2 * x2/log(x2) + 0.5
    percent = score2 / score1 * 100 - 100
    return f"$+{percent:.1f}\%$"


non_winning_x = [2, 4, 5, 6, 7, 8, 9]
results2 = []
for x in non_winning_x:
    chunk_results = [calculate_percent_difference(n, 3, x)
                     for n in interesting_n]
    results2.append(chunk_results)

results2[1:1] = [results[1]]
print(pd.DataFrame(results2,
                   columns=headers,
                   index=indices)
      .to_markdown())
```

z którego otrzymujemy:

|                                                |                                          $n=64$ |                                         $n=100$ |                                         $n=10^4$ |                                         $n=10^6$ |                                         $n=10^9$ |                                      $n=10^{12}$ |
| ----------------------------------------------:| -----------------------------------------------:| -----------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:| ------------------------------------------------:|
|                                          $x=2$ |                                        $+5.2\%$ |                                        $+5.2\%$ |                                         $+5.4\%$ |                                         $+5.5\%$ |                                         $+5.6\%$ |                                         $+5.6\%$ |
| <span style="color: #9D5;"><b>$x=3$</b></span> | <span style="color: #9D5;"><b>$6.18$</b></span> | <span style="color: #9D5;"><b>$6.79$</b></span> | <span style="color: #9D5;"><b>$13.08$</b></span> | <span style="color: #9D5;"><b>$19.36$</b></span> | <span style="color: #9D5;"><b>$28.79$</b></span> | <span style="color: #9D5;"><b>$38.23$</b></span> |
|                                          $x=4$ |                                        $+5.2\%$ |                                        $+5.2\%$ |                                         $+5.4\%$ |                                         $+5.5\%$ |                                         $+5.6\%$ |                                         $+5.6\%$ |
|                                          $x=5$ |                                       $+12.7\%$ |                                       $+12.8\%$ |                                        $+13.2\%$ |                                        $+13.4\%$ |                                        $+13.5\%$ |                                        $+13.6\%$ |
|                                          $x=6$ |                                       $+20.8\%$ |                                       $+21.0\%$ |                                        $+21.8\%$ |                                        $+22.0\%$ |                                        $+22.2\%$ |                                        $+22.3\%$ |
|                                          $x=7$ |                                       $+29.2\%$ |                                       $+29.4\%$ |                                        $+30.5\%$ |                                        $+30.9\%$ |                                        $+31.2\%$ |                                        $+31.3\%$ |
|                                          $x=8$ |                                       $+37.6\%$ |                                       $+37.9\%$ |                                        $+39.3\%$ |                                        $+39.8\%$ |                                        $+40.2\%$ |                                        $+40.4\%$ |
|                                          $x=9$ |                                       $+46.0\%$ |                                       $+46.3\%$ |                                        $+48.1\%$ |                                        $+48.7\%$ |                                        $+49.1\%$ |                                        $+49.3\%$ |

### Krok 4 - optymalizacja $z_m$

Wyniki takie same jak w [[Grouping by 3-4 elements = fastest search### Krok 2 - optymalizacja $z_n$|kroku 2]]. Wyjaśnienie w [[Grouping by 3-4 elements = fastest search### Krok 4 - policzenie $z_m$|kroku 4 wyników czysto matematycznych]].

## Dodatkowe wnioski

Podobną optymalizację szybkości wyszukiwania możemy zastosować w wielu innych miejscach.

### Organizacja plików i folderów

Jeśli podzielimy pliki i foldery w taki sposób, że każdy folder zawiera nie więcej niż 4 pliki i foldery, to szybkość odnajdywania tego czego szukamy będzie najwyższa.

Są jednak wyjątki.

Jeśli to jest nasz komputer to niektórych folderów używamy codziennie, więc możemy tutaj sobie pomóc pamięcią długotrwałą, czyli po prostu pamiętać gdzie co jest. Główny folder może zawierać np. 10 folderów typu "Dokumenty", "Nazwa firmy 1", "Nazwa firmy 2", "Prywatne", "Książki", "Kolarstwo", "Łowienie ryb" itd. Zapamiętamy to, więc nie tracimy na prędkości wyszukiwania. Jeśli to jest jednak system plików współdzielony pomiędzy kilkoma osobami, np. kilka osób w firmie pracuje na folderze "Administracja", to wtedy koniecznie powinno się stosować podział na 4, bo pracownicy nie będą mogli sobie tak skutecznie pomagać pamięcią długotrwałą i jak przyjdzie nowy pracownik to będzie mu znacznie łatwiej się odnaleźć.

Drugi wyjątek to folder zawierający bardzo przejrzyście zorganizowane pliki i foldery, np. folder "Finanse" zawierający foldery:
- 2022-01
- 2022-02
- 2022-03
- ...
- 2023-07
- 2023-08
W takim przypadku tych folderów może być nawet setki, a i tak szybko znajdziemy miesiąc, którego szukamy, bo przeskakujemy wiele folderów naraz szukając właściwego, czyli innymi słowy ten system organizacji pozwala nam uniknąć czytania większości nazw folderów.

Trzeci wyjątek to wyszukiwarka systemowa, która zazwyczaj pozwala szybko znaleźć właściwy plik nawet jeśli jest schowany w jakimś dziwnym miejscu. Często jednak:
- ona nie znajduje pliku, który szukamy - możemy wręcz mieć otwarty właściwy folder i widzieć plik i jego dokładną nazwę, wpisać ją do wyszukiwarki, a ona stwierdzi, że takiego pliku nie ma
- nie pamiętamy jak ten plik się dokładnie nazywa

### System IVR, czyli algorytm automatycznej sekretarki

Sytuacja - dzwonisz do Orange i słyszysz:
- jeśli dzwonisz w sprawie X - wybierz 1,
- jeśli w sprawie Y - wybierz 2,
- ...
- jeśli z jeszcze czymś innym - wybierz 9

Przypuśćmy, że wybierasz 4, ale kategoria nie brzmiała dokładnie jak to czego potrzebujesz, więc słuchałeś do końca wszystkie 9 opcji. Po wybraniu 4 znowu słyszysz 9 opcji i znowu żadna nie brzmiała dokładnie jak to czego potrzebujesz, ale stwierdzasz, że najbliżej brzmi opcja 2. Czasami tu się sprawa skończy, a czasami usłyszysz jeszcze kolejne opcje.

Żeby algorytm był najszybszy dla człowieka, na każdym etapie powinny być max 3-4 opcje.

<span style="color: #F33;"><b>Ten jeden algorytm dzień w dzień marnuje tak wielu ludziom tak ogromne ilości czasu, że jest to wręcz niewiarygodne.</b></span> Obstawiam, że jeden dzień pracy jednego człowieka, żeby to poprawić, mógłby zaoszczędzić setki godzin miesięcznie czasu klientów Orange czy innych firm z tego typu centralami telefonicznymi.

### UI, czyli interfejs użytkownika

Weź swój telefon i otwórz ustawienia. Ile masz opcji widocznych już na start? Ja w moim OnePlusie mam <span style="color: #F33;"><b>26</b></span>. Jak wejdę dalej w "Ustawienia systemu" to mam tam <span style="color: #F33;"><b>16</b></span> opcji. Tego typu firmy niby zastanawiają się jak uczynić telefon łatwiejszym w użytkowaniu, a jednak nikt się nie zastanawia nad tym ile opcji może być widocznych dla użytkownika w jednym momencie. iPhone z tego co wiem też ma ustawienia, które mogą mieć na jednym widoku mnóstwo opcji. Wiem, że macbook ma obecnie <span style="color: #F33;"><b>29</b></span> kategorii na pierwszym widoku ustawień (macOS Ventura 13.5.1).

Wystarczyłoby starannie podzielić te ustawienia na sekcje po max 4 elementy każda i wszystko byłoby znacznie łatwiejsze do znalezienia.

Odnośnie walki iPhone'a z androidem słyszałem tego typu argument:
- android daje znacznie więcej opcji konfigurowania telefonu pod swoje potrzeby
- iPhone daje znacznie mniej opcji konfigurowania telefonu, ale te domyślne opcje, których się nie da zmienić, są zazwyczaj bardzo wygodne dla większości użytkowników
- dzięki temu, że iPhone ma mniej opcji konfiguracyjnych, jest łatwiejszy w obsłudze, bo użytkownik nie musi przechodzić przez setki czy nawet tysiące różnych opcji
- mamy tutaj więc sytuację coś za coś, tzn. albo użytkownik może wybrać łatwiejszą obsługę (iPhone), albo większe możliwości konfiguracji (android)

Ale stosując podział na 4 możemy znacznie zwiększyć liczbę dostępnych opcji konfiguracyjnych nie tracąc zupełnie na łatwości obsługi.

To samo możemy zastosować w wielu innych miejscach. Strony internetowe byłyby prostsze dla użytkownika, jeśli stosowałyby podział na 3-4. Np. fajnie by było, gdyby pasek u góry miał 4 opcje, a nie 7. Jeśli firma szkoleniowa ma w ofercie np. 100 szkoleń to fajnie by było, gdyby nie były wrzucone do jednego wora, tylko były uporządkowane w kategorie i podkategorie po 3-4 elementy.

***

# Bibliografia

1. Dirlam, D. K. (1972). Most efficient chunk sizes. _Cognitive Psychology, 3_(2), 255–359. [https://doi.org/10.1016/0010-0285(72)90012-6](https://psycnet.apa.org/doi/10.1016/0010-0285(72)90012-6)

