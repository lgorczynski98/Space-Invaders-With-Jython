Projekt którego celem było dodanie do gry Invaders.jar funkcjonalności jaką jest interpreter języka Python przy użyciu biblioteki Jython.

Lista kroków:
1) Uruchamiamy konsolę oraz przy użyciu programu cheatEngine-1.0-SNAPSHOT.jar modyfikujemy plik .jar z grą (która uprzednio została już uzupełniona o jythona) w celu dodania socketów.

w konsoli: java -jar cheatEngine-1.0-SNAPSHOT.jar --i modifiedInvaders.jar --script script.txt --o test.jar

utworzony zostanie plik .jar z jythonem oraz nasłuchujący na porcie 4000. Może to zająć kilka sekund z powodu sporego rozmiaru.

2) Uruchamiamy nowo utworzony plik .jar 

w konsoli: java -jar test.jar

Uruchomiona zostanie gra

Otwieramy nowe okno konsoli oraz uruchamiamy telnet na porcie 4000

w konsoli: telnet localhost 4000

Uruchomiony zostanie program telnet przesyłający dane na port 4000 localhosta.

3) W oknie telnetu wpisujemy skrypt lub kopiujemy zawartość plików na3.txt, na4.txt, na5.txt. Każdy skrypt powinien kończyć się słowem 'run' w nowej lini co powoduje uruchomienie skryptu (Nie trzeba od nowa uruchamiać telnetu aby uruchomić kolejny skrypt). Podczas pierwszych prób uruchomienia skryptu mogą wystąpić opóźnienia. 

-plik na3.txt zawiera skrypt wyświetlający messageBox z komunikatem "Hello JVM"
-plik na4.txt zawiera skrypt zmieniający pozycję statku gracza o określoną w skrypcie ilość pikseli
-plik na5.txt zawiera skrypt który odczytuje dane pliku o określonej nazwie z katalogu głównego użytkownika (wewnątrz	pliku na5.txt jest to "dane.txt") a następnie odczytane dane przesyla do konsoli z uruchomionym programem telnet.