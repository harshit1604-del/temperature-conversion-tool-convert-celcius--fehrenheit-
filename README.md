#include <iostream>
using namespace std;
class Temperature {
private:
float value;
public:
// Constructor
Temperature(float v = 0.0) {
value = v;
}
// Convert Celsius to Fahrenheit
float convertToFahrenheit() {
return (value * 9 / 5) + 32;
}
// Convert Fahrenheit to Celsius
float convertToCelsius() {
return (value - 32) * 5 / 9;
}
};
int main() {
int choice;
float temp;
cout << "===== TEMPERATURE CONVERSION TOOL =====\n";
cout << "1. Convert Celsius to Fahrenheit\n";
cout << "2. Convert Fahrenheit to Celsius\n";
cout << "Enter your choice: ";
cin >> choice;
if (choice == 1) {
cout << "Enter temperature in Celsius: ";
cin >> temp;
Temperature t(temp);
cout << "Temperature in Fahrenheit: " << t.convertToFahrenheit()
<< " °F\n";
}
else if (choice == 2) {
cout << "Enter temperature in Fahrenheit: ";
cin >> temp;
Temperature t(temp);
cout << "Temperature in Celsius: " << t.convertToCelsius() <<
" °C\n";
}
else {
cout << "Invalid choice.\n";
}
return 0;
}
