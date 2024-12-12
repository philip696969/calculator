#include <iostream>
using namespace std;

void add() {
    double a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "Sum: " << a + b << endl;
}

void subtract() {
    double a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "Difference: " << a - b << endl;
}

void multiply() {
    double a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    cout << "Product: " << a * b << endl;
}

void divide() {
    double a, b;
    cout << "Enter two numbers: ";
    cin >> a >> b;
    if (b != 0)
        cout << "Quotient: " << a / b << endl;
    else
        cout << "Cannot divide by zero!" << endl;
}

int main() {
    int choice;
    while (true) {
        cout << "\nCalculator Menu:\n";
        cout << "1. Add\n2. Subtract\n3. Multiply\n4. Divide\n5. Exit\n";
        cout << "Enter choice (1-5): ";
        cin >> choice;

        switch (choice) {
            case 1:
                add();
                break;
            case 2:
                subtract();
                break;
            case 3:
                multiply();
                break;
            case 4:
                divide();
                break;
            case 5:
                cout << "Exiting the calculator.\n";
                return 0;
            default:
                cout << "Invalid choice. Please try again.\n";
        }
    }
}
