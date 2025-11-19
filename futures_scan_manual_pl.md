# Futures Scan – Instrukcja obsługi (PL)

**Wersja dokumentu:** 1.0  
**Aplikacja:** Futures Scan (Android)

---

## 1. Wprowadzenie

Futures Scan to aplikacja do **analizy technicznej i generowania sygnałów** na rynku kryptowalut (kontrakty futures).  
Aplikacja:

- skanuje wybrane pary i interwały czasowe,
- wykorzystuje **wiele filtrów** (Trend, Momentum, Bollinger Bands, RSI, Donchian, MACD, Z-Score, ATR, wolumen, EMA200),
- wyznacza **targety TP1 / TP2 / TP3 oraz SL**,
- obsługuje **logikę retestu**, blokadę sygnałów po SL oraz **pracę w tle**.

> ⚠️ **UWAGA – brak doradztwa inwestycyjnego**  
> Futures Scan NIE jest narzędziem doradztwa inwestycyjnego.  
> Wszystkie decyzje podejmujesz samodzielnie i na własne ryzyko.  
> Handel lewarowany (futures) wiąże się z możliwością utraty całości kapitału.

---

## 2. Wymagania i instalacja

### 2.1. Wymagania

- Telefon / tablet z Androidem (zalecane min. Android 8+).
- Stały dostęp do Internetu (Wi-Fi lub LTE/5G).
- Konto na giełdzie (np. Bybit / inna), jeżeli chcesz realnie handlować – **aplikacja nie wykonuje zleceń za Ciebie**.

### 2.2. Instalacja

1. Zainstaluj aplikację z **Google Play**.
2. Przy pierwszym uruchomieniu:
   - zaakceptuj regulamin / zastrzeżenia,
   - nadaj wymagane uprawnienia (powiadomienia, praca w tle – jeśli chcesz).

---

## 3. Trial i subskrypcje

### 3.1. Okres próbny (Trial)

Po instalacji aplikacja uruchamia **okres próbny** (trial).  
W trakcie triala masz dostęp praktycznie do pełnej funkcjonalności (jak pakiet **ELITE**).

Na ekranie **Ustawienia aplikacji → Subskrypcja** zobaczysz:

- informację, czy trial jest aktywny,
- liczbę dni pozostałych do końca triala.

Po zakończeniu triala:

- jeżeli **nie kupisz subskrypcji**, aplikacja przełączy się w tryb ograniczony (pakiet **NONE**),
- możesz w każdej chwili aktywować płatny pakiet.

### 3.2. Pakiety subskrypcyjne

Aplikacja obsługuje 3 płatne pakiety:

- **BASIC**
- **PRO**
- **ELITE**

Każdy z nich może mieć okresy:
- **1 tydzień** (week),
- **1 miesiąc** (month).

Szczegółowe ceny i dostępne okresy widzisz na **ekranie subskrypcji** – są pobierane bezpośrednio z Google Play.

#### 3.2.1. Pakiet NONE (po trialu, bez subskrypcji)

- Brak pracy w tle.
- Targety: tylko **Fixed** (stałe procenty).
- Limit **1 para**.
- Limit **1 TF na filtr**.
- Brak szczegółów sygnału (ograniczony dostęp).

#### 3.2.2. Pakiet BASIC

- Dozwolony tryb tła: **REST**.
- Targety: **Fixed**.
- Limit: **2 pary**.
- Limit: **2 TF na filtr**.
- Bez szczegółowego widoku sygnału.

#### 3.2.3. Pakiet PRO

- Dozwolone tryby tła: **REST + SMART**.
- Targety: **Fixed + Levels R/S (lokalne wsparcia/opory)**.
- Większa liczba par (np. do 5).
- Bez limitu TF na filtr.
- Włączone szczegóły sygnałów.

#### 3.2.4. Pakiet ELITE

- Wszystkie tryby tła: **REST / LIVE / SMART**.
- Wszystkie tryby targetów (Fixed, **Levels R/S** itd.).
- **Brak limitu TF na filtr.**
- **Brak limitu par.**
- Pełne szczegóły sygnałów.

---

## 4. Ekran „Ustawienia aplikacji”

Wejście: **Menu → Ustawienia aplikacji**.

### 4.1. Praca w tle – Foreground Service

**Przełącznik:** „Praca w tle / skanowanie w tle”

