Generator stron dla 1osobych dziłanosći

Apliakjca jest bardzo minimalistyczna i prosta, design jest elegancki i nowoczesny 

------- WAZNE ------ 
Zrobić welcome page i menu wyboru tempaltów (jest 1 testwoy)
Po wyborze tempaltu odpala się szczegołowsze menu gdzie można zanaczyć co z danego tempaltu się chce a czego nie, on ma bazowo zaznaczone jakieś elementy

Głowym modleułem jest strona główna, kalendarz oraz strona o mnie <--- To zrobić
ale do wyboru powinny być też inne moduły i podstrony (moduł i podstrona to chyba to samo) 

Edytor to główna aplikacja, strona zawiera się w nim :
<Edytor>
    <Strona>
        <Kalendarz></Kalendarz>
    </Strona>
</Edytor>

Edyotr jest stroną, dlatgeo może edytować "siebie"

# TEMPLATY i Zapis
Kluczowa jest możliwość eksportu storny jako TEMPLATU, 
powinien być to np plik z rozszerzniem ".page" (lub folder by zapsiać użyte multimedia)

Eksportuje to wszytkie ustawinia użyte do stworzenia strony,
jako że strona jest w całości stworzona z naszych modułów, którym nadano jakieś ustawienia, możemy wszytkie te informacje łatwo zapisać, zapisując ustwiania użytych modułów.

W ten sosób możemy proawdzić wersojnowanie strony, po portsu zapsiaywać stronę jako nowy tempalte po zmianach. 

Załadowanie templatu do pustego edytora powinno odtowrzyć stronę bez starty żdanych danych.
------------------------------------------------

# HOME PAGE
na początku pwoien wyświetlić się ekran powitalny, czarne logo na beżowym(lub białym) tle i przycisk stwórz, pod nim mały napis "lub upuść plik" który powinien załadować upouszcozny template

W prawym górym rogu powinno być zaloguj które przeniesie do twojej strony jeśli ją masz,
powinno być też autmatyczne logowanie aby ułatwić życie

Przycisk stówrz otiwera menu wybriania tamepletu (na pocztaku 1 tetsowy)

Po wybrnaiu templatu wyświetla się szczegołowsze menu gdzie można zanaczyć lub odznaczyć moduły(podstrony) i zmienić ich ustawienia.

KAZDY MODÓŁ MA SWOJE USTWAINIA np dla kalendarza :
minimaly odstęp między spotaknami w kalndarzu,
rozdaj zajęć [indywidualne/ grupowe]

Po wybraniu opcji kliknąć OK

następnie powinno nastąpić przejście do strony, bez edycji, po prostu wyświetlić stworzoną stronę z wybarnymi modułami

## i wyśiwtelić wskazówkę na przycisk edytora

edytor powinień mieć mały przycisk w prawym gorym rogu ktory go aktywuje,
pojawia się miniamly toolbox na górze ktory ma tylko najbardziej potrzebne toole, takie jak zmainia orietacji na mobilną itd,

edycja powinna być maksymalnie prosta powinnien wysaoczyć mały czat z agentem AI ktory spyta co chemy zorbić i po wpisaniu powinien zanzaczyć co chce zmienić i wyświtelić 3 możliwe opcje zmiany lub dopytać się o szczegóły.

powinien wyśiwtelić też porzebne do edycji narzędzia np okno do zmiany koloru. Musi ono być proste w obsłudze, efekty muszą być widoczne od razu, musi wykonwać ono 1 funkcjonalość, np zmeiniać kolor wybranego elementu.

Można też klinać na element i napsiac co zmienić, wtedy agent powinien wiedzieć co zostało zaznaczone.

Edytor musi być minimalny, ładny i prosty, ui musi być płynne, zaookroglne i eststyczne 
jest to celowane do użytkowiników którzy cenią sobie profesjonalość (ale mogą nie znać sie na porgramowaniu)

powinno prezenteać 3 mozliwe opcje zeby mogli wybrac i NIE BYLI PRZYTŁOCZENI

edytor pwoonien zapsiaywać zmiany w prostym systemie wersjonownia, np tylko 1 gałąź main aby można było wrócic po zmianaich

# struktura projektu ----- DO OPRAWCOWANIA
opisz jaka struktra apliakcji umożliwi aby kazdy uzwykowik miał sowją prywatną stronę ale główna witryna powinna być naszym generatorem, który wita nowcyh uzywkikch a potem przesyła ich na ich stronę, na pcoztaku nie musi to działac ale musi być na to miejsce 

struktura projektu musi być modułowa i łatwa do modyfikacji.

Aplikacja jest stworzona dla 1osobowych działnosci wiec strony są proste i nie przewiduje się bardzo dużego ruchu.

Główną funckjonalsoćą jest kalendarz integrujacy sie z google kalnadrzem, wyysłanie maili , system rezerwacji i potwerdzanie spotakń, zajecia indywidujane i grupowe( kazde z nich to osobna część klandarza)

KAZDY MODÓŁ MA SWOJE USTWAINIA np :
minimaly odstęp między spotaknami w kalndarzu,
rozdaj zajęć [indywidualne/ grupowe]

na zajecia indywidujlne moze sie zapisać 1 osoba i sa zajete, 
podczas zajecć grupowych właściciel storny jest zajęty ale
jest to blok na który używkonicy mogą się zapisać wiec jest on dostepny,
powien być mozliwy do ustawinia limit miejsc oraz podanie podstwaych informacji o zajęciach( lokalizacja lub np że online [POTEM to wtedy link do spotkania na google np])

# DO OPRACOWANIA

1 backend dla nas zaawansowy ?

bakcend dla kaxdego uzywkowika ?

Czy każdy użytkowik musi mieć pełen backend i forntend z edytorem, czy zbyt nie spowolni to stron i czy jest to potzrbne ?

# roziwązanie
czy może że strona jest hostawana z ostaniej(najnowszej) wersji strony stworzonej w edytorze ale edtor działa tylko u nas a link na stronie przenosi admina do naszego edytora gdzie może zmieniać swoją stronę.

wtedy każdy może mieć własny mały backend i frontend (w trybie produkcyjnym)
a edycja bedzie działała u nas (w trybie deloperskim, co daje hot realod - zmiany są widoczne od razu)

Po skończeniu edycji następuje relunch prawdziwej strony z nową wersją