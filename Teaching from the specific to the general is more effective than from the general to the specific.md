- `date created:` `=dateformat(this.file.ctime, "yyyy-MM-dd HH:mm")`
- `date modified:` `=dateformat(this.file.mtime, "yyyy-MM-dd HH:mm")`
- `tags:` #Claim 
- `parents:` [[Claims (to verify)]]

***

> [!tip] Claim
> Uczenie od szczegółu do ogółu jest efektywniejsze niż od ogółu do szczegółu.

***

# Edukacja

Wyobraź sobie, że jesteś w szkole na matematyce i nauczyciel uczy logarytmów. Wygląda to zapewne mniej więcej następująco:

- będziemy się dziś uczyć logarytmów
- logarytmy działają tak i tak
- wzory są takie i takie
- tu są zadanka, zróbcie zadanka
- (jeśli nauczyciel się postara) logarytmy są stosowane po to, żeby ...

Przez cały proces nauki nie masz pojęcia po co te logarytmy są Ci potrzebne. To jest do niczego nie potrzebne, więc po co się tego uczyć? Po co się tak wytężać? No właśnie. Bez sensu.

A jak by to mogło być zrobione inaczej? Zobaczmy:

- wyobraź sobie, że jesteś XVII wiecznym astronomem
- chcesz policzyć odległości między planetami a Słońcem
- po drodze musisz kilkukrotnie wykonać mnożenie bardzo dużych liczb (dla przykładu odległość między Ziemią a Słońcem to 149 597 870 700 m)
- jako XVII wieczny astronom nie masz kalkulatora, więc musisz liczyć pod kreskę
- po chwili zmagań zdajesz sobie sprawę z kolosalności zadania i zaczynasz czuć się przytłoczony (jeśli nie wierzysz to spróbuj odległość Ziemi od Słońca pomnożyć razy siebie, czyli wziąć do kwadratu)
- po około 10 minutach nauczyciel przerywa Twoją męczarnię i mówi Ci o sztuczce, która pozwala bardzo szybko uzyskać wynik mnożenia dwóch ogromnych liczb
- chciałbyś poznać tę sztuczkę? pewnie tak, bo inaczej będziesz musiał skończyć działanie pod kreskę
- sztuczka działa z użyciem magicznej funkcji
- magiczna funkcja działa tak i tak, i nazywa się logarytm
- żeby magiczna funkcja przyspieszała nam mnożenie korzystamy sobie z gotowych tablic pokazujących wyniki tej funkcji
- łącząc działanie magicznej funkcji z tablicami sztuczka działa tak i tak
- próbujesz wykonać mnożenie za pomocą tej sztuczki

Pierwsze podejście to podejście <span style="color: #F33;"><b>od początku do końca. Od ogółu do szczegółu. Najpierw rozwiązanie, a potem ewentualnie problem.</b></span> Drugie podejście to podejście <span style="color: #69F;"><b>od końca do początku. Od szczegółu do ogółu. Najpierw problem, potem rozwiązanie. Najpierw potrzeba, potem spełnienie potrzeby.</b></span>

Które byś wolał?

***

# Jedna z najważniejszych lekcji w biznesie wg Steve'a Jobsa

>[!quote]
>Musisz zacząć od tego co chce klient i <span style="color: #69F;"><b>rozpracować drogę wstecz</b></span> do technologii. Nie możesz zacząć od technologii i później zastanawiać się gdzie ją sprzedasz.
>\- Steve Jobs

<details>
    <summary>Oryginał angielski</summary>
    <blockquote>
        You gotta start with the customer experience and work backwards to the technology. You can't start with the technology and try to figure out where you're gonna try to sell it.
    </blockquote>
</details>

W tym przypadku łatwo znaleźć kontrsytuację, gdzie niektóre osoby jednak muszą zacząć od technologii. Weźmy np. naukowca, który szuka grawitonu, czyli cząstki pola grawitacyjnego. Nie umiemy sobie wyobrazić na co ona może się przełożyć dla klientów. Ktoś jednak powinien się takimi badaniami zajmować.

# Pomyśl o Twoich ulubionych, najbardziej wciągających książkach

Co jest na pierwszej stronie?

Opis świata, postaci, zasad, polityki, religii?

Nie.

Na pierwszej stronie jesteśmy w środku akcji. Coś się dzieje. Prawdopodobnie zaangażowany w akcję jest główny bohater, ale niekoniecznie.

Akcja trwa i w ciągu kilku stron zazwyczaj się skończy.

W trakcie tej akcji poznamy kilka szczegółów, prawdopodobnie imię bohatera i kilka dodatkowych informacji o nim. Kilka detali związanych z akcją, która się działa, być może coś o wrogach bohatera, może o świecie, w jakim toczy się akcja.

Dalsze szczegóły świata i otoczenia poznajemy "przy okazji" wraz z rozwojem akcji. Po kilkudziesięciu, może nawet po stu stronach, zaczynamy mieć klarowny obraz scenerii.

