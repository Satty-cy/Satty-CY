#include <iostream>
#include <string>
#include <vector>

using namespace std;

class Attendance {
private:
    vector<string> students;
    vector<bool> present;

public:
    void addStudent(string name) {
        students.push_back(name);
        present.push_back(false);
    }

    void markPresent(string name) {
        for (int i = 0; i < students.size(); i++) {
            if (students[i] == name) {
                present[i] = true;
                cout << name << " has been marked present." << endl;
                return;
            }
        }
        cout << name << " is not a valid student." << endl;
    }

    void markAbsent(string name) {
        for (int i = 0; i < students.size(); i++) {
            if (students[i] == name) {
                present[i] = false;
                cout << name << " has been marked absent." << endl;
                return;
            }
        }
        cout << name << " is not a valid student." << endl;
    }

    void displayAttendance() {
        cout << "Attendance List:" << endl;
        for (int i = 0; i < students.size(); i++) {
            cout << students[i] << ": " << (present[i] ? "Present" : "Absent") << endl;
        }
    }
};

int main() {
    Attendance attendance;
    attendance.addStudent("Alice");
    attendance.addStudent("Bob");
    attendance.addStudent("Charlie");

    attendance.markPresent("Alice");
    attendance.markAbsent("Bob");
    attendance.markPresent("David");

    attendance.displayAttendance();

    return 0;
}
