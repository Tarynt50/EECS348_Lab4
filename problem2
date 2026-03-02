#include <stdio.h>

float celsius_to_fahrenheit (float celsius) {
    float result = (9.0/5.0)*celsius + 32.0;

    return result; 
}

float celsius_to_kelvin (float celsius){
    float result = celsius + 273.15;

    return result;
}

float fahrenheit_to_celsius (float fahrenheit){
    float result =(5.0/9.0)*(fahrenheit - 32.0);

    return result;
} 

float fahrenheit_to_kelvin (float fahrenheit){
    float result = (fahrenheit - 32) * (5./9.0) + 273.15;

    return result;
}

float kelvin_to_celsius (float kelvin){
    float result = kelvin - 273.15;

    return result;
}

float kelvin_to_fahrenheit (float kelvin){ 
    float result = (kelvin - 273.15) * (9.0/5.0) + 32;

    return result;
}

void categorizze_temperture(float celsius) {
    if(celsius < 0){
        printf("Temperature is below freezing:\nPlease stay warm indoors");
    }

    else if(celsius < 10){
        printf("Temperature is cold:\n Please wear a jacket");
    }

    else if(celsius < 25){
        printf("Temperature is comfortable:\nEnjoy a beautiful day!");
    }

    else if(celsius < 35){
        printf("Temperature is hot:\nStay hydrated");
    }

    else{
        printf("Temperature is extreme heat:\n Stay indoors, too hot outside");
    }
}

int main(){

    float temperature;
    int choice;
    int conversion; 

    while (1){
        printf("enter temperature:   \n");
        if(scanf("%f", &temperature)== 1) {
            break;
        }
        printf("Invalid Input:   Please re-enter temperture");
        while(getchar() != '\n');

    }

    while (1){
        printf("\nIs this in: \n1)Fahrenheit \n2)Celsius \n3)Kelvin \nEnter 1, 2, 3:   \n");
        if (scanf("%d", &choice) ==1 && choice >=1 && choice <= 3) {
            break;
        }
        printf("Invalid Input: Please re-enter 1, 2, or 3");
        while(getchar() != '\n');

    }

    while (choice == 3 && temperature < 0 ){
        printf("Kelvin Cannot be negative.   Re-enter temperature:   ");
        scanf("%f", &temperature);
    }

    while (1){
        printf("\nChoose Temperature Conversion:  \n1)Fahrenheit \n2)Celsius \n3)Kelvin \nEnter 1, 2, 3:   \n");
        if(scanf("%d", &conversion)==1 && conversion >= 1 && conversion <= 3){
            break;
        }
        printf("Invalid Input: Please enter 1, 2, or 3 ");
        while(getchar() != '\n');

    }

    while (conversion == choice){
        printf("You cannot have the same temperature scale and conversion temperature");
        printf("Choose Temoperature Conversion:  \n1)Fahrenheit \n2)Celsius \n3)Kelvin \nEnter 1, 2, 3:   \n");
        if (scanf("%d", &conversion) != 1 || conversion < 1 || conversion > 3) { 
            printf("Invalid input. Try again.\n"); 
            while (getchar() != '\n'); 
            continue;
        }
    }

    

    float result;
    float celsius_value;

    if (choice ==1 && conversion ==2){
        result = fahrenheit_to_celsius(temperature);
        celsius_value = result;
    }

    else if (choice ==1 && conversion == 3){
        result = fahrenheit_to_kelvin(temperature);
        celsius_value = fahrenheit_to_celsius(temperature);
    }

    else if (choice == 2 && conversion == 1){
        result = celsius_to_fahrenheit(temperature);
        celsius_value = temperature;
    }

    else if (choice == 2 && conversion == 3){
        result = celsius_to_kelvin(temperature);
        celsius_value = temperature;
    }

    else if (choice == 3 && conversion == 1){ 
        result = kelvin_to_fahrenheit(temperature);
        celsius_value = kelvin_to_celsius(temperature);
    }

    else if (choice == 3 && conversion == 2){
        result = kelvin_to_celsius(temperature);
        celsius_value = result;
    }

    printf("\nConverted temperture: %.2f \n", result);

    categorizze_temperture(celsius_value);

    return 0;
   
}