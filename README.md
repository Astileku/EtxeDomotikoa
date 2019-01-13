#include <LiquidCrystal.h>    // importa libreria
int ledOK=3;
int ledERR=2;
int pulsaA=11;
int pulsaB=12;
int pulsaC=13;
int pulsaD=28;
int alt=10;
int led1 = 2; // Habitación 1
int led2 = 3; // Habitación 2
int led3 = 4; // Cocina
int led4 = 5; // Garaje
int led5 = 6; // Salón
int led6 = 7; // baño
int led7 = 8; // Pasillo
int led8 = 9; // Jardín
int estado= 0;
int buzzer = 10; 
int led = 3;
int sensor = A1;
int luz = 0;       
int valor_sensor = 0;       
int valor_limite = 470;  //Este valor hara que el LED cambie de estado a una determinada luminosidad (podeis con distintos valores para ajustar la sensibilidad)
int tiempo = 90;
int clave[]={0,1,2,3};
int sec[]={100,100,100,100};
int estad = 0;
LiquidCrystal lcd(27, 22, 23, 24, 25, 26);

void setup(){
  Serial.begin(9600);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  pinMode(led3, OUTPUT);
  pinMode(led4, OUTPUT);
  pinMode(led5, OUTPUT);
  pinMode(led6, OUTPUT);
  pinMode(led7, OUTPUT);
  pinMode(led8, OUTPUT);
  pinMode(buzzer, OUTPUT);
  pinMode(sensor,INPUT);
  pinMode(22, OUTPUT);    // Pin 11 conectar a IN4
  pinMode(13, OUTPUT);    // Pin 10 conectar a IN3
  pinMode(12, OUTPUT);     // Pin 9 conectar a IN2
  pinMode(11, OUTPUT);     // Pin 8 conectar a IN1
  pinMode(ledOK, OUTPUT);
  pinMode(ledERR,OUTPUT);
  pinMode(pulsaA,INPUT);
  pinMode(pulsaB,INPUT);
  pinMode(pulsaC,INPUT);
  pinMode(pulsaD,INPUT);
  pinMode(alt, OUTPUT);
   lcd.begin(16, 2); 
  }
  
void loop(){
    estado = analogRead(A0);
   Serial.println(estado);
  // activa el buzzer
  if (estado < 500){
   digitalWrite(buzzer, HIGH);
   delay(100);
  // Desactiva el buzzer
  digitalWrite(buzzer, LOW);
  delay(50);
  }
  if( Serial.available()>0)
  {
    estado = Serial.read();
  }
  switch( estado)
  {
    case 'a':
    digitalWrite(led1, HIGH);
    break;
    case 'b':
    digitalWrite(led1, LOW);
    break;
    
    case 'c':
    digitalWrite(led2, HIGH);
    break;
    case 'd':
    digitalWrite(led2, LOW);
    break;

      case 'e':
    digitalWrite(led3, HIGH);
    break;
    case 'f':
    digitalWrite(led3, LOW);
    break;

      case 'g':
    digitalWrite(led4, HIGH);
    break;
    case 'h':
    digitalWrite(led4, LOW);
    break;

      case 'i':
    digitalWrite(led5, HIGH);
    break;
    case 'j':
    digitalWrite(led5, LOW);
    break;

      case 'k':
    digitalWrite(led6, HIGH);
    break;
    case 'l':
    digitalWrite(led6, LOW);
    break;

      case 'm':
    digitalWrite(led7, HIGH);
    break;
    case 'n':
    digitalWrite(led7, LOW);
    break;

      case 'o':
    digitalWrite(led8, HIGH);
    break;
    case 'p':
    digitalWrite(led8, LOW);
    break;

     case 'q':
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
    digitalWrite(led4, HIGH);
    digitalWrite(led5, HIGH);
    digitalWrite(led6, HIGH);
    digitalWrite(led7, HIGH);
    digitalWrite(led8, HIGH);
    break;
    case 'r':
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    digitalWrite(led5, LOW);
    digitalWrite(led6, LOW);
    digitalWrite(led7, LOW);
    digitalWrite(led8, LOW);
    break;

       case 's':
    digitalWrite(buzzer, HIGH);
   delay(100);
    break;
    case 't':
     digitalWrite(buzzer, LOW);
  delay(50);
    break;

    case 'u':          
  
    digitalWrite(led1, HIGH);
    delay(tiempo);
    digitalWrite(led1, LOW);
    
    digitalWrite(led2, HIGH);
    delay(tiempo);
    digitalWrite(led2, LOW);
    
    digitalWrite(led3, HIGH);
    delay(tiempo);
    digitalWrite(led3, LOW);
    
    digitalWrite(led4, HIGH);
    delay(tiempo);
    digitalWrite(led4, LOW);
    
    digitalWrite(led5, HIGH);
    delay(tiempo);
    digitalWrite(led5, LOW);
    
    digitalWrite(led6, HIGH);
    delay(tiempo);
    digitalWrite(led6, LOW);
    
    digitalWrite(led7, HIGH);
    delay(tiempo);
    digitalWrite(led7, LOW);
    
    digitalWrite(led8, HIGH);
    delay(tiempo);
    digitalWrite(led8, LOW);
      
    digitalWrite(led8, HIGH);
    delay(tiempo);
    digitalWrite(led8, LOW);
    
    digitalWrite(led7, HIGH);
    delay(tiempo);
    digitalWrite(led7, LOW);
    
    digitalWrite(led6, HIGH);
    delay(tiempo);
    digitalWrite(led6, LOW);
    
    digitalWrite(led5, HIGH);
    delay(tiempo);
    digitalWrite(led5, LOW);
    
    digitalWrite(led4, HIGH);
    delay(tiempo);
    digitalWrite(led4, LOW);
    
    digitalWrite(led3, HIGH);
    delay(tiempo);
    digitalWrite(led3, LOW);
    
    digitalWrite(led2, HIGH);
    delay(tiempo);
    digitalWrite(led2, LOW);
    
    digitalWrite(led1, HIGH);
    delay(tiempo);
    digitalWrite(led1, LOW);
  
    digitalWrite(led1, HIGH);
    delay(tiempo);
    digitalWrite(led1, LOW);
    
    digitalWrite(led2, HIGH);
    delay(tiempo);
    digitalWrite(led2, LOW);
    
    digitalWrite(led3, HIGH);
    delay(tiempo);
    digitalWrite(led3, LOW);
    
    digitalWrite(led4, HIGH);
    delay(tiempo);
    digitalWrite(led4, LOW);
    
    digitalWrite(led5, HIGH);
    delay(tiempo);
    digitalWrite(led5, LOW);
    
    digitalWrite(led6, HIGH);
    delay(tiempo);
    digitalWrite(led6, LOW);
    
    digitalWrite(led7, HIGH);
    delay(tiempo);
    digitalWrite(led7, LOW);
    
    digitalWrite(led8, HIGH);
    delay(tiempo);
    digitalWrite(led8, LOW);
    
    digitalWrite(led7, HIGH);
    delay(tiempo);
    digitalWrite(led7, LOW);
    
    digitalWrite(led6, HIGH);
    delay(tiempo);
    digitalWrite(led6, LOW);
    
    digitalWrite(led5, HIGH);
    delay(tiempo);
    digitalWrite(led5, LOW);
    
    digitalWrite(led4, HIGH);
    delay(tiempo);
    digitalWrite(led4, LOW);
    
    digitalWrite(led3, HIGH);
    delay(tiempo);
    digitalWrite(led3, LOW);
    
    digitalWrite(led2, HIGH);
    delay(tiempo);
    digitalWrite(led2, LOW);
  
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
    digitalWrite(led4, HIGH);
    delay(100);
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    delay(100);
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
    digitalWrite(led4, HIGH);
    delay(100);
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    delay(100);
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
    digitalWrite(led4, HIGH);
    delay(100);
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    delay(100);
  
    digitalWrite(led5, HIGH);
    digitalWrite(led6, HIGH);
    digitalWrite(led7, HIGH);
    digitalWrite(led8, HIGH);
    delay(100);
    digitalWrite(led5, LOW);
    digitalWrite(led6, LOW);
    digitalWrite(led7, LOW);
    digitalWrite(led8, LOW);
    delay(100);
    digitalWrite(led5, HIGH);
    digitalWrite(led6, HIGH);
    digitalWrite(led7, HIGH);
    digitalWrite(led8, HIGH);
    delay(100);
    digitalWrite(led5, LOW);
    digitalWrite(led6, LOW);
    digitalWrite(led7, LOW);
    digitalWrite(led8, LOW);
    delay(100);
    digitalWrite(led5, HIGH);
    digitalWrite(led6, HIGH);
    digitalWrite(led7, HIGH);
    digitalWrite(led8, HIGH);
    delay(100);
    digitalWrite(led5, LOW);
    digitalWrite(led6, LOW);
    digitalWrite(led7, LOW);
    digitalWrite(led8, LOW);
    delay(100);
 
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
    digitalWrite(led3, HIGH);
    digitalWrite(led4, HIGH);
    delay(500);
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    
    digitalWrite(led5, HIGH);
    digitalWrite(led6, HIGH);
    digitalWrite(led7, HIGH);
    digitalWrite(led8, HIGH);
    delay(500);
    digitalWrite(led5, LOW);
    digitalWrite(led6, LOW);
    digitalWrite(led7, LOW);
    digitalWrite(led8, LOW);
 
    digitalWrite(led1, HIGH);
    digitalWrite(led8, HIGH);
    delay(150);
    digitalWrite(led1, LOW);
    digitalWrite(led8, LOW);
    
    digitalWrite(led2, HIGH);
    digitalWrite(led7, HIGH);
    delay(150);
    digitalWrite(led2, LOW);
    digitalWrite(led7, LOW);
    
    digitalWrite(led3, HIGH);
    digitalWrite(led6, HIGH);
    delay(150);
    digitalWrite(led3, LOW);
    digitalWrite(led6, LOW);
    
    digitalWrite(led4, HIGH);
    digitalWrite(led5, HIGH);
    delay(150);
    digitalWrite(led4, LOW);
    digitalWrite(led5, LOW);
 
    digitalWrite(led4, HIGH);
    digitalWrite(led5, HIGH);
    delay(150);
    digitalWrite(led4, LOW);
    digitalWrite(led5, LOW);
    
    digitalWrite(led3, HIGH);
    digitalWrite(led6, HIGH);
    delay(150);
    digitalWrite(led3, LOW);
    digitalWrite(led6, LOW);
    
    digitalWrite(led2, HIGH);
    digitalWrite(led7, HIGH);
    delay(150);
    digitalWrite(led2, LOW);
    digitalWrite(led7, LOW);
    
    digitalWrite(led1, HIGH);
    digitalWrite(led8, HIGH);
    delay(150);
    digitalWrite(led1, LOW);
    digitalWrite(led8, LOW);
 
    digitalWrite(led1, HIGH);
    digitalWrite(led8, HIGH);
    delay(150);
    digitalWrite(led1, LOW);
    digitalWrite(led8, LOW);
    
    digitalWrite(led2, HIGH);
    digitalWrite(led7, HIGH);
    delay(150);
    digitalWrite(led2, LOW);
    digitalWrite(led7, LOW);
    
    digitalWrite(led3, HIGH);
    digitalWrite(led6, HIGH);
    delay(150);
    digitalWrite(led3, LOW);
    digitalWrite(led6, LOW);
    
    digitalWrite(led4, HIGH);
    digitalWrite(led5, HIGH);
    delay(150);
    digitalWrite(led4, LOW);
    digitalWrite(led5, LOW);
    
    digitalWrite(led3, HIGH);
    digitalWrite(led6, HIGH);
    delay(150);
    digitalWrite(led3, LOW);
    digitalWrite(led6, LOW);
    
    digitalWrite(led2, HIGH);
    digitalWrite(led7, HIGH);
    delay(150);
    digitalWrite(led2, LOW);
    digitalWrite(led7, LOW);
  
  break; 
    case 'v':
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
    digitalWrite(led3, LOW);
    digitalWrite(led4, LOW);
    digitalWrite(led5, LOW);
    digitalWrite(led6, LOW);
    digitalWrite(led7, LOW);
    digitalWrite(led8, LOW);
  break;    
        
    }
    lcd.setCursor(0, 0);      // ubica cursor en columna 0, linea 0
  lcd.print("Pasahitza(4 Zbk)");  // escribe el texto en pantalla
  lcd.setCursor(0,1);
  lcd.print('-');
  
    
    {
    valor_sensor = analogRead(sensor); 
  luz = (5.0 * valor_sensor * 100.0)/1024.0; //Para entender esta formula visitar: http://programarfacil.com/podcast/48-sensor-de-temperatura-en-arduino/
  Serial.print(luz);  
  Serial.println(" Luz");             
  delay(300);                       
  
  if (luz <= valor_limite)   //Si el valor de luz es menor o igual que el valor limite
  {
    digitalWrite (led8, LOW);  //El led se apaga
  }
  if (luz > valor_limite)   //Si es mayor que el valor limite
  {
    digitalWrite (led8, HIGH);  //El led se eniende
  }

  
  } 
  if(digitalRead(pulsaA)){
    lcd.setCursor(0, 1);      // ubica cursor en columna 0, linea 0
    lcd.print('0');
    sec[estad]=0;
    estad++;
    delay(500);
    digitalWrite(alt, HIGH);
    delay(200);
    digitalWrite(alt, LOW);
    delay(100);
    
        
  }
  if(digitalRead(pulsaB)){
   lcd.setCursor(0, 1);      // ubica cursor en columna 0, linea 0
    lcd.print('1');
    sec[estad]=1;
    estad++;
    delay(500);
    digitalWrite(alt, HIGH);
    delay(200);
    digitalWrite(alt, LOW);
    delay(100);
    
  }
   if(digitalRead(pulsaC)){
    lcd.setCursor(0, 1);      // ubica cursor en columna 0, linea 0
    lcd.print('2');
    sec[estad]=2;
    estad++;
    delay(500);
     digitalWrite(alt, HIGH);
    delay(200);
    digitalWrite(alt, LOW);
    delay(100);
  }
   if(digitalRead(pulsaD)){
    lcd.setCursor(0, 1);      // ubica cursor en columna 0, linea 0
    lcd.print('3');
    sec[estad]=3;
    estad++;
    delay(500);
    digitalWrite(alt, HIGH);
    delay(200);
    digitalWrite(alt, LOW);
    delay(100);
    
        
  }
  if(estad==4){
    if((sec[0]==clave[0])&&(sec[1]==clave[1])&&(sec[2]==clave[2])&&(sec[3]==clave[3])){
      lcd.clear();
      lcd.print("PASAHITZA ZUZENA");     
      digitalWrite(ledOK,HIGH);
      delay(200);
      digitalWrite(alt, HIGH);
      delay(300);
      digitalWrite(alt, LOW);
      delay(100);
      digitalWrite(alt, HIGH);
      delay(300);
      digitalWrite(alt, LOW);
      delay(100);
      digitalWrite(alt, HIGH);
      delay(300);
      digitalWrite(alt, LOW);
      delay(100);
      
      

    }
    else {
      lcd.setCursor(0,1);
      lcd.clear();
      lcd.print("PASAHITZA OKERRA");
      digitalWrite(ledERR,HIGH);
      delay(200);
      digitalWrite(alt, HIGH);
      delay(1000);
      digitalWrite(alt, LOW);
      delay(1);
    }
    digitalWrite(ledOK,LOW);
    digitalWrite(ledERR,LOW);
    estad=0;
  }
 
    }

  

    
