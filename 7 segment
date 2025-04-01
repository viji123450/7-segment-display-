
int segmentPins[7] = {2, 3, 4, 5, 6, 7, 8};

// Digit patterns for 0-9 (Common Cathode)
byte digits[10] = {
    0b00111111, 
    0b00000110, 
    0b01011011, 
    0b01001111, 
    0b01100110, 
    0b01101101,
    0b01111101, 
    0b00000111, 
    0b01111111, 
    0b01101111  
};

void setup() {
    for (int i = 0; i < 7; i++) {
        pinMode(segmentPins[i], OUTPUT);
    }
}

void loop() {
    for (int num = 0; num <= 9; num++) { // Loop through digits 0-9
        displayDigit(num);
        delay(1000); // Wait 1 second
    }
}


void displayDigit(int num) {
    for (int i = 0; i < 7; i++) {
        digitalWrite(segmentPins[i], (digits[num] >> i) & 1);
    }
}