- Po włączeniu aplikacja uruchamia **Foreground Service** (ikonka w pasku statusu).
- Silnik sygnałów działa wtedy niezależnie od tego, czy ekran jest włączony, czy aplikacja jest na wierzchu.

Wymagania:

- Aktywny **trial** lub pakiet BASIC/PRO/ELITE,
- Włączone powiadomienia dla aplikacji.

Jeżeli nie spełniasz warunków, aplikacja pokaże komunikat, że praca w tle jest dostępna tylko w trialu lub z subskrypcją.

### 4.2. Tryb pracy w tle (REST / LIVE / SMART)

W sekcji „Tryb pracy silnika” wybierasz:

- **REST** – odpytywanie danych przez HTTP w interwałach,
- **LIVE** – (jeśli dostępny) tryb bardziej „na żywo” – z użyciem strumieni (np. WebSocket),
- **SMART** – tryb hybrydowy / inteligentny (wybór źródła danych w zależności od sieci, obciążenia itd.).

> Dostępne tryby zależą od pakietu (np. BASIC – tylko REST, PRO – REST+SMART, ELITE – wszystkie).

### 4.3. Powiadomienia

Przełącznik „Powiadomienia”:

- Włącza/wyłącza powiadomienia o nowych sygnałach.
- Na Androidzie 13+ wymagane jest osobne uprawnienie „Wyświetlanie powiadomień” – aplikacja poprosi o nie przy pierwszym uruchomieniu pracy w tle.

### 4.4. Optymalizacja baterii

Sekcja z kartą „Optymalizacja baterii”:

- Pomaga poprawnie skonfigurować system, aby nie ubijał pracy w tle.
- Zalecane:
  - Wyłączyć optymalizację baterii dla Futures Scan,
  - Dopuścić działanie w tle w ustawieniach systemowych (szczególnie na chińskich ROM-ach).

### 4.5. Sekcja Trial / Subskrypcja

Zobaczysz:

- informację o trialu (aktywny / wygasł, ile dni zostało),
- przyciski:
  - **„Zarządzaj subskrypcją”** – otwiera ekran subskrypcji,
  - **„Kup / przedłuż”** – również ekran subskrypcji.

---

## 5. Ekran „Subskrypcja”

Ekran pokazuje **trzy pakiety**: BASIC, PRO, ELITE.

Dla każdego:

- krótki opis (co odblokowuje),
- przyciski:
  - **1 week – [cena z Google Play]**,
  - **1 month – [cena z Google Play]**.

Po kliknięciu:
- uruchamia się standardowe okno zakupu Google Play,
- po udanym zakupie/subskrypcji aplikacja automatycznie zaktualizuje Twój pakiet.

---

## 6. Ekran „Ustawienia sygnałów”

Wejście: **Menu → Ustawienia sygnałów**.

Ekran podzielony jest na dwie zakładki:

- **BASIC** – ustawienia główne,
- **ADVANCED** – wybór interwałów (TF) per filtr.

### 6.1. Zakładka BASIC

#### 6.1.1. Czułość sygnałów (Sensitivity)

**Suwak:** 30–90%

- Określa „jak wymagająca” jest logika generowania sygnałów.
- Niższa czułość (30–40%):
  - mniej filtrów musi się zgodzić,
  - więcej sygnałów, ale bardziej „luźnych”.
- Wyższa czułość (70–90%):
  - więcej filtrów musi wskazywać ten sam kierunek,
  - mniej sygnałów, ale mocniej „wyselekcjonowanych”.

#### 6.1.2. Styl tradingowy

Opcje:

- **Scalping**
- **Day trading**
- **Swing trading**
- **Position trading**

Styl wpływa na **domyślne TF-y filtrów**, targety, retest itp.  
Możesz go zmienić, a aplikacja dopasuje zalecane ustawienia startowe.

#### 6.1.3. Presety

Sekcja presetów pozwala:

- zapisać aktualne ustawienia jako **preset** (przycisk „Zapisz”),
- wybrać preset z listy i **zastosować** go,
- **usunąć** preset.

Przykładowe użycie:

- „Scalp agresywny BTC/ETH”
- „Swing spokojny Altcoiny”

Presety obejmują m.in.: czułość, filtry, targety, retest, TF-y itd.

---

