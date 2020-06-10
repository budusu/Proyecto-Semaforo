# Proyecto-Semaforo
Administracion del proyecto de semaforos de Topicos de Especialidad USACH


void setup()
{
  pinMode(2, INPUT_PULLUP);
  
  for(int pin = 3; pin < 8; pin++) {
  	pinMode(pin, OUTPUT);
  }
}

void loop()
{
  while(digitalRead(2) == false) {
  	digitalWrite(4, HIGH);
    digitalWrite(5, HIGH);
  }
  
  delay(2000);
  digitalWrite(5, LOW);
  digitalWrite(6, HIGH);
  delay(3000);
  digitalWrite(3, HIGH);
  digitalWrite(4, LOW);
  digitalWrite(6, LOW);
  digitalWrite(7, HIGH);
  delay(5000);
  
  for(int i = 0; i < 5; i++) {
  	digitalWrite(3, HIGH);
    delay(500);
    digitalWrite(3, LOW);
    delay(500);
  }
  
  digitalWrite(7, LOW);
}
