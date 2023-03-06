#include <iostream>
#include <fstream>
#include <string>
#include <vector>
using namespace std;
int main()
{
    vector<string> linie;
    ofstream MyFile("filename.txt");
        ifstream MyFile2("filename.txt");
        string data;
    linie.push_back("1. Pierwsza linia");
    linie.push_back("2. Druga linia");
    for (auto linia : linie)
        MyFile << linia << endl;
    while(!MyFile.eof())
    {
        //MyFile2 >> data; //dzieli na spacje
        getline(MyFile2, data);
        cout << data << endl;
    
    }
    MyFile.close();
    MyFile2.close();


}
