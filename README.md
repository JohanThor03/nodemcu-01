# Vecka-3-presentation
## Blink i arduino
```
 // the setup function runs once when you press reset or power the board
void setup() {
 // initialize digital pin LED_BUILTIN as an output.
   pinMode(LED_BUILTIN, OUTPUT);
```
Under ``` viod setup () ``` så skriver kod som krävs för att få ett program att starta en gång, t.ex. som att logga in eller få access till en server. Saker som inte behöver göras fler än en gång.
under funktionen pinMode så finner vi ```LED_BUILTIN``` och ```OUTPUT```. 

LED_BUILTIN är namnet på den inbyggda led pinnen på arduino kortet. Output gör så att den pinnen ska användas som utgång, den ska alltså skicka ut signaler istället för att ta emot signaler.

```
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}
```
Under ```Void loop ()```skrivs kod som ska repeteras under programmets körning. Det kommer alltså till skillnad från ```void setup()```som bara körs en gång, köras om och om igen tills att körningen stoppas. 

```digitalWrite(LED_BUILTIN, HIGH);```gör så att lapan som är kopplad till arduino lyser, då spänningne höjs till ```HIGH```

Sedan startat ett ```delay```i 1000 millisekunder för att fortsätt hålla lampan tänd.
Till sist så avänds ```digitalWrite(LED_BUILTIN, LOW);``` för att släcka lampan, och sedan en till ```delay```för att hålla lampan släckt
