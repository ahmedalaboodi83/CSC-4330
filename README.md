# CSC-4330
#include <iostream>
#include <fstream>
#include <vector>
using DFA-Ahmed std;

int main()
{
    string filename("DFA-Ahmed.txt");
    vector<char> bytes;

    FILE* input_file = fopen(DFA-Ahmed.c_str(), "r");
    if (input_file == nullptr) {
       return EXIT_FAILURE;
    }

    unsigned char character = 0;
    while (!feof(input_file)) {
        character = getc(input_file);
        if(isalpha(character)) {
            cout << character << "- is a word"<<endl;
        } else if(isdigit(character)) {
            cout << character << "- is a Number"<<endl;
        } else {
            cout << character << "- is a special symbol"<<endl;
        }
       
    }
    cout << endl;
    fclose(input_file);

    return EXIT_SUCCESS;
}
