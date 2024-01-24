#define segA 2//connecting segment A to PIN2
#define segB 3// connecting segment B to PIN3
#define segC 4// connecting segment C to PIN4
#define segD 5// connecting segment D to PIN5
#define segE 6// connecting segment E to PIN6
#define segF 7// connecting segment F to PIN7
#define segG 8// connecting segment G to PIN8
#define buzzerPin 10// Buzzer connected to PIN10
 
                int COUNT=0;//count integer for 0-9 increment
 
void setup()
 
{
 
                  for (int i=2;i<9;i++)
 
                  {
 
                                    pinMode(i, OUTPUT);// taking all pins from 2-8 as output
                  }
 
pinMode(buzzerPin , OUTPUT);
}
 
void loop()
 
{
 
switch (COUNT)
 
                {
 
                case 0://when count value is zero show”0” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, HIGH);
 
                digitalWrite(segF, HIGH);
 
                digitalWrite(segG, LOW);
 
                break;
 
                case 1:// when count value is 1 show”1” on disp
                digitalWrite(segA, LOW);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, LOW);
 
                digitalWrite(segE, LOW);
 
                digitalWrite(segF, LOW);
 
                digitalWrite(segG, LOW);
 
                break;
 
                case 2:// when count value is 2 show”2” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, LOW);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, HIGH);
 
                digitalWrite(segF, LOW);
 
                digitalWrite(segG, HIGH);
 
                break;
 
 
                case 3:// when count value is 3 show”3” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, LOW);
 
                digitalWrite(segF, LOW);
 
                digitalWrite(segG, HIGH);
 
                break;
 
                case 4:// when count value is 4 show”4” on disp
                digitalWrite(segA, LOW);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, LOW);
 
                digitalWrite(segE, LOW);
 
                digitalWrite(segF, HIGH);
 
                digitalWrite(segG, HIGH);
 
                break;
 
 
                case 5:// when count value is 5 show”5” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, LOW);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, LOW);
 
                digitalWrite(segF, HIGH);
 
                digitalWrite(segG, HIGH);
 
                break;
 
 
                case 6:// when count value is 6 show”6” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, LOW);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, HIGH);
 
                digitalWrite(segF, HIGH);
 
                digitalWrite(segG, HIGH);
 
                break;
 
                case 7:// when count value is 7 show”7” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, LOW);
 
                digitalWrite(segE, LOW);
 
                digitalWrite(segF, LOW);
 
                digitalWrite(segG, LOW);
 
                break;
 
 
                case 8:// when count value is 8 show”8” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, HIGH);
 
                digitalWrite(segF, HIGH);
 
                digitalWrite(segG, HIGH);
 
                break;
 
 
                case 9:// when count value is 9 show”9” on disp
                digitalWrite(segA, HIGH);
 
                digitalWrite(segB, HIGH);
 
                digitalWrite(segC, HIGH);
 
                digitalWrite(segD, HIGH);
 
                digitalWrite(segE, LOW);
 
                digitalWrite(segF, HIGH);
 
                digitalWrite(segG, HIGH);
 
                break;
 
                break;
 
                }
 
                if (COUNT<10)
 
                {
 
                                COUNT++;
 
                                delay(1000);///increment count integer for every second
 
                }
 
                if (COUNT==10)
 
                {
 
                                COUNT=0;// if count integer value is equal to 10, reset it to zero.
 
                                digitalWrite(buzzerPin, HIGH);
                                delay(150);
                                digitalWrite(buzzerPin, LOW);
 
                                delay(1000);
 
                }
 
}
