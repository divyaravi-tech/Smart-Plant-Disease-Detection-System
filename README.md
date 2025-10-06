# Smart-Plant-Disease-Detection-System
This project simulates an embedded or IoT-based plant monitoring system that detects whether a plant is healthy or diseased.
#include <stdio.h>
#include <string.h>

int main() {
    char leafColor[20];
    float moisture, temperature;

    printf("---- SMART PLANT DISEASE DETECTION SYSTEM ----\n");

    printf("Enter leaf color (Green/Yellow/Brown): ");
    scanf("%s", leafColor);

    printf("Enter soil moisture level (in percentage): ");
    scanf("%f", &moisture);

    printf("Enter temperature (in °C): ");
    scanf("%f", &temperature);

    printf("\n---- ANALYZING PLANT CONDITION ----\n");

    if ((strcmp(leafColor, "Green") == 0) && (moisture >= 40 && moisture <= 70) && (temperature >= 20 && temperature <= 30)) {
        printf("✅ Plant is Healthy.\n");
    } 
    else if ((strcmp(leafColor, "Yellow") == 0) || (moisture < 40 || moisture > 70) || (temperature < 18 || temperature > 35)) {
        printf("⚠️ Plant is at Risk! Possible Early Symptoms of Disease.\n");
    } 
    else if (strcmp(leafColor, "Brown") == 0 || moisture < 25 || temperature > 40) {
        printf("❌ Plant is Diseased! Immediate action required.\n");
    } 
    else {
        printf("⚠️ Unable to determine condition. Check sensor readings.\n");
    }

    printf("\nSystem Analysis Complete.\n");
    return 0;
}
