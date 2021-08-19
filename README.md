// Projeto - SEMÁFORO_ARDUINO-UNO

// Define os pinos que serao utilizados
int carroVerde = 12;
int carroAmarelo = 11;
int carroVermelho = 10;

void setup() // Define os pinos como saidas
{
  pinMode(carroVerde, OUTPUT);
  pinMode(carroAmarelo, OUTPUT);
  pinMode(carroVermelho, OUTPUT);

  digitalWrite(carroVerde, HIGH); // Coloca na posição inicial. Somente o verde dos carros e o vermelho dos pedestres acesos
  digitalWrite(carroAmarelo, LOW);
  digitalWrite(carroVermelho, LOW);
}

void loop()
{
  digitalWrite(carroVerde, HIGH); // Acende o verde dos carros e o vermelho dos pedestres  
  delay(5000); // Aguarda 5 segundos
  digitalWrite(carroVerde, LOW);
  digitalWrite(carroAmarelo, HIGH); // apaga o verde dos carros e acende o amarelo
  delay(3000); // aguarda mais 3 segundos
  digitalWrite(carroAmarelo, LOW); // apaga o amarelo dos carros e acende o vermelho
  digitalWrite(carroVermelho, HIGH);
  delay(5000);  // aguarda mais 5 segundos
  digitalWrite(carroVermelho, LOW);  
}
