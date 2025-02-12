# C-_Activity1
#include <iostream>
#include <vector>

using namespace std;

// TrafficSignal class definition
class TrafficSignal {
private:
    int signalId;
    string state; // Red, Yellow, Green

public:
    // Parameterized constructor
    TrafficSignal(int id, string initState) {
        signalId = id;
        state = initState;
    }

    // Function to change the state of the signal
    void changeState(string newState) {
        state = newState;
    }

    // Function to display the signal details
    void display() {
        cout << "Signal ID: " << signalId << " | State: " << state << endl;
    }
};

int main() {
    // Create an array of TrafficSignal objects
    vector<TrafficSignal> signals;
    
    // Initialize traffic signals with different states
    signals.push_back(TrafficSignal(1, "Red"));
    signals.push_back(TrafficSignal(2, "Green"));
    signals.push_back(TrafficSignal(3, "Yellow"));

    // Display initial states
    cout << "Initial Traffic Signals States:\n";
    for (auto &signal : signals) {
        signal.display();
    }

    // Change the state of signals
    signals[0].changeState("Green");
    signals[1].changeState("Yellow");
    signals[2].changeState("Red");

    // Display updated states
    cout << "\nUpdated Traffic Signals States:\n";
    for (auto &signal : signals) {
        signal.display();
    }

    return 0;
}