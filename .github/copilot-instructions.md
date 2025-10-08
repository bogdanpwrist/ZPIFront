Tworzysz frontend dla :

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
aplikacja powinna płynnie prowadzić użytkowika, wskazówki nie powinny blokować użytkownika tylko lekko wskazywać kierunek.

edytor powinień mieć mały przycisk w prawym gorym rogu ktory go aktywuje,
pojawia się miniamly toolbox na górze ktory ma tylko najbardziej potrzebne toole, takie jak zmainia orietacji na mobilną itd,

edycja powinna być maksymalnie prosta powinnien wysaoczyć mały czat z agentem AI ktory spyta co chemy zorbić i po wpisaniu powinien zanzaczyć co chce zmienić i wyświtelić 3 możliwe opcje zmiany lub dopytać się o szczegóły.

powinien wyśiwtelić też porzebne do edycji narzędzia np okno do zmiany koloru. Musi ono być proste w obsłudze, efekty muszą być widoczne od razu, musi wykonwać ono 1 funkcjonalość, np zmeiniać kolor wybranego elementu.

Można też klinać na element i napsiac co zmienić, wtedy agent powinien wiedzieć co zostało zaznaczone.

Edytor musi być minimalny, ładny i prosty, ui musi być płynne, zaookroglne i eststyczne 
jest to celowane do użytkowiników którzy cenią sobie profesjonalość (ale mogą nie znać sie na porgramowaniu)

powinno prezenteać 3 mozliwe opcje zeby mogli wybrac i NIE BYLI PRZYTŁOCZENI

edytor pwoonien zapsiaywać zmiany w prostym systemie wersjonownia, np tylko 1 gałąź main aby można było wrócic po zmianaich

# Struktura projektu
Głównya witryna to [HOME PAGE] edytora opisnay powyżej,
następnie można się zalogować aby zarządzać swoimi stronami
lub nie logować się i kliknąć przycisk aby rozpocząć tworzenie nowej strony(logowanie potem)

Każdy użytkowik może mieć :
    max 3 strony(frontend) osobiste - (każda na inną działalność)
    1 backend zarządzający wszystkimi stronami
    1 bazę danych zapisującą wszytkie wydarzenia ze wszytkich stron
    (+ jakiś backup jako że chcemy używać darmowych hostingów xd)

Po zalogowaniu do edytora użytkowik zobaczy swoje "Studio" ze stronami i może :
    stworzyć nową stronę i przejść do edycji
    wybrać dowolną ze swoich stron by ją załadować do edytora
    wybrać dowolną ze swoich stron i przejść do niej bez edytora (po prostu link)

Edytor zmienia układ strony, dodaje i usuwa moduły itd. ale każda ze stron ma ten swój panel admina gdzie układa się spotaknia, terminy oraz dostępność, tego NIE ROBI SIE W EDYTORZE.

Struktura projektu musi być modułowa i łatwa do modyfikacji.

Aplikacja jest stworzona dla 1osobowych działnosci wiec strony są proste i nie przewiduje się bardzo dużego ruchu.

Główną funckjonalsoćą jest kalendarz integrujacy sie z google kalnadrzem, system rezerwacji, wysyłanie maili z potwierdzeniami, zajecia indywidujane i grupowe(kazde z nich to osobna część kalendarza)

# Struktura Infrastruktury
strona użytkowika jest hostawana z ostaniej(najnowszej) wersji strony stworzonej w edytorze ale edytor działa tylko u nas a przycisk edycji przenosi go do naszego edytora gdzie może zmieniać swoją stronę.

wtedy każdy może mieć własny mały backend i frontend (w trybie produkcyjnym)
a edycja bedzie działała u nas (w trybie deloperskim, co daje hot realod - zmiany są widoczne od razu)

Po skończeniu edycji następuje relunch prawdziwej strony z nową wersją

Każdy użytkowik może mieć max 3 storny, wszytskie powinny mieć 1 współny bakcend. 
jest to strona osobista więc jeśli użytkowik ma zajęcia yogi od 14 do 15 to na innej swojej stronie gdizie prowadzi np kurs kulinarny jest niedostępny w tym terminie.

Znacznie ułatwia to integracje wielu stron danego użytkownika, mamy 1 backend i 1 baze danych i max 3 frontedny (dla każdej innej działalności). Każdy frontend powinien więc zapisawć do bazy z której strony pochodzi dany wpis, każda strona powinna mieć krótki tytuł np [YOGA] lub [KULINARIA], taki tag, najepiej 1 słowo, niech użytowkik sam to wpisze.