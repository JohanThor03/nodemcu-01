# nodemcu-01
## Förstå Blink i arduino
Med hjälp av arduino så kan man relativt enkelt skapa program som kan användas både för mer komplicerade prylar, men även väldigt simpla system. Ett arduinosystem är dessutom enkelt att implementera i ett internet of things system. För att kunna programmera en arduino board så använder vi språket C++. Här visas koden för att köra exempelkoden för att få en lampa att blinka.

<img width="650" height="366" alt="image" src="https://github.com/user-attachments/assets/3d9c796d-5625-40ec-b922-0645c3206bb6" />


```
void setup() {
   pinMode(LED_BUILTIN, OUTPUT);
```
Under ``` viod setup () ``` så skriver man kod som krävs för att få ett program att starta en gång, t.ex. som att logga in eller få access till en server. Saker som inte behöver göras fler än en gång.
under funktionen pinMode så finner vi ```LED_BUILTIN``` och ```OUTPUT```. 

LED_BUILTIN är namnet på den inbyggda led pinnen på arduino kortet. Output gör så att den pinnen ska användas som utgång, den ska alltså skicka ut signaler istället för att ta emot signaler.

```
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  
  delay(1000);                      
  digitalWrite(LED_BUILTIN, LOW);   
  delay(1000);                      
}
```
Under ```Void loop ()```skrivs kod som ska repeteras under programmets körning. Det kommer alltså till skillnad från ```void setup()```som bara körs en gång, köras om och om igen tills att körningen stoppas. 

```digitalWrite(LED_BUILTIN, HIGH);```gör så att lapan som är kopplad till arduino lyser, då spänningne höjs till ```HIGH```

Sedan startat ett ```delay```i 1000 millisekunder för att fortsätt hålla lampan tänd.
Till sist så avänds ```digitalWrite(LED_BUILTIN, LOW);``` för att släcka lampan, och sedan en till ```delay```för att hålla lampan släckt
