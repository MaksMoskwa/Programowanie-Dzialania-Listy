📚 Menedżer uczniów — C++

Prosty program konsolowy napisany w języku C++, służący do zarządzania listą uczniów. Program umożliwia dodawanie, wyświetlanie, sortowanie i usuwanie uczniów oraz wczytywanie i zapisywanie danych do pliku tekstowego.

Projekt wykorzystuje podstawowe elementy programowania obiektowego oraz biblioteki standardowe języka C++.

✨ Funkcjonalności

Program posiada interaktywne menu, za pomocą którego można:

📂 wczytać listę uczniów z pliku,
👀 wyświetlić wszystkich uczniów,
💾 zapisać listę uczniów do pliku,
➕ dodać nowego ucznia,
🔤 posortować uczniów alfabetycznie według nazwiska,
🗑️ usunąć ucznia na podstawie numeru,
❌ zakończyć działanie programu.
🛠️ Technologie

Projekt został napisany w:

C++
Biblioteki standardowe:
<iostream> — obsługa wejścia i wyjścia,
<string> — obsługa napisów,
<fstream> — obsługa plików,
<vector> — przechowywanie listy uczniów,
<algorithm> — sortowanie danych.
📋 Struktura programu
struct Uczen

Struktura przechowuje informacje o jednym uczniu:

struct Uczen
{
    string imie;
    string nazwisko;
    int wiek;
};


Każdy uczeń posiada:

Pole	Typ	Opis
imie	string	Imię ucznia
nazwisko	string	Nazwisko ucznia
wiek	int	Wiek ucznia
class Kolekcja

Klasa Kolekcja odpowiada za przechowywanie i obsługę listy uczniów.

Wewnątrz klasy znajduje się:

vector<Uczen> lista_uczniow;


Klasa udostępnia następujące funkcje:

Funkcja	Opis
dodaj_ucznia()	Dodaje ucznia do listy
wczytaj()	Wczytuje uczniów z pliku
zapisz()	Zapisuje listę do pliku
wyswietl()	Wyświetla wszystkich uczniów
sortuj()	Sortuje uczniów według nazwiska
usun_ucznia()	Usuwa ucznia o podanym numerze
📁 Plik z danymi

Program domyślnie korzysta z pliku:

osoby.txt


Każdy uczeń powinien znajdować się w osobnym wierszu, a dane powinny być zapisane w kolejności:

imie nazwisko wiek

Przykładowy osoby.txt
Jan Kowalski 18
Anna Nowak 17
Piotr Zielinski 19
Katarzyna Wisniewska 18


Program podczas wczytywania odczytuje kolejno imię, nazwisko oraz wiek.

▶️ Uruchomienie programu
1. Klonowanie repozytorium
git clone https://github.com/TWOJ_LOGIN/TWOJE_REPOZYTORIUM.git
cd TWOJE_REPOZYTORIUM

2. Kompilacja

Jeżeli korzystasz z kompilatora g++, program można skompilować poleceniem:

g++ main.cpp -o program


Można również określić standard języka C++:

g++ -std=c++17 main.cpp -o program

3. Uruchomienie

Linux / macOS:

./program


Windows:

program.exe

🖥️ Menu programu

Po uruchomieniu programu pojawi się menu:

===== MENU =====
0 - zakoncz program
1 - wczytaj z pliku
2 - wypisz
3 - zapisz do pliku
4 - dodaj ucznia
5 - posortuj
6 - usun ucznia o danym numerze
Wybor:

Opcja 1 — wczytaj z pliku

Wczytuje dane znajdujące się w pliku osoby.txt do aktualnej listy uczniów.

Zmiany są przechowywane w pamięci programu. Aby zapisać je na dysku, należy później wybrać opcję 3.

Opcja 2 — wypisz

Wyświetla wszystkich uczniów znajdujących się aktualnie w kolekcji.

Przykład:

1. Jan Kowalski, 18 lat
2. Anna Nowak, 17 lat
3. Piotr Zielinski, 19 lat

Opcja 3 — zapisz do pliku

Zapisuje aktualną zawartość listy do pliku osoby.txt.

Ta opcja jest potrzebna po dodaniu, usunięciu lub posortowaniu uczniów, jeśli zmiany mają zostać zachowane po zakończeniu programu.

Opcja 4 — dodaj ucznia

Program poprosi o podanie:

Podaj imie:
Podaj nazwisko:
Podaj wiek:


Następnie uczeń zostanie dodany do listy.

Opcja 5 — posortuj

Sortuje uczniów alfabetycznie według nazwiska.

Przykładowo:

Kowalski
Nowak
Zielinski

Opcja 6 — usuń ucznia

Usuwa ucznia na podstawie jego numeru wyświetlanego na liście.

Podanie wartości:

0


anuluje operację usuwania.

🔄 Przykładowy przebieg

Przykładowe użycie programu:

===== MENU =====
0 - zakoncz program
1 - wczytaj z pliku
2 - wypisz
3 - zapisz do pliku
4 - dodaj ucznia
5 - posortuj
6 - usun ucznia o danym numerze
Wybor: 1

Wczytano liste z pliku.


Następnie użytkownik może wyświetlić listę:

Wybor: 2

1. Jan Kowalski, 18 lat
2. Anna Nowak, 17 lat
3. Piotr Zielinski, 19 lat


Można dodać nowego ucznia:

Wybor: 4

Podaj imie: Adam
Podaj nazwisko: Wójcik
Podaj wiek: 18

Dodano ucznia.


Po wykonaniu zmian można użyć opcji 3, aby zapisać aktualną listę do osoby.txt.

🧠 Wykorzystane zagadnienia C++

Projekt wykorzystuje między innymi:

struktury (struct),
klasy i obiekty,
enkapsulację,
wektor std::vector,
operacje na plikach,
instrukcję switch,
pętlę do...while,
funkcje,
referencje,
lambdę,
algorytm std::sort,
usuwanie elementów z std::vector.
⚠️ Ograniczenia

Program jest prostym projektem edukacyjnym i posiada kilka ograniczeń:

imię i nazwisko nie mogą zawierać spacji,
dane są przechowywane wyłącznie w pliku tekstowym,
program korzysta ze stałej nazwy pliku osoby.txt,
program nie posiada rozbudowanej walidacji danych wejściowych,
wielokrotne wczytanie pliku powoduje dodanie danych do istniejącej listy zamiast jej wyczyszczenia,
sortowanie odbywa się wyłącznie według nazwiska.
🚀 Możliwe rozszerzenia

Projekt można rozbudować między innymi o:

wyszukiwanie ucznia po imieniu lub nazwisku,
sortowanie również po wieku i imieniu,
możliwość edycji danych ucznia,
obsługę imion i nazwisk zawierających spacje,
walidację wieku i pozostałych danych,
możliwość wyboru nazwy pliku,
automatyczne zapisywanie zmian,
obsługę większej liczby informacji o uczniu,
zapis danych w formacie CSV lub JSON,
graficzny interfejs użytkownika.
📄 Licencja

Projekt ma charakter edukacyjny i może być wykorzystywany oraz modyfikowany do nauki języka C++.
