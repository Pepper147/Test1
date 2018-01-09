# Test1

#include <FastLED.h>
#define LED_TYPE WS2812B
#define LED_PIN 7
#define COLOR_ORDER GRB
#define NUM_LEDS 25
#define BRIGHTNESS 65

CRGB leds[NUM_LEDS];

void setup() {
  delay(3000);
  LEDS.addLeds<LED_TYPE, LED_PIN, COLOR_ORDER>(leds, NUM_LEDS);
  FastLED.setBrightness(BRIGHTNESS);
}
void loop() {
  leds[6]  = CRGB:: Red;
  leds[8]  = CRGB:: Red;
  leds[12] = CRGB:: Red;
  leds[16] = CRGB:: Red;
  leds[18] = CRGB:: Red;
  FastLED.show();
  FastLED.delay(10);
}