### 6.2. Targety (TP/SL)

Masz dwa tryby:

1. **Fixed (stałe procenty)**  
2. **Levels R/S (lokalne wsparcia/opory)** – w pakietach PRO/ELITE.

#### 6.2.1. Fixed

Ustawiasz ręcznie:

- **TP1, TP2, TP3** (w % ruchu ceny),
- **SL** (w %).

Przykład:

- TP1: `0.6 %`
- TP2: `1.2 %`
- TP3: `1.8 %`
- SL: `0.8 %`

Dla scalpu można ustawiać niższe wartości, dla swingów – wyższe.

##### TP1 final (Scalping)

Opcja: **„TP1 final (scalp)”**

- Jeśli włączona:
  - po osiągnięciu TP1 pozycja jest traktowana jako **zakończona** (statystycznie).
  - Aplikacja liczy wynik jako wyjście w TP1 (bez dalszych targetów).

Przydaje się przy ultra-szybkich scalpach.

#### 6.2.2. Levels R/S (lokalne wsparcia/opory)

Tryb, w którym targety i SL mogą być dopasowywane do **lokalnych poziomów wsparcia / oporu**.

Parametry:

1. **TF dla poziomów R/S**
   - Wybierasz interwał, z którego aplikacja ma wyznaczać poziomy (np. M15 / H1).
   - `Default (from style)` – TF dobierany automatycznie pod styl (Scalp/Day/Swing).

2. **Lookback (liczba świec wstecz)**
   - Zakres danych do szukania swing high/low.
   - Im większy lookback:
     - tym „ważniejsze” i mocniejsze poziomy,
     - ale mogą być dalsze od aktualnej ceny.

3. **Ilość poziomów (1–3)**
   - Ile najważniejszych poziomów wsparcia/oporu ma zostać uwzględnionych jako potencjalne targety.

4. **Tryb pivotów (RsPivotMode)**

   - **Czasowy (Time recent)** – preferuje **najnowsze** pivoty w czasie;
   - **Cenowy (Price nearest)** – preferuje poziomy **najbliższe obecnej cenie**.

   Dzięki temu możesz:
   - skupić się na świeżych reakcjach rynku (czas),
   - albo na poziomach najlepiej pasujących cenowo (cenowo).

> **Uwaga:** Logika R/S jest zaawansowana i na rynku o dużej zmienności nie zawsze idealnie „trafi” w idealne zwroty. To narzędzie pomocnicze, nie wyrocznia.

---

### 6.3. Filtry (włącz/wyłącz)

Każdy filtr możesz osobno:

- włączyć,
- wyłączyć.

Im więcej aktywnych filtrów, tym bardziej wymagająca jest logika sygnału.

Poniżej opis najważniejszych filtrów:

#### 6.3.1. Trend

- Sprawdza, w jakim kierunku porusza się rynek (np. na podstawie średnich kroczących).
- Celem jest filtrowanie sygnałów **pod prąd trendu**.
- Przykład:
  - Trend wzrostowy → aplikacja preferuje sygnały long,
  - Trend spadkowy → preferuje short.

#### 6.3.2. Momentum

- Bada **siłę i dynamikę ruchu** (np. wskaźniki ROC / Rate of Change).
- Może odrzucać sygnały w okresach kompletnej „flaty” (brak ruchu).
- Przydaje się przy scalpie – unikasz wejść w martwy rynek.

#### 6.3.3. Bollinger Bands (BB)

- Wykorzystuje **kanały Bollingera** do oceny położenia ceny:
  - „wyjście” z kanału,
  - zachowanie przy odchyleniach standardowych.
- Może służyć do:
  - wychwytywania wybicia,
  - lub mean-reversion (zależnie od kombinacji z innymi filtrami).

#### 6.3.4. RSI

- Klasyczny **Relative Strength Index**.
- Pomaga odfiltrować:
  - skrajne wykupienie,
  - skrajne wyprzedanie,
  - lub brak dynamiki.

#### 6.3.5. Donchian Channel

- Kanał oparty na **maksimach/minimach z określonego okna czasowego**.
- Przydatny do wyznaczania wybicia z zakresu (breakouty).

#### 6.3.6. Slope

- „Nachylenie” ceny / trendu.
- W praktyce: czy ruch jest wystarczająco zdecydowany, by warto było wchodzić.

