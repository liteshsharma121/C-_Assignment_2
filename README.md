#include <iostream>
#include <string>
using namespace std;

class Television {
private:
    string brand;
    int modelYear;
    double price;

public:
    // Default Constructor
    Television() {
        brand = "Samsung";
        modelYear = 2024;
        price = 50000;
    }

    // Parameterized Constructor
    Television(string b, int y, double p) {
        brand = b;
        modelYear = y;
        price = p;
    }

    // Copy Constructor
    Television(const Television &t) {
        brand = t.brand;
        modelYear = t.modelYear;
        price = t.price;
    }

    // Member Function
    void display() {
        cout << "\nTelevision Details:" << endl;
        cout << "Brand: " << brand << endl;
        cout << "Model Year: " << modelYear << endl;
        cout << "Price: " << price << endl;
    }
};

int main() {
    string brand;
    int modelYear;
    double price;

    // Input for Parameterized Constructor
    cout << "Enter television brand: ";
    getline(cin, brand);

    cout << "Enter model year: ";
    cin >> modelYear;

    cout << "Enter television price: ";
    cin >> price;

    // Default Constructor
    Television t1;
    cout << "\nDefault Constructor:";
    t1.display();

    // Parameterized Constructor
    Television t2(brand, modelYear, price);
    cout << "\nParameterized Constructor:";
    t2.display();

    // Copy Constructor
    Television t3(t2);
    cout << "\nCopy Constructor:";
    t3.display();

    return 0;
}