Ale jak to się ma do metody <span style="color: #69F;"><b>od końca do początku</b></span>?

Wyobraź sobie przez moment, że zgodnie z ograniczeniami naszej pamięci roboczej, w której możemy pomieścić naraz 4 elementy, próbujesz zorganizować wszystkie swoje foldery na komputerze tak, aby w żadnym folderze nie było więcej niż 4 pliki lub foldery.

Oczywiście byłyby pewne dozwolone wyjątki, ale na razie je pomińmy.

Wyobraź sobie, że próbujesz to zadanie wykonać <span style="color: #F33;"><b>od początku do końca</b></span>. Główny folder to proste, ale jakie będą Twoje 4 pierwsze foldery? Wymyślisz sobie cztery, ale potem, po kilku godzinach segregowania zdasz sobie sprawę, że jednak nie działa to idealnie. Zmienisz któryś na inny i po kilku kolejnych godzinach znowu coś nie będzie pasowało. Jeśli Twoich plików i folderów jest mega dużo, to takie podejście jest niewyobrażalnym wyzwaniem.

Na swoim przykładzie powiem, że próbowałem to zrobić może nie z folderami, ale ze swoimi notatkami w programie Obsidian. Idea jest bardzo podobna, z tym, że jedna notatka linkuje do innych notatek zamiast układać je w foldery, coś jak na wikipedii.

Chciałem mieć główną notatkę, linkującą do 4 kolejnych notatek, z których te dalej do 4 kolejnych notatek itd. Siedziałem nad tym z pewnością ponad 5 godzin, porównując strukturę notatek do struktury drzewa z coraz to mniejszymi gałęziami, rozważałem jak moje notatki ułożyć chociaż od środkowych gałęzi, bo *"być może jak będę miał kilka podobnego typu środkowych gałęzi to zobaczę podobieństwo i sposób połączenia ich wyższą notatką"*. Nic z tego. Za dużo różnych notatek. Czułem, że mój mózg jest nieadekwatny do takiego zadania.

Po czym w końcu zaświeciła mi się żarówka w głowie.

Może w takim razie zamiast jedna notatka-rodzic linkować do 4 notatek-dzieci, zrobię odwrotnie? Jedna notatka-dziecko linkuje do (zazwyczaj) jednego lub więcej rodziców. Wtedy mogę zacząć od końca, połączyć sobie kilka krańcowych gałązek, co się okazuje banalnie proste, i budować drzewo od małych gałązek do pnia.

Nie muszę zawczasu wiedzieć jakie będą 4 główne foldery - budując drzewo od końca one się same wyłonią.

Tak jak wyłania się świat i głębia postaci w książkach.

<span style="color: #69F;"><b>Od szczegółu do ogółu. Od końca do początku. Od gałązek do pnia.</b></span>

***

# Kłopoty

Człowiek wyewoluował tak, aby się uczyć na konkretnych przykładach. Na podstawie przykładów jego mózg wyciąga wnioski i próbuje określić zasadę działania. Na podstawie kolejnych przykładów zasada działania jest coraz lepiej klarowna dla człowieka. To co jest przydatne dla człowieka to zasada działania. Z czasem zapomina on przykłady, ale zasadę pamięta.

Później staje się nauczycielem i ma nauczyć innych tego co umie.

Powinien uczyć na przykładach, ale ich nie pamięta, więc opowiada o zasadzie działania. Uczniowie się męczą, bo chcą konkretne przykłady.

Jeśli nauczyciel chce uczyć poprzez konkretne przykłady, to musi spędzić sporo czasu wymyślając je. Wymaga to od niego znacznie więcej wysiłku niż podejście <span style="color: #F33;"><b>od ogółu do szczegółu</b></span>. Dlatego też domyślnie skuteczność nauczania jest niska, nawet jeśli nauczyciel jest bardzo dobry w swojej dziedzinie.

Jednym możliwym rozwiązaniem tego problemu jest, aby już na etapie uczenia się nowej rzeczy robić sobie notatki i zapisywać przykłady. Wtedy gdy np. kilka lat później będziemy musieli tego uczyć to odszukamy swoją notatkę z przykładami i mamy wszystko gotowe.

Innym rozwiązaniem, gdy nie mamy takich notatek, jest włożenie wysiłku i przestudiowanie historycznego podłoża danego problemu. Jak wyglądał oryginalny problem i kto go rozwiązał? W jaki sposób? John Napier wymyślił logarytmy w 1614 roku, aby ułatwić obliczenia matematyczne astronomom. Tak naprawdę wymyślił je wcześniej, ale potem spędził 20 lat licząc logarytmy i tworząc tabele logarytmowe. Najlepsze jest to, co się stało niedługo później. Inny matematyk, Henry Briggs, dał Napierowi feedback, który można określić następująco: "Ej stary, te logarytmy to fantastyczna sprawa, ale te tabelki... słuchaj no... te tabelki są do dupy. Poczekaj chwilę, przygotuję lepsze." I faktycznie, przygotował w 3 lata tabele logarytmów, gdzie logarytmy miały podstawę 10, co było znacznie prostsze do obliczeń.

