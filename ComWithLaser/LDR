const int ldrPin = A0;

void setup() {

Serial.begin(9600);
pinMode(ldrPin, INPUT);

}

void loop() {

int bits[9];

if (analogRead(ldrPin) > 800) {// 0 . yani ilk kontrol biti 1 olursa döngüye giriyor (B)
    for(int i = 0; i<9; i++){
      if(analogRead(ldrPin) > 800){
        bits[i+1]=1;
      }
      else{
        bits[i+1]=0;
      }
      delay(200); // 0 VE 1 Bit geçişi arasındaki saniye farkı (A)
    }

    for(int i = 1; i<9; i++){ //Ekrana yazdırma döngüsü
      Serial.print(bits[i+1]);
      }
      Serial.println("");
    } 
}
