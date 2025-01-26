#include <Adafruit_GFX.h>
#include <Adafruit_SSD1306.h>
#define SCREEN_WIDTH 128
#define SCREEN_HEIGHT 64
#define OLED_RESET    -1
#define OLED_ADDR     0x3C  // I2C address
Adafruit_SSD1306 display(SCREEN_WIDTH, SCREEN_HEIGHT, &Wire, OLED_RESET);

int Text[] = {3, 2, 1};


bool Start = false;
bool A = false;
bool B = false;
bool C = false;
bool D = false;
bool E = false;
bool F = false;
bool G = false;
bool H = false;
bool I = false;
bool J = false;
bool K = false;
bool L = false;
bool M = false;
bool N = false;
bool O = false;
bool P = false;

void setup() {
  display.begin(SSD1306_SWITCHCAPVCC, OLED_ADDR);
  display.clearDisplay();
}
void loop() {
  display.display();
  if (!Start) {
    Lights();
    display.display();
    delay(500);
  }
  Start = true;
  display.clearDisplay();
  if (!A) {
    Lights();
    LightsOn();
    Room();
    PunchingBag();
    KickPad();
    display.display();
    delay(500);
  }
  A = true;
  display.clearDisplay();

  if (!B) {
    FirstText3();
    display.display();
    delay(100);
    display.clearDisplay();

    FirstText2();
    display.display();
    delay(100);
    display.clearDisplay();

    FirstText1();
    display.display();
    delay(100);
    display.clearDisplay();

    FirstText4();
    display.display();
    delay(100);
    display.clearDisplay();

  }
  B = true;
  display.clearDisplay();
  if (!C) {
    FirstSequence();
    Flip();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
  }
  C = true;
  display.clearDisplay();
  if (!D) {
    Smallweights();
    Smallweights1();
    Smallweights();
    Smallweights1();
    Smallweights();
    Smallweights2();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
  }
  D = true;
  display.clearDisplay();

  if (!E) {
    JumpRope1();
    JumpRope1();
    JumpRope1();
    JumpRope1();
    JumpRope1();
    JumpRope1();
    JumpRope1();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
  }
  E = true;
  display.clearDisplay();


  if (!F) {
    PunchingMan1();
    PunchingMan2();
    PunchingEffect2();
    PunchingEffect3();
    PunchingEffect4();
    PunchingMan2();
    display.display();
  }
  F = true;
  display.clearDisplay();

  if (!G) {
    PunchingMan6();
    display.display();
    delay(100);
  }
  G = true;
  display.clearDisplay();
  if (!H) {
    PunchingEffect5();
    display.display();
  }
  H = true;
  display.clearDisplay();
  if (!I) {
    PunchingEffect6();
    display.display();
  }
  I = true;
  display.clearDisplay();

  if (!J) {
    drawblade1();
    display.display();
  }
  J = true;
  display.clearDisplay();

  if (!K) {
    Strike1();
    PunchingBag();
    Lights();
    Room();
    display.display();
  }
  K = true;
  display.clearDisplay();


  if (!L) {
    Strike2pause();
    Stick1();
    PunchingBag();
    Lights();
    Room();
    Stick3();
    display.display();
    delay(100);
  }
  L = true;
  display.clearDisplay();


  if (!M) {
    Strike2();
    Strike3();
    Strike2();
    Strike3();
    Strike2();
    Strike3();
    Strike2();
    Strike3();
    PunchingBag();
    Lights();
    Room();
    display.display();
  }
  M = true;
  display.clearDisplay();


  if (!N) {
    End1();
    PunchingBag();
    Lights();
    Room();
    Stick1();
    display.display();
  }
  N = true;
  display.clearDisplay();


  if (!O) {
    End2();
    End3();
    PunchingBag();
    Stick1();
    Lights();
    Room();
    display.display();
    delay(400);
  }
  O = true;
  display.clearDisplay();

  if (!P) {
    LightsOn();
    PunchingBag();
    Stick1();
    End3();
    Lights();
    Room();
    display.display();
    delay(300);
  }
  P = true;
  display.clearDisplay();
}













//Code Starts Here😍💓☺️💓☺️💓☺️💓😍💓😍😂😍😂😉😂😉💜😂💜😂😉💓😉😍😀😀😍😀😍😀




void FirstText1() {
  display.setTextSize(4);
  display.setCursor(60, 20);
  display.setTextColor(SSD1306_WHITE);
  display.println("1");

}
void FirstText2() {
  display.setTextSize(4);
  display.setCursor(60, 20);
  display.setTextColor(SSD1306_WHITE);
  display.println("2");

}

void FirstText3() {
  display.setTextSize(4);
  display.setCursor(60, 20);
  display.setTextColor(SSD1306_WHITE);
  display.println("3");

}
void FirstText4() {
  display.setTextSize(4);
  display.setCursor(5, 20);
  display.setTextColor(SSD1306_WHITE);
  display.println("Start");

}


void Lights() {
  display.drawLine(20, 1, 20, 5, WHITE);
  display.fillCircle(20, 5, 2, WHITE);//Light 1
  display.drawLine(65, 1, 65, 5, WHITE);
  display.fillCircle(65, 5, 2, WHITE);//Light 2
  display.drawLine(110, 1, 110, 5, WHITE);
  display.fillCircle(110, 5, 2, WHITE); //Light 3

}

void Room() {
  //Left Side
  display.drawLine(1, 60, 10, 45, WHITE);
  display.drawLine(10, 7, 10, 45, WHITE);
  display.drawLine(0, 1, 10, 7, WHITE);
  //Right Side
  display.drawLine(112, 45, 127, 60, WHITE);
  display.drawLine(112, 7, 112, 45, WHITE);
  display.drawLine(127, 1, 112, 7, WHITE);
  //Corner
  display.drawLine(10, 45, 112, 45, WHITE);
  display.drawLine(10, 7, 112, 7, WHITE);
  // Switch Board
  display.fillRect(116, 35, 3, 2, WHITE);



}


void PunchingBag() {
  display.fillRect(15, 20, 5, 23, WHITE);
  display.drawLine(17, 1, 17, 20, WHITE);

}

void KickPad() {
  display.fillCircle(23, 20, 2, WHITE); //Light 3
  display.drawLine(20, 20, 23, 20, WHITE);

}



void LightsOn() { //Hero First Position
  int Side = 0;
  int Up = 5;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
  //Arms
  display.drawLine(122 - Side, 48 - Up, 125 - Side, 52 - Up, WHITE);
  display.drawLine(125 - Side, 52 - Up, 122 - Side, 56 - Up, WHITE);
  //Switch On
  display.drawLine(122 - Side, 48 - Up, 116 - Side, 40 - Up, WHITE);

  //LLegs
  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);

}




void Squatweigtlift1() { //Hero First Position
  int Side = 70;
  int Up = 10;
  for (int I = 0; I <= 4; I++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up + I, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up + I, 121 - Side, 54 - Up + I, WHITE);

    //Lhand
    display.drawLine(121 - Side, 48 - Up + I, 127 - Side, 53 - Up + I, WHITE);
    display.drawLine(127 - Side, 48 - Up + I, 127 - Side, 53 - Up + I, WHITE);
    //Rhand
    display.drawLine(115 - Side, 53 - Up + I, 121 - Side, 48 - Up + I, WHITE);
    display.drawLine(115 - Side, 53 - Up + I, 115 - Side, 48 - Up + I, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up + I, 119 - Side, 58 - Up + I, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up + I, 123 - Side, 58 - Up + I, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    //Weight
    display.fillRect(36, 38 + I, 31, 1, WHITE);
    display.fillRect(32, 35 + I, 10, 8, WHITE);
    display.fillRect(61, 35 + I, 10, 8, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Squatweigtlift2() { //Hero First Position
  int Side = 70;
  int Up = 10;
  for (int I = 0; I <= 4; I++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up - I + 4, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up - I + 4, 121 - Side, 54 - Up - I + 4, WHITE);

    //Lhand
    display.drawLine(121 - Side, 48 - Up - I + 4, 127 - Side, 53 - Up - I + 4, WHITE);
    display.drawLine(127 - Side, 48 - Up - I + 4, 127 - Side, 53 - Up - I + 4, WHITE);
    //Rhand
    display.drawLine(115 - Side, 53 - Up - I + 4, 121 - Side, 48 - Up - I + 4, WHITE);
    display.drawLine(115 - Side, 53 - Up - I + 4, 115 - Side, 48 - Up - I + 4, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up - I + 4, 119 - Side, 58 - Up - I + 4, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up - I + 4, 123 - Side, 58 - Up - I + 4, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    //Weight
    display.fillRect(36, 42 - I, 31, 1, WHITE);
    display.fillRect(32, 39 - I, 10, 8, WHITE);
    display.fillRect(61, 39 - I, 10, 8, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Squatweigtlift3() { //Hero First Position
  int Side = 70;
  int Up = 10;
  for (int I = 0; I <= 12; I++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

    //Lhand
    display.drawLine(121 - Side, 48 - Up, 127 - Side, 53 - Up - I, WHITE);
    display.drawLine(127 - Side, 48 - Up - I, 127 - Side, 53 - Up - I, WHITE);
    //Rhand
    display.drawLine(115 - Side, 53 - Up - I, 121 - Side, 48 - Up, WHITE);
    display.drawLine(115 - Side, 53 - Up - I, 115 - Side, 48 - Up - I, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    //Weight
    display.fillRect(36, 38 - I, 31, 1, WHITE);
    display.fillRect(32, 35 - I, 10, 8, WHITE);
    display.fillRect(61, 35 - I, 10, 8, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}



void Squatweigtlift4() { //Hero First Position
  int Side = 70;
  int Up = 10;
  for (int I = 0; I <= 12; I++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

    //Lhand
    display.drawLine(121 - Side, 48 - Up, 127 - Side, 53 - Up - 12 + I, WHITE);
    display.drawLine(127 - Side, 48 - Up - 12 + I, 127 - Side, 53 - Up - 12 + I, WHITE);
    //Rhand
    display.drawLine(115 - Side, 53 - Up - 12 + I, 121 - Side, 48 - Up, WHITE);
    display.drawLine(115 - Side, 53 - Up - 12 + I, 115 - Side, 48 - Up - 12 + I, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    //Weight
    display.fillRect(36, 38 - 12 + I, 31, 1, WHITE);
    display.fillRect(32, 35 - 12 + I, 10, 8, WHITE);
    display.fillRect(61, 35 - 12 + I, 10, 8, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Squatweigtlift5() { //Hero First Position
  int Side = 70;
  int Up = 10;
  int I = 12;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

  //Lhand
  display.drawLine(121 - Side, 48 - Up, 127 - Side, 53 - Up - I, WHITE);
  display.drawLine(127 - Side, 48 - Up - I, 127 - Side, 53 - Up - I, WHITE);
  //Rhand

  //LLegs
  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
  //Weight
  PunchingBag();
  KickPad();
  Lights();
  Room();

}



void Backflip1() { //Hero First Position
  int Side = 70;
  int Up = 13;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

  //Lhand
  display.drawLine(121 - Side, 48 - Up, 127 - Side, 53 - Up, WHITE);
  display.drawLine(127 - Side, 53 - Up, 121 - Side, 53 - Up, WHITE);
  //Rhand
  display.drawLine(115 - Side, 53 - Up, 121 - Side, 48 - Up, WHITE);
  display.drawLine(115 - Side, 53 - Up, 121 - Side, 53 - Up, WHITE);

  //LLegs
  display.drawLine(121 - Side, 54 - Up, 117 - Side, 50 - Up, WHITE);
  display.drawLine(117 - Side, 50 - Up, 117 - Side, 55 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 125 - Side, 50 - Up, WHITE);
  display.drawLine(125 - Side, 50 - Up, 125 - Side, 55 - Up, WHITE);
  //Weight

  PunchingBag();
  KickPad();
  Lights();
  Room();
}

void Backflip2() { //Hero First Position
  int Side = 70;
  int Up = 13;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 44 - Up, 121 - Side, 44 - Up, WHITE);

  //Lhand
  display.drawLine(121 - Side, 44 - Up, 127 - Side, 40 - Up, WHITE);
  display.drawLine(127 - Side, 40 - Up, 121 - Side, 40 - Up, WHITE);
  //Rhand
  display.drawLine(115 - Side, 40 - Up, 121 - Side, 44 - Up, WHITE);
  display.drawLine(115 - Side, 40 - Up, 121 - Side, 40 - Up, WHITE);

  //LLegs
  display.drawLine(117 - Side, 40 - Up, 117 - Side, 40 - Up, WHITE);
  display.drawLine(117 - Side, 40 - Up, 121 - Side, 44 - Up, WHITE);
  //Rleg
  display.drawLine(125 - Side, 40 - Up, 125 - Side, 40 - Up, WHITE);
  display.drawLine(125 - Side, 40 - Up, 121 - Side, 44 - Up, WHITE);
  //Weight

  PunchingBag();
  KickPad();
  Lights();
  Room();
}


void Backflip3() { //Hero First Position
  int Side = 70;
  int Up = 13;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 41 - Up, 121 - Side, 32 - Up, WHITE);

  //Lhand
  display.drawLine(121 - Side, 41 - Up, 127 - Side, 36 - Up, WHITE);
  display.drawLine(127 - Side, 36 - Up, 121 - Side, 36 - Up, WHITE);
  //Rhand
  display.drawLine(115 - Side, 36 - Up, 121 - Side, 41 - Up, WHITE);
  display.drawLine(115 - Side, 36 - Up, 121 - Side, 36 - Up, WHITE);

  //LLegs
  display.drawLine(121 - Side, 32 - Up, 117 - Side, 36 - Up, WHITE);
  display.drawLine(117 - Side, 36 - Up, 117 - Side, 30 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 32 - Up, 125 - Side, 36 - Up, WHITE);
  display.drawLine(125 - Side, 36 - Up, 125 - Side, 30 - Up, WHITE);
  //Weight

  PunchingBag();
  KickPad();
  Lights();
  Room();
}

void Backflip4() { //Hero First Position
  int Side = 70;
  int Up = 10;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

  //Lhand
  display.drawLine(121 - Side, 48 - Up, 127 - Side, 53 - Up, WHITE);
  display.drawLine(127 - Side, 48 - Up, 127 - Side, 53 - Up, WHITE);
  //Rhand
  display.drawLine(115 - Side, 53 - Up, 121 - Side, 48 - Up, WHITE);
  display.drawLine(115 - Side, 53 - Up, 115 - Side, 48 - Up, WHITE);

  //LLegs
  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
  PunchingBag();
  KickPad();
  Lights();
  Room();

}

void Flip() {
  Weight();
  PunchingBag();
  KickPad();
  Lights();
  Room();
  display.display();
  display.clearDisplay();

  Weight1();
  PunchingBag();
  KickPad();
  Lights();
  Room();
  display.display();
  display.clearDisplay();

  Weight2();
  PunchingBag();
  KickPad();
  Lights();
  Room();
  display.display();
  display.clearDisplay();

  Weight3();
  PunchingBag();
  KickPad();
  Lights();
  Room();
  display.display();
  display.clearDisplay();

  Weight4();
  PunchingBag();
  KickPad();
  Lights();
  Room();
  display.display();
  display.clearDisplay();

}

void FirstSequence() {
  Squatweigtlift1();
  Squatweigtlift2();
  Squatweigtlift3();
  Squatweigtlift4();
  Squatweigtlift1();
  Squatweigtlift2();
  Squatweigtlift3();
}

void Weight() {
  for (int I = 0; I <= 5; I += 5) {
    display.fillRect(36, 26 - I, 31, 1, WHITE);
    display.fillRect(32, 23 - I, 10, 8, WHITE);
    display.fillRect(61, 23 - I, 10, 8, WHITE);
    Backflip1();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}



void Weight1() {
  for (int I = 0; I <= 5; I += 5) {
    display.fillRect(36, 21 - I, 31, 1, WHITE);
    display.fillRect(32, 18 - I, 10, 8, WHITE);
    display.fillRect(61, 18 - I, 10, 8, WHITE);
    Backflip2();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Weight2() {
  for (int I = 0; I <= 5; I += 5) {
    display.fillRect(36, 16 - I, 31, 1, WHITE);
    display.fillRect(32, 13 - I, 10, 8, WHITE);
    display.fillRect(61, 13 - I, 10, 8, WHITE);
    Backflip3();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}
void Weight3() {
  for (int I = 0; I <= 5; I += 5) {
    display.fillRect(36, 11 - I, 31, 1, WHITE);
    display.fillRect(32, 8 - I, 10, 8, WHITE);
    display.fillRect(61, 8 - I, 10, 8, WHITE);
    Backflip4();
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Weight4() {
  for (int I = 0; I <= 20; I += 4) {
    display.fillRect(36, 6 + I, 31, 1, WHITE);
    display.fillRect(32, 3 + I, 10, 8, WHITE);
    display.fillRect(61, 3 + I, 10, 8, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    Squatweigtlift5();
    display.display();
    display.clearDisplay();

  }
}





//Phase 1💋💋💋💋💋💋🫰🫰🫰🫰🫰🫰🌼💓🌼💓🌼💓🌸💓🌼💞🌼💪🌼💪🌼💪🌼💪🌼🌼💪🌼💪🌼🌼💋🌼💋🌼💋🌼






void Smallweights() { //Hero First Position
  int Side = 20;
  int Up = 10;
  for (int I = 0; I <= 8; I++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
    //Arms
    display.drawLine(122 - Side, 48 - Up, 125 - Side, 52 - Up, WHITE);
    display.drawLine(125 - Side, 52 - Up, 122 - Side, 56 - Up, WHITE);
    //Weight Arm
    display.drawLine(121 - Side, 48 - Up, 118 - Side, 52 - Up, WHITE);
    display.drawLine(118 - Side, 53 - Up, 115 - Side, 56 - Up - I, WHITE);
    display.fillCircle(115 - Side, 56 - Up - I, 2, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Smallweights1() { //Hero First Position
  int Side = 20;
  int Up = 10;
  for (int I = 0; I <= 8; I++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
    //Arms
    display.drawLine(122 - Side, 48 - Up, 125 - Side, 52 - Up, WHITE);
    display.drawLine(125 - Side, 52 - Up, 122 - Side, 56 - Up, WHITE);
    //Weight Arm
    display.drawLine(121 - Side, 48 - Up, 118 - Side, 52 - Up, WHITE);
    display.drawLine(118 - Side, 53 - Up, 115 - Side, 56 - Up - 8 + I, WHITE);
    display.fillCircle(115 - Side, 56 - Up - 8 + I, 2, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Smallweights2() { //Hero First Position
  int Side = 20;
  int Up = 10;
  for (int I = 0; I <= 90; I += 20) {
    // Head
    display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
    //Arms
    display.drawLine(122 - Side, 48 - Up, 125 - Side, 52 - Up, WHITE);
    display.drawLine(125 - Side, 52 - Up, 122 - Side, 56 - Up, WHITE);
    //Weight Arm
    display.drawLine(110 - Side, 48 - Up, 121 - Side, 48 - Up, WHITE);
    display.fillCircle(110 - Side - I, 48 - Up, 2, WHITE);

    //LLegs
    display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
    display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
    display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}


//Phase 3💋💋💋💋💟🫰💐🫰🌸🫰🫰🌸💜💜💜🌸💜🌸💜💜❣️💜❣️🌸😘🌸😘😘🌸😘😘🌸🌸



void JumpRope1() { //Hero First Position
  int Side = 60;
  int Up = 8;
  for (int I = 0, J = 0; I <= 26, J <= 3; I += 8, J++) {
    // Head
    display.drawCircle(121 - Side, 44 - Up - J, 2, WHITE);
    // Body
    display.drawLine(121 - Side, 48 - Up - J, 121 - Side, 54 - Up - J, WHITE);
    //Arms
    display.drawLine(121 - Side, 48 - Up - J, 127 - Side, 56 - Up - J, WHITE);
    display.drawLine(121 - Side, 48 - Up - J, 115 - Side, 56 - Up - J, WHITE);
    //Jump Rope🫰💌🫰💌🫰💌
    display.drawLine(110 - Side, 37 - Up + I, 132 - Side, 37 - Up + I, WHITE); //Jump Rope Up Down
    display.drawLine(110 - Side, 37 - Up + I, 115 - Side, 56 - Up - J, WHITE); //Side
    display.drawLine(132 - Side, 37 - Up + I, 127 - Side, 56 - Up - J, WHITE);
    //LLegs💛💞💛💞🌹💞🌹💞
    display.drawLine(121 - Side, 54 - Up - J, 117 - Side, 63 - Up - J, WHITE);
    //Rleg
    display.drawLine(121 - Side, 54 - Up - J, 125 - Side, 63 - Up - J, WHITE);
    PunchingBag();
    KickPad();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}





//Phase 4💓💋💕💓💞💋💕💓💋💞💕💓💓💓💓💋💕💞💓💞💋💓💓💞💓💞💋💕💞💓💕💋💞💓💕💓💞💋💕💞💓😘💕😘💓💞💕😘💞💓😭💓😭😘💞😘😘😭💞😭❣️😘💞❣️😭💞😭❣️💞😘❣️😭😭💞


//Effect 1💖❤️❤️💖💖❤️❤️💖💖❤️💖❤️💖❤️💖❤️❤️💖

void PunchingMan1() { //Hero First Position
  int Side = 90;
  int Up = 14;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
  //Arms
  display.drawLine(122 - Side, 48 - Up, 125 - Side, 52 - Up, WHITE);
  display.drawLine(125 - Side, 52 - Up, 122 - Side, 56 - Up, WHITE);
  //LLegs
  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
  Lights();
  Room();
  PunchingEffect1();
}


void PunchingEffect1() {

  display.fillRect(15, 20, 5, 23, WHITE);//Bag
  display.drawLine(17, 1, 17, 20, WHITE);//Bag Rope
  //Kick Pad
  display.fillCircle(23, 20, 2, WHITE); // Kickpad
  display.drawLine(20, 20, 23, 20, WHITE);//KickPad Hold

}


//Effect 2😘😭❤️😭😘😭💓❤️💓😭😘❤️💓😭❤️😘💓😭❤️😘💓😭😭😘❤️💓😭😭😘❤️😭😭😘❤️😘😭❤️💓




void PunchingMan2() { //Hero First Position
  int Side = 90;
  int Up = 14;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
  //L Hand💙❤️💙❤️💙🌹💞💜💞💞
  display.drawLine(121 - Side, 48 - Up, 117 - Side, 49 - Up, WHITE);
  display.drawLine(117 - Side, 49 - Up, 116 - Side, 42 - Up, WHITE);
  //R Hand💛💋💛💛💋💛♥️💛💛♥️
  display.drawLine(121 - Side, 48 - Up, 115 - Side, 50 - Up, WHITE);
  display.drawLine(115 - Side, 50 - Up, 114 - Side, 44 - Up, WHITE);
  //LLegs💕💜❣️😭❣️😭❣️😭❣️😭❣️😭
  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
  Lights();
  Room();
  PunchingEffect1();
}


//Effect 3💞🌹❤️💞❤️♥️💞❤️🌹💞❤️♥️💞❤️♥️💞❤️♥️💞❤️♥️💞💙♥️💞💗💙😘💙💗💙💗💞💙💗💗💞💙💞💗💙😘💗💗💙😘💗😘💗❤️💞❤️💗

void PunchingMan3() { //Hero First Position
  int Side = 90;
  int Up = 14;
  // Head
  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);
  // Body
  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);
  //L Hand💙❤️💙❤️💙🌹💞💜💞💞
  display.drawLine(121 - Side, 48 - Up, 117 - Side, 49 - Up, WHITE);
  display.drawLine(117 - Side, 49 - Up, 116 - Side, 42 - Up, WHITE);
  //R Hand💛💋💛💛💋💛♥️💛💛♥️
  display.drawLine(121 - Side, 48 - Up, 110 - Side, 48 - Up, WHITE);
  //LLegs💕💜❣️😭❣️😭❣️😭❣️😭❣️😭
  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);
  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);
  //Rleg
  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);
  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);
  Lights();
  Room();
}


void PunchingEffect2() {
  for (int I = 0; I <= 4; I += 2) {
    display.fillRect(15 - I, 20, 5, 23, WHITE); //Bag
    display.drawLine(17, 1, 17 - I, 20, WHITE); //Bag Rope
    //Kick Pad
    display.fillCircle(23 - I, 20, 2, WHITE); // Kickpad
    display.drawLine(20 - I, 20, 23 - I, 20, WHITE); //KickPad Hold
    PunchingMan3();
    display.display();
    display.clearDisplay();
  }
}

//Effect 4💓💋💗😻💙😘💗🌹😘💙🌹💗💙♥️😘💙♥️🌹💙💗😘🌹💙😘💗🌹💙😘💗🌹💙😘💗🌹💙😘❣️🌹💙😘💗🌹💙😘💗🌹💙😘💗🌹💙😘💗🌹




void PunchingMan4() { //Hero First Position

  int Side = 90;

  int Up = 14;

  // Head

  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);

  // Body

  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

  //L Hand💙❤️💙❤️💙🌹💞💜💞💞

  display.drawLine(121 - Side, 48 - Up, 110 - Side, 46 - Up, WHITE);

  //R Hand💛💋💛💛💋💛♥️💛💛♥️

  display.drawLine(121 - Side, 48 - Up, 115 - Side, 50 - Up, WHITE);

  display.drawLine(115 - Side, 50 - Up, 114 - Side, 44 - Up, WHITE);

  //LLegs💕💜❣️😭❣️😭❣️😭❣️😭❣️😭

  display.drawLine(121 - Side, 54 - Up, 119 - Side, 58 - Up, WHITE);

  display.drawLine(119 - Side, 58 - Up, 117 - Side, 63 - Up, WHITE);

  //Rleg

  display.drawLine(121 - Side, 54 - Up, 123 - Side, 58 - Up, WHITE);

  display.drawLine(123 - Side, 58 - Up, 125 - Side, 63 - Up, WHITE);

  Lights();

  Room();


}

void PunchingEffect3() {
  for (int I = 0; I <= 4; I += 2) {
    display.fillRect(15 - I, 20, 5, 23, WHITE); //Bag
    display.drawLine(17, 1, 17 - I, 20, WHITE); //Bag Rope
    //Kick Pad
    display.fillCircle(23 - I, 20, 2, WHITE); // Kickpad
    display.drawLine(20 - I, 20, 23 - I, 20, WHITE); //KickPad Hold
    PunchingMan4();
    display.display();
    display.clearDisplay();
  }
}

//Effect 5😻💕🌹❣️💜❣️💙💕💜❣️💙💕❣️💙💜😘💕❣️💜💕❣️😘💜💕❣️😘💜💕😘❣️💜😘❣️💕💜😘❣️💕💜❣️💕😘💜💕😘❣️💜


void PunchingMan5() { //Hero First Position

  int Side = 90;

  int Up = 20;

  // Head

  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);

  // Body

  display.drawLine(121 - Side, 48 - Up, 121 - Side, 54 - Up, WHITE);

  //L Hand💙❤️💙❤️💙🌹💞💜💞💞

  display.drawLine(121 - Side, 48 - Up, 117 - Side, 52 - Up, WHITE);

  display.drawLine(117 - Side, 52 - Up, 121 - Side, 56 - Up, WHITE);

  //R Hand💛💋💛💛💋💛♥️💛💛♥️

  display.drawLine(121 - Side, 48 - Up, 123 - Side, 52 - Up, WHITE);

  display.drawLine(123 - Side, 52 - Up, 126 - Side, 56 - Up, WHITE);

  //LLegs💕💜❣️😭❣️😭❣️😭❣️😭❣️😭

  display.drawLine(121 - Side, 54 - Up, 128 - Side, 56 - Up, WHITE);

  display.drawLine(128 - Side, 56 - Up, 130 - Side, 63 - Up, WHITE);

  //Rleg💋💗💋💗💋💗💋💗💋💗💋💋💋💗💗

  display.drawLine(121 - Side, 54 - Up, 110 - Side, 54 - Up, WHITE);


  Lights();

  Room();



}




void PunchingEffect4() {
  for (int I = 0; I <= 10; I += 5) {
    display.fillRect(15 - I, 20, 5, 23, WHITE); //Bag
    display.drawLine(17, 1, 17 - I, 20, WHITE); //Bag Rope
    //Kick Pad
    display.fillCircle(23 - I, 20, 2, WHITE); // Kickpad
    display.drawLine(20 - I, 20, 23 - I, 20, WHITE); //KickPad Hold
    PunchingMan5();
    display.display();
    display.clearDisplay();
  }
}


void PunchingMan6() { //Hero First Position

  int Side = 90;

  int Up = 14;

  // Head

  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);

  // Body

  display.drawLine(121 - Side, 48 - Up, 113 - Side, 49 - Up, WHITE);

  //L Hand💙❤️💙❤️💙🌹💞💜💞💞

  display.drawLine(121 - Side, 48 - Up, 117 - Side, 50 - Up, WHITE);

  display.drawLine(117 - Side, 50 - Up, 116 - Side, 44 - Up, WHITE);

  //R Hand💛💋💛💛💋💛♥️💛💛♥️

  display.drawLine(121 - Side, 48 - Up, 115 - Side, 50 - Up, WHITE);

  display.drawLine(115 - Side, 50 - Up, 114 - Side, 44 - Up, WHITE);

  //LLegs💕💜❣️😭❣️😭❣️😭❣️😭❣️😭

  display.drawLine(113 - Side, 34 - Up, 113 - Side, 63 - Up, WHITE);

  PunchingEffect1();
  Lights();

  Room();

}



void PunchingMan7() { //Hero First Position

  int Side = 90;

  int Up = 14;

  // Head

  display.drawCircle(121 - Side, 44 - Up, 2, WHITE);

  // Body

  display.drawLine(121 - Side, 48 - Up, 113 - Side, 49 - Up, WHITE);

  //L Hand💙❤️💙❤️💙🌹💞💜💞💞

  display.drawLine(121 - Side, 48 - Up, 117 - Side, 50 - Up, WHITE);

  display.drawLine(117 - Side, 50 - Up, 116 - Side, 44 - Up, WHITE);

  //R Hand💛💋💛💛💋💛♥️💛💛♥️

  display.drawLine(121 - Side, 48 - Up, 115 - Side, 50 - Up, WHITE);

  display.drawLine(115 - Side, 50 - Up, 114 - Side, 44 - Up, WHITE);

  //LLegs💕💜❣️😭❣️😭❣️😭❣️😭❣️😭

  display.drawLine(113 - Side, 34 - Up, 113 - Side, 63 - Up, WHITE);


  Lights();

  Room();

}


void PunchingEffect5() {
  for (int I = 0; I <= 100; I += 10) {

    display.fillRect(15, 20, 5, 23, WHITE);//Bag
    display.drawLine(17, 1, 17, 20, WHITE);//Bag Rope
    //Kick Pad
    display.fillCircle(23, 20, 2 + I, WHITE); // Kickpad
    display.drawLine(20, 20, 23, 20, WHITE);//KickPad Hold
    PunchingMan7();
    display.display();
    display.clearDisplay();

  }
}

void PunchingEffect6() {
  for (int I = 0; I <= 300; I += 60) {


    display.fillRect(15, 20, 5, 23, WHITE);//Bag
    display.drawLine(17, 1, 17, 20, WHITE);//Bag Rope
    //Kick Pad
    display.fillCircle(23, 20 + I, 102, WHITE); // Kickpad
    Drawblade();
    PunchingBag();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }

}





//Final Phase 💖💙💗💗💗💖♥️💗❤️💗♥️❤️💗♥️❤️💗♥️❤️♥️💗❤️💗💗❤️💙❤️🇮🇹♥️💞💗♥️💞💗💗💞💙🇮🇹🇮🇹💙🇮🇹💋♥️🇮🇹💙❣️💋

void Drawblade() {
  // Mirrored Hero Character Drawing
  int MirrorSide = 20;
  int Up = 5;

  // Head (mirrored)
  display.drawCircle(3 + MirrorSide, 44 - Up, 2, WHITE); // (127 - 124 = 3)

  // Body
  display.drawLine(3 + MirrorSide, 46 - Up, 3 + MirrorSide, 54 - Up, WHITE); // Neck to waist

  // Arms
  display.drawLine(3 + MirrorSide, 48 - Up, 9 + MirrorSide, 54 - Up, WHITE); // Right arm (was left)


  display.drawLine(10 + MirrorSide, 52 - Up, 8 + MirrorSide, 56 - Up, WHITE);

  display.drawLine(12 + MirrorSide, 53 - Up, 8 + MirrorSide, 51 - Up, WHITE); // Crossguard

  display.drawLine(12 + MirrorSide, 52 - Up, 10 + MirrorSide, 52 - Up, WHITE); // Sword blade

  // Legs
  display.drawLine(3 + MirrorSide, 54 - Up, 7 + MirrorSide, 63 - Up, WHITE); // Right leg (was left)
  display.drawLine(3 + MirrorSide, 54 - Up, -1 + MirrorSide, 63 - Up, WHITE); // Left leg (was right)
}




void Stick1() {
  display.fillRect(60, 43, 3, 20, WHITE);

  PunchingBag();
  Lights();
  Room();
}
void Stick2() {
  display.drawLine(60, 42, 62, 42, WHITE); // Neck to waist
  display.drawLine(60, 41, 62, 41, WHITE); // Neck to waist
  display.drawLine(60, 40, 62, 40, WHITE); // Neck to waist
  display.drawLine(60, 39, 62, 39, WHITE); // Neck to waist
  display.drawLine(60, 38, 62, 38, WHITE); // Neck to waist
  display.drawLine(60, 37, 62, 37, WHITE); // Neck to waist
  display.drawLine(60, 36, 62, 36, WHITE); // Neck to waist
  display.drawLine(60, 35, 62, 35, WHITE); // Neck to waist

}


void Stick3() {
  int Up = 3;
  display.drawLine(60, 42 - Up, 62, 42 - Up, WHITE); // Neck to waist
  display.drawLine(60, 41 - Up, 62, 41 - Up, WHITE); // Neck to waist
  display.drawLine(60, 40 - Up, 62, 40 - Up, WHITE); // Neck to waist
  display.drawLine(60, 39 - Up, 62, 39 - Up, WHITE); // Neck to waist
  display.drawLine(60, 38 - Up, 62, 38 - Up, WHITE); // Neck to waist
  display.drawLine(60, 37 - Up, 62, 37 - Up, WHITE); // Neck to waist
  display.drawLine(60, 36 - Up, 62, 36 - Up, WHITE); // Neck to waist
  display.drawLine(60, 35 - Up, 62, 35 - Up, WHITE); // Neck to waist

}






void drawblade1() {
  // Mirrored Hero Character Drawing
  int MirrorSide = 20;
  int Up = 5;
  for (int I = 0; I <= 12; I += 3) {

    // Head (mirrored)
    display.drawCircle(3 + MirrorSide, 44 - Up, 2, WHITE); // (127 - 124 = 3)

    // Body
    display.drawLine(3 + MirrorSide, 46 - Up, 3 + MirrorSide, 54 - Up, WHITE); // Neck to waist

    // Arms
    display.drawLine(3 + MirrorSide, 48 - Up, 9 + MirrorSide, 54 - Up, WHITE); // Right arm (was left)


    display.drawLine(10 + MirrorSide, 52 - Up, 8 + MirrorSide, 56 - Up, WHITE);

    display.drawLine(12 + MirrorSide, 53 - Up, 8 + MirrorSide, 51 - Up, WHITE); // Crossguard

    display.drawLine(12 + MirrorSide, 52 - I - Up, 10 + MirrorSide, 52 - Up, WHITE); // Sword blade

    // Legs
    display.drawLine(3 + MirrorSide, 54 - Up, 7 + MirrorSide, 63 - Up, WHITE); // Right leg (was left)
    display.drawLine(3 + MirrorSide, 54 - Up, -1 + MirrorSide, 63 - Up, WHITE); // Left leg (was right)
    Stick1();
    Stick2();
    PunchingBag();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}



void Strike1() {
  // Mirrored Hero Character Drawing
  int MirrorSide = 20;
  int Up = 5;

  for (int I = 0, J = 0; I <= 40, J <= 52; I += 10, J += 26) {
    MirrorSide += J;
    // Head (mirrored)
    display.drawCircle(3 + MirrorSide, 44 - Up, 2, WHITE); // (127 - 124 = 3)

    // Body
    display.drawLine(3 + MirrorSide, 46 - Up, 3 + MirrorSide, 54 - Up, WHITE); // Neck to waist

    // Arms
    display.drawLine(3 + MirrorSide, 48 - Up, 7 + MirrorSide, 49 - Up, WHITE); // Right arm (was left)

    // Sword
    display.drawLine(-12 + I + MirrorSide, 49 - Up, 7 + MirrorSide, 49 - Up, WHITE); // Sword blade

    // Legs
    display.drawLine(3 + MirrorSide, 54 - Up, 10 + MirrorSide, 56 - Up, WHITE); // Right leg
    display.drawLine(10 + MirrorSide, 56 - Up, 10 + MirrorSide, 63 - Up, WHITE); // Right leg
    display.drawLine(3 + MirrorSide, 54 - Up, -4 + MirrorSide, 63 - Up, WHITE); // Left leg
    Stick1();
    Stick2();
    PunchingBag();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}


void Strike2() {
  // Mirrored Hero Character Drawing
  int MirrorSide = 100;
  int Up = 5;
  for (int I = 0, J = 0; I <= 40, J <= 52; I += 10, J += 26) {
    MirrorSide -= J;
    // Head (mirrored)
    display.drawCircle(3 + MirrorSide, 44 - Up, 2, WHITE); // (127 - 124 = 3)

    // Body
    display.drawLine(3 + MirrorSide, 46 - Up, 3 + MirrorSide, 54 - Up, WHITE); // Neck to waist

    // Arms
    display.drawLine(3 + MirrorSide, 48 - Up, 0 + MirrorSide, 49 - Up, WHITE); // Right arm (was left)

    // Sword
    display.drawLine(19 - I + MirrorSide, 45 - Up, 0 + MirrorSide, 49 - Up, WHITE); // Sword blade

    // Legs Done
    display.drawLine(3 + MirrorSide, 54 - Up, -4 + MirrorSide, 56 - Up, WHITE); // Right leg
    display.drawLine(-4 + MirrorSide, 56 - Up, -4 + MirrorSide, 63 - Up, WHITE); // Right leg
    display.drawLine(3 + MirrorSide, 54 - Up, 10 + MirrorSide, 63 - Up, WHITE); // Left leg
    PunchingBag();
    Lights();
    Room();
    Stick1();
    Stick3();
    display.display();
    display.clearDisplay();

  }
}


void Strike2pause() {

  // Mirrored Hero Character Drawing

  int MirrorSide = 100;

  int Up = 5;



  // Head (mirrored)

  display.drawCircle(3 + MirrorSide, 44 - Up, 2, WHITE); // (127 - 124 = 3)



  // Body

  display.drawLine(3 + MirrorSide, 46 - Up, 3 + MirrorSide, 54 - Up, WHITE); // Neck to waist



  // Arms

  display.drawLine(3 + MirrorSide, 48 - Up, 0 + MirrorSide, 49 - Up, WHITE); // Right arm (was left)



  // Sword

  display.drawLine(19 + MirrorSide, 45 - Up, 0 + MirrorSide, 49 - Up, WHITE); // Sword blade



  // Legs Done

  display.drawLine(3 + MirrorSide, 54 - Up, -4 + MirrorSide, 56 - Up, WHITE); // Right leg

  display.drawLine(-4 + MirrorSide, 56 - Up, -4 + MirrorSide, 63 - Up, WHITE); // Right leg

  display.drawLine(3 + MirrorSide, 54 - Up, 10 + MirrorSide, 63 - Up, WHITE); // Left

}

void Strike3() {
  // Mirrored Hero Character Drawing
  int MirrorSide = 20;
  int Up = 5;

  for (int I = 0, J = 0; I <= 40, J <= 52; I += 20, J += 26) {
    MirrorSide += J;
    // Head (mirrored)
    display.drawCircle(3 + MirrorSide, 44 - Up, 2, WHITE); // (127 - 124 = 3)

    // Body
    display.drawLine(3 + MirrorSide, 46 - Up, 3 + MirrorSide, 54 - Up, WHITE); // Neck to waist

    // Arms
    display.drawLine(3 + MirrorSide, 48 - Up, 7 + MirrorSide, 49 - Up, WHITE); // Right arm (was left)

    // Sword
    display.drawLine(-12 + I + MirrorSide, 45 - Up, 7 + MirrorSide, 49 - Up, WHITE); // Sword blade

    // Legs
    display.drawLine(3 + MirrorSide, 54 - Up, 10 + MirrorSide, 56 - Up, WHITE); // Right leg
    display.drawLine(10 + MirrorSide, 56 - Up, 10 + MirrorSide, 63 - Up, WHITE); // Right leg
    display.drawLine(3 + MirrorSide, 54 - Up, -4 + MirrorSide, 63 - Up, WHITE); // Left leg
    Stick1();
    Stick3();
    PunchingBag();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}

void Slices() {
  int Up = 3;
  display.drawLine(60 - 3, 42 - Up, 62 - 3, 42 - 2 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 4, 41 + 2 - Up, 62 + 4, 41 - Up, WHITE); // Neck to waist
  display.drawLine(60 - 2, 40 - Up + 4, 62 - 2, 40 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 2, 39 - Up, 62 + 2, 39 + 3 - Up, WHITE); // Neck to waist
  display.drawLine(60 - 3, 38 - Up, 62 - 3, 38 + 4 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 4, 37 - Up, 62 + 4, 37 - Up - 4, WHITE); // Neck to waist
  display.drawLine(60 - 2, 36 - 3 - Up, 62 - 2, 36 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 3, 35 + 3 - Up, 62 + 3, 35 - Up, WHITE); // Neck to waist

}

void End1() {
  int Up = 3;
  int Up2 = 5;
  int Side = 21;

  for (int I = 0; I <= 12; I ++) {
    Up -= I;
    // Hero😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻
    // Head
    display.drawCircle(124 - Side, 44 - Up2, 2, WHITE);
    // Body
    display.drawLine(124 - Side, 48 - Up2, 124 - Side, 54 - Up2, WHITE);
    // Arms
    display.drawLine(124 - Side, 48 - Up2, 118 - Side, 54 - Up2, WHITE);
    //Sword
    display.drawLine(117 - Side, 52 - Up2, 119 - Side, 56 - Up2, WHITE);
    display.drawLine(115 - Side, 53 - Up2, 119 - Side, 51 - Up2, WHITE);
    display.drawLine(115 - Side, 40 - Up2 + I, 117 - Side, 52 - Up2, WHITE);
    // Legs
    display.drawLine(124 - Side, 54 - Up2, 120 - Side, 63 - Up2, WHITE);
    display.drawLine(124 - Side, 54 - Up2, 128 - Side, 63 - Up2, WHITE);
    //💋💕💋💕💋💕💋💕💋💋💕💋💕
    display.drawLine(60 - 3, 42 - Up, 62 - 3, 42 - 2 - Up, WHITE); // Neck to waist
    display.drawLine(60 + 4, 41 + 2 - Up, 62 + 4, 41 - Up, WHITE); // Neck to waist
    display.drawLine(60 - 2, 40 - Up + 4, 62 - 2, 40 - Up, WHITE); // Neck to waist
    display.drawLine(60 + 2, 39 - Up, 62 + 2, 39 + 3 - Up, WHITE); // Neck to waist
    display.drawLine(60 - 3, 38 - Up, 62 - 3, 38 + 4 - Up, WHITE); // Neck to waist
    display.drawLine(60 + 4, 37 - Up, 62 + 4, 37 - Up - 4, WHITE); // Neck to waist
    display.drawLine(60 - 2, 36 - 3 - Up, 62 - 2, 36 - Up, WHITE); // Neck to waist
    display.drawLine(60 + 3, 35 + 3 - Up, 62 + 3, 35 - Up, WHITE); // Neck to waist
    Stick1();
    PunchingBag();
    Lights();
    Room();
    display.display();
    display.clearDisplay();

  }
}


void End2() {
  int Side = 21;
  int Up2 = 5;

  // Hero😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻😻
  // Head
  display.drawCircle(107 - Side, 48 - Up2, 2, WHITE);
  // Body
  display.drawLine(110 - Side, 48 - Up2, 124 - Side, 50 - Up2, WHITE);
  // Arms
  display.drawLine(110 - Side, 48 - Up2, 117 - Side, 46 - Up2, WHITE);
  display.drawLine(117 - Side, 46 - Up2, 124 - Side, 52 - Up2, WHITE);
  // Legs
  display.drawLine(124 - Side, 50 - Up2, 124 - Side, 63 - Up2, WHITE);


}



void End3() {
  int Up = -23;
  display.drawLine(60 - 3, 42 - Up, 62 - 3, 42 - 2 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 4, 41 + 2 - Up, 62 + 4, 41 - Up, WHITE); // Neck to waist
  display.drawLine(60 - 2, 40 - Up + 4, 62 - 2, 40 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 2, 39 - Up, 62 + 2, 39 + 3 - Up, WHITE); // Neck to waist
  display.drawLine(60 - 3, 38 - Up, 62 - 3, 38 + 4 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 4, 37 - Up, 62 + 4, 37 - Up - 4, WHITE); // Neck to waist
  display.drawLine(60 - 2, 36 - 3 - Up, 62 - 2, 36 - Up, WHITE); // Neck to waist
  display.drawLine(60 + 3, 35 + 3 - Up, 62 + 3, 35 - Up, WHITE); // Neck to waist

}
