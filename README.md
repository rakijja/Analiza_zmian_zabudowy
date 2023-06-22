# Analiza_zmian_zabudowy
Ten projekt przedstawia część praktyczną wykonaną na potrzeby pracy magisterskiej pt.: 
## "Wyznaczenie przedziału czasowego powstania budynków na podstawie ortofotomapy z użyciem narzędzi głębokiego uczenia"
### STRESZCZENIE
W niniejszej pracy przedstawiono metodę pozyskania danych wektorowych,
zawierających informacje o kształcie i położeniu budynków, na podstawie ortofotomapy, /n
wykorzystując do tego narzędzia głębokiego uczenia. ArcGIS, po skonfigurowaniu środowiska
systemowego i instalacji niezbędnych rozszerzeń, umożliwia przeprowadzanie analiz metodami
głębokiego uczenia. Obiekty wyznaczano poprzez użycie narzędzia geoprzetwarzania Detect
Objects Using Deep Learning na arkuszach ortofotomap, pobranych z Geoportalu,
dla obszarów znajdujących się w granicach miasta Gdyni.
Program, z wykorzystaniem algorytmów opartych na konwolucyjnych sieciach
neuronowych oraz modelu uczącego dostępnego na stronie producenta, pozwolił
na wykrywanie obiektów klasyfikowanych przez algorytm jako budynki, wyznaczał
ich obwiednie tworząc poligony odpowiadające ich dachom i zapisywał je do nowej warstwy
wektorowej. Średnia ufność z jaką wyznaczono takie obiekty wyniosła 89,0%. Po zakończeniu
procesu detekcji dane z kolejnych lat porównano ze sobą, aby znaleźć budynki nowopowstałe.
W tym celu wykryte poligony o nieregularnych kształtach przekształcono w obiekty lepiej
odpowiadające graficznej reprezentacji budynków tj. z prostopadłymi bokami. Następnie,
wykorzystując kolejne narzędzia ArcGIS, obiekty powierzchniowe przekonwertowano w liniowe
i porównano, czy w roku poprzednim w sprawdzanym miejscu występował budynek.
Do zoptymalizowania metody stworzono algorytm w języku programowania Python, który
pozwala na przeprowadzenie procesu porównawczego w sposób półautomatyczny.
Kontrolę dokładności wykonano poprzez porównanie danych wektorowych pozyskanych
z najnowszego zobrazowania (ortofotomapa z roku 2021) z aktualnymi danymi wektorowymi
zawartymi w Bazie Danych Obiektów Topograficznych. Spośród 39442 budynków
wyznaczonych dzięki narzędziom głębokiego uczenia, 3100 miało swój odpowiednik
w BDOT10k. Daje to 77,82% dokładności wyznaczenia budynków co koreluje z ufnością
zadaną podczas ustalania parametrów detekcji na poziomie 75%.