#### 6.3.7. MACD

- Wskaźnik MACD (Moving Average Convergence Divergence).
- Używany do:
  - potwierdzania kierunku ruchu,
  - unikania wejść przeciwko mocnemu sygnałowi MACD.

#### 6.3.8. Z-Score

- Statystyczny wskaźnik odchylenia od średniej.
- Pomaga wykryć **odstające** poziomy ceny (overextended).

#### 6.3.9. ATR Regime

- Wykorzystuje **Average True Range**:
  - jeśli zmienność jest zbyt mała – filtr może blokować sygnały (brak sensu scalpować),
  - przy zbyt dużej – możesz świadomie zrezygnować z wejść (zbyt niebezpiecznie).

#### 6.3.10. Volume Pressure

- Analizuje **wolumen**:
  - czy za ruchem stoi realny handel,
  - czy jest to suchy „pusty” skok.
- Może odrzucać sygnały bez wsparcia wolumenowego.

#### 6.3.11. EMA200 Distance

- Sprawdza odległość ceny od **EMA200** (często traktowanej jako „główny” trend).
- Pozwala unikać wejść ekstremalnie oddalonych od EMA200 (łapanie szczytów/dołków bez kontekstu).

---

### 6.4. Retest

Logika **retestu** pozwala wymusić, aby po wybiciu cena:

- wróciła w określone **pasmo**,
- wykonała **dotknięcie kanału**,
- i dopiero wtedy wygenerowała sygnał.

Dzięki temu możesz ograniczyć fałszywe wybicia.

Parametry:

1. **Tryb retestu**
   - **ENTRY BAND** – klasyczny retest wejścia:
     - cena po wybiciu wraca do pasma wokół poziomu,
     - pasmo określasz w % (np. 0.2–0.5%).
   - **CHANNEL TOUCH** – retest kanału:
     - logika oparta na kanale (np. Donchian / Bollinger),
     - wymaga dotknięcia granicy kanału w zadanym lookbacku.

2. **Retest enabled**
   - Włącza/wyłącza retest jako całość.

3. **Confirm close**
   - Jeżeli włączone:
     - retest jest zaliczany dopiero, gdy **świeca zamknie się** w pasmie/kanale.
   - Jeżeli wyłączone:
     - wystarczy „dotknięcie” knotem (ruch intra-candle).

4. **Breakout bypass**
   - Pozwala przepuścić niektóre silne wybicia **bez retestu** (np. bardzo mocne momentum).

5. **Base TF dla retestu**
   - TF, na którym liczony jest retest (np. M1 / M3 / M5).
   - `Default (from style)` – aplikacja dobiera TF do stylu.

6. **Lookback kanału** (tryb CHANNEL_TOUCH)
   - Okno świec, z którego liczony jest kanał.
   - Większa wartość → szerszy kontekst, ale wolniejsza reakcja.

7. **Pasmo (% – Band)**
   - Szerokość pasma retestu w procentach.
   - Przykład:
     - 0.2% – wymagający retest blisko poziomu,
     - 0.6% – szersze pasmo, większa tolerancja.

8. **Timeout (minuty)**
   - Maksymalny czas (w minutach) od wybicia, w którym ma nastąpić retest.
   - Po przekroczeniu czasu sygnał jest odpuszczany.

Jest też przycisk **„Przywróć domyślne dla stylu”** – przywraca domyślne wartości retestu bazujące na aktualnym stylu (Scalp/Day/Swing).

---

### 6.5. Blokada sygnałów po SL

Sekcja **„Blokada po SL”**:

- Przełącznik – włącza/wyłącza logikę cooldownu po SL.
- Suwak czasu (minuty) – ile czasu po SL na danej parze **nie będą generowane nowe sygnały** w tym samym kierunku.

Pomaga to ograniczyć:

- „flip-flop”,
- zemstę na rynku (seria szybkich strat w tym samym miejscu).

---

## 7. Zakładka ADVANCED – TF dla filtrów

W zakładce **ADVANCED** decydujesz, na jakich **interwałach czasowych (TF)** mają pracować poszczególne filtry.

Przykład:

- Trend: M15 / H1,
- Momentum: M1 / M3,
- Bollinger: M3,
- RSI: M5,
- Donchian: M5 / M15,
- itd.

Każdy filtr ma osobny **Multi TF Picker**:

