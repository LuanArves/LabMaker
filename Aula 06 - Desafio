#define pinoTrig 3 // Pino de comunicaçao ligado do Trigger
#define pinoEcho 2 // Pino de comunicaçao ligado do Echo
#define buzzer 4  // Pino de comunicação do buzer

// VARIÁVEIS UTILIZADAS
unsigned long tempo; 
float distancia_cm;

void setup()
{
  pinMode(pinoTrig, OUTPUT);
  pinMode(pinoEcho, INPUT);
  pinMode(buzzer, OUTPUT);   
  digitalWrite(pinoTrig, LOW);
}

void loop()
{
  //Responsavel por efetuar um pequno pulso
  digitalWrite (pinoTrig, HIGH);
  delayMicroseconds(10);
  digitalWrite (pinoTrig, LOW); 
  
  tempo = pulseIn(pinoEcho, HIGH);
  distancia_cm = tempo/58.2; 
 
  //Responsável por acionar o buzzer a depender da distância mensurada
  if (distancia_cm<20){
    tone(buzzer,528);    
    delay(150);
    noTone(buzzer);
    delay(50);
  }
  else if (distancia_cm>=20 && distancia_cm<30){
    tone(buzzer,440);    
    delay(150);
    noTone(buzzer);
    delay(250);
  }
  else if (distancia_cm>=30 && distancia_cm<40){
    tone(buzzer,349);    
    delay(150);
    noTone(buzzer);
    delay(450);
  }
  else if (distancia_cm>=40 && distancia_cm<50){
    tone(buzzer,294);    
    delay(150);
    noTone(buzzer);
    delay(650);
  }
    
  // Intervalo entre atualizacao da distancia
  delay(1000); 
}

