// Defina os pinos do sensor ultrassônico
const int trigPin = 3;
const int echoPin = 2;

// Defina o pino do LED
const int ledPin = 4;

void setup() {
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  pinMode(ledPin, OUTPUT);
  digitalWrite(trigPin, LOW);
}

void loop() {
  
  // Gerando um pulso curto para iniciar a medição
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

  // Medindo o tempo que leva para o eco retornar
  unsigned long tempo = pulseIn(echoPin, HIGH);

  // Convertendo o tempo de retorno em centímetros
  double distancia_cm = tempo / 58.2;
  
  // Controlando o brilho do LED com base na distância
  if (distancia_cm <= 20) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }

  delay(100); // Aguarde um curto período de tempo 
}
