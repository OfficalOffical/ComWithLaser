#define laserPin 5

void setup() {

  pinMode(laserPin, OUTPUT);
  
}

void loop() {
  
  // 00101000
  int bits[]= {LOW, LOW, HIGH, LOW, HIGH, LOW, LOW, LOW};

  digitalWrite(laserPin, HIGH); // Döngü başlasın diye gönderilen kontrol biti (B)
  delay(10);
  digitalWrite(laserPin, LOW);
  
  for(int i = 0; i<8; i++){
    digitalWrite(laserPin, bits[i]);
    delay(200); // 0 VE 1 Bit geçişi arasındaki saniye farkı (A)
  }
  
  digitalWrite(laserPin, LOW);
  delay(1000); // 1 saniye bekletiyor ki karışmasın
    
}