***

# Dwa trafne cytaty Elona Muska

> [!quote]
> Ludzie moim zdaniem nie zastanawiają się "dlaczego uczymy tego i tego?" A powinniśmy ludziom chyba powiedzieć dlaczego ich uczymy tych rzeczy. Bo wiele dzieciaków w szkole jest skonsternowanych, nie wiedzą po co tam są.
> \- Elon Musk

<details>
    <summary>Oryginał angielski</summary>
    <blockquote>
        People I think, don't stand back and say - why are we teaching people these things? And we should tell them, probably, why we're teaching these things. Cause a lot of kids just in school are kinda puzzled as to why they're there.
    </blockquote>
</details>

> [!quote]
> Myślę, że jeśli potrafisz wyjaśnić "po co" coś robimy, to ma to ogromny wpływ na motywację ludzi. Rozumieją sens.
> \- Elon Musk

<details>
    <summary>Oryginał angielski</summary>
    <blockquote>
        I think if you can explain the "why" of things then that makes a huge difference to people's motivation. They understand purpose.
    </blockquote>
</details>

***

# Od ogółu do szczegółu - szersze spojrzenie

Na uczelniach, patrząc nawet na same przedmioty, uczy się <span style="color: #F33;"><b>od ogółu do szczegółu</b></span>, tzn. najpierw matma, całki, teoria, to, tamto, a dopiero na końcu praktyka, której tak naprawdę już nie ma, bo całe 5 lat to tylko teoria.

Gdyby to podejście zastosować do piłki nożnej, to zanim dziecko mogłoby kopnąć piłkę musiałoby nauczyć się fizycznych obliczeń lotu piłki, historii ostatnich 200 lat sportu itd.

Dopiero po paru latach mogłoby obejrzeć pierwszy mecz, a po paru kolejnych zagrać pierwszy raz.

Pokażcie mi dziecko, które będzie chętne w ten sposób uczyć się piłki nożnej.

Ludzie funkcjonują <span style="color: #69F;"><b>od szczegółu do ogółu</b></span>.

Najpierw gramy, zaczyna nam się ta gra podobać (pojawia się zainteresowanie, kontekst), chcemy być coraz lepsi i staramy się wygrać, a dopiero z czasem zaczynamy się zastanawiać które indywidualne aspekty można usprawnić, żeby zwiększyć nasze szanse na wygraną.

***

# Projektowanie odwrotne lekcji/szkolenia (ang. "backward design")

Przykład wykorzystania metody <span style="color: #69F;"><b>od końca do początku</b></span> w projektowaniu lekcji lub szkolenia z książki "Teaching Tech Together" Grega Wilsona.

> *A similar method called backward design works very well for lesson design. This method was developed independently in \[Wigg2005, Bigg2011, Fink2013\] and is summarized in \[McTi2013\]. In simplified form, its steps are:
> 1. ﻿﻿﻿Create or recycle learner personas (discussed in the next section) to figure out who you are trying to help and what will appeal to them.
> 2. ﻿﻿﻿Brainstorm to get a rough idea of what you want to cover, how you're going to do it, what problems or misconceptions you expect to encounter, what's not going to be included, and so on. Drawing concept maps can help a lot at this stage (Section 3.1).
> 3. ﻿﻿﻿Create a summative assessment (Section 2.1) to define your overall goal. This can be the final exam for a course or the capstone project for a one-day workshop; regardless of its form or size, it shows how far you hope to get more clearly than a point-form list of objectives.
> 4. ﻿﻿﻿Create formative assessments that will give people a chance to practice the things they're learning. These will also tell you (and them) whether they're making progress and where they need to focus their attention. The best way to do this is to itemize the knowledge and skills used in the summative assessment you developed in the previous step and then create at least one formative assessment for each.
> 5. ﻿﻿﻿Order the formative assessments to create a course outline based on their complexity, their dependencies, and how well topics will motivate your learners (Section 10.1).
> 6. ﻿﻿﻿Write material to get learners from one formative assessment to the next. Each hour of instruction should consist of three to five such episodes.
> 7. ﻿﻿﻿Write a summary description of the course to help its intended audience find it and figure out whether it's right for them.*  

> *This method helps keep teaching focused on its objectives. It also ensures that learners don't face anything at the end of the course that they are not prepared for.*

> *Reverse design is described as a sequence, but it's almost never done that way. We may, for example, change our mind about what we want to teach based on something that occurs to us while we're writing an MCQ, or re-assess who we're trying to help once we have a lesson outline. However, the notes we leave behind should present things in the order described above so that whoever has to use or maintain the lesson after us can retrace our thinking. \[Parn1986\]*

