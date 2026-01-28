#include <iostream>
using namespace std;

class Square {
protected:
    double side;

public:
    // Constructor
    Square(double s) : side(s) {}

    // Destructor
    ~Square() {
        cout << "Square object destroyed." << endl;
    }

    // Member functions
    double getPeri() { return 4 * side; }
    double getArea() { return side * side; }
};

class Cube : public Square {
public:
    // Constructor
    Cube(double s) : Square(s) {}

    // Destructor
    ~Cube() {
        cout << "Cube object destroyed." << endl;
    }

    // Member functions
    double getArea() { return 6 * side * side; }
    double getVolume() { return side * side * side; }
};