- po kliknięciu wybierasz jeden lub kilka TF (np. M1, M3, M5),
- pusta lista = użyj domyślnych TF wynikających ze stylu tradingowego.

Limity:

- Pakiet NONE/BASIC – ograniczona liczba TF per filtr (np. 1–2),
- PRO/ELITE – brak limitu (lub wysoki limit).

To miejsce dla bardziej zaawansowanych użytkowników, którzy chcą:

- np. liczyć trend na wyższym TF (H1/H4),
- a wejścia i momentum na niższych (M1/M3).

---

## 8. Ekran główny i historia sygnałów

### 8.1. Lista sygnałów

Na głównym ekranie widzisz listę ostatnich sygnałów:

- para (np. BTCUSDT),
- kierunek (LONG / SHORT),
- cena wejścia,
- targety (TP1/TP2/TP3),
- SL,
- status sygnału:
  - aktywny,
  - trafiony TP1 / TP2 / TP3,
  - BE (Break Even),
  - SL.

### 8.2. Historia

Osobna zakładka lub ekran pokazuje **historię wszystkich sygnałów**:

- czas wygenerowania,
- para,
- wynik (TP/SL/BE),
- dodatkowe informacje diagnostyczne (w miarę rozwoju aplikacji).

---

## 9. Dobór ustawień – wskazówki

To jedynie ogólne wskazówki, nie gotowe „złote ustawienia”.

### 9.1. Start – bez przeginania

Na początek:

- Styl: **Scalping** lub **Day trading**.
- Czułość: okolice **60–70%**.
- Filtry:
  - Włącz: Trend, Momentum, Donchian, BB, RSI, MACD.
  - Na początku możesz wyłączyć Z-Score / ATR / Volume / EMA200, żeby zobaczyć „gołą” logikę.
- Targety: Fixed,
  - TP1: 0.6–0.8%,
  - TP2: 1.2–1.5%,
  - TP3: 1.8–2.5%,
  - SL: 0.8–1.0%.

### 9.2. Testowanie zmian

- Zmieniaj **1–2 rzeczy na raz** (np. tylko TF Donchiana, tylko pasmo retestu).
- Obserwuj **co najmniej kilkadziesiąt–kilkaset sygnałów**, zanim wyciągniesz wnioski.
- Patrz nie tylko na **winrate**, ale też na:
  - relację zysk/strata (R:R),
  - jak sygnały zachowują się w różnych warunkach (trend vs. konsolidacja).

---

## 10. Najczęstsze pytania / problemy

### 10.1. „Nie widzę sygnałów”

Sprawdź:

1. Czy masz wybrane **pary** do obserwacji.
2. Czy praca w tle jest **włączona** (jeśli chcesz skanować w tle).
3. Czy ustawienia filtrów nie są zbyt restrykcyjne:
   - Czułość > 80%,
   - włączone wszystkie filtry na raz,
   - retest z bardzo małym pasmem i krótkim timeoutem.
4. Czy Twoja subskrypcja/trial jest aktywna (w przeciwnym razie praca w tle będzie ograniczona).

### 10.2. „Za dużo SL / słabe PF”

- Spróbuj:
  - zwiększyć czułość (np. z 60% na 70–75%),
  - włączyć więcej filtrów trend/momentum,
  - poszerzyć pasmo retestu lub wydłużyć timeout,
  - dodać **blokadę po SL** na kilka minut.

### 10.3. „Za mało sygnałów”

- Zmniejsz czułość (np. z 80% na 60–65%),
- wyłącz część filtrów (np. Z-Score, ATR, EMA200),
- poluzuj retest (szersze pasmo, dłuższy timeout).

---

## 11. Podsumowanie

Futures Scan jest narzędziem, które:

- łączy szereg klasycznych i zaawansowanych wskaźników,
- pozwala zbudować **własny profil sygnałów** (scalp/dzień/swing),
- daje dużą kontrolę nad:
  - filtrami,
  - targetami,
  - retestem,
  - pracą w tle.

Pamiętaj:

- aplikacja nie gwarantuje zysku,
- to Ty odpowiadasz za zarządzanie kapitałem, dobór dźwigni i psychologię tradingu,
- najlepsze ustawienia powstają z **testów i obserwacji**, a nie z „cudzych magicznych presetów”.