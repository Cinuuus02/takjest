1. a) zdefiniuj i inicjalizuj tablice z 10 liczbami typu int. 
wypisz na konsoli liczby z tablicy ktore sa podzielne przez 
wypisz kazda liczbe tablicy mnozona przez jej indeks 
  
#include <iostream>
using namespace std;
int main() {
    int liczba[10] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    cout << "Liczby podzielne przez 2: " << endl;
    for (int i = 0; i < 10; i++) {
        if (liczba[i] % 2 == 0) {
            cout << liczba[i] << endl;
        }
    }
    cout << "Liczby pomnożone przez indeks: " << endl;
    for (int i = 0; i < 10; i++) {
        cout << liczba[i] * i << endl;
    }
    return 0;
}
  
b) zdefiniuj i inicjalizuj tablice z 10 elementami typu char. 
  wypisz na konsoli co 3 element zaczynajac od 0 
  wypisz elementy tablicy w odwrotnym porzadku
  
#include <iostream>
using namespace std;
int main() {
    char tablica[10] = {'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j'};
    cout << "Co 3 element tablicy:" << endl;
    for (int i = 0; i < 10; i += 3) {
        cout << tablica[i] << endl;
    }
    cout << "Odwrotna kolejność elementów tablicy: " << endl;
    for (int i = 9; i >= 0; i--) {
        cout << tablica[i] << endl;
    }
    return 0;
}

2. a) zdefiniuj i inicjalizuj wektor z 10 liczbami typu int 
  wypisz  na konsoli parzysty liczby wektora przy pomocy petli
  wypisz na konsoli parzysty liczby wektora przy pomocy operatora for_each.

#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main()
{
    vector<int> wektor {1,2,3,4,5,6,7,8,9,10};
    cout << "Parzyste liczby wektora przy pomocy pętli:" << endl;
    for (int i = 0; i < wektor.size(); i++)
    {
        if (wektor[i]%2==0)
            cout << wektor[i] << endl;
    }
    cout << "Parzyste liczby wektora przy pomocy for_each:" << endl;
    for_each(wektor.begin(), wektor.end(), [](int x){
        if(x%2 == 0)
            cout << x << endl;
    });
    return 0;
}
                             
b) zdefiniuj i inicjalizuj wektor z 7 slowami typu string 
   wypisz kazde slowo w nowym wierszu i przez dwukropek ilosc liter w nim
                             
#include <iostream>
#include <vector>
#include <string>
using namespace std;

int main()
{
    vector<string> wektor {"pies","kot","dom","drzewo","miłość","słońce","deszcz"};
    for (int i = 0; i < wektor.size(); i++)
    {
        cout << wektor[i] << " : " << wektor[i].size() << endl;
    }
    return 0;
}

  1. a) zdefiniuj i inicjalizuj 2 tablice arr1 i arr2 z 7 liczbami int 
                                                              #include <iostream>
using namespace std;

int main()
{
    int arr1[7] = {1,2,3,-4,-5,6,7};
    int arr2[7] = {8,9,10,11,12,13,14};
    int arr3[7];
    for(int i = 0; i < 7; i++)
    {
        arr3[i] = arr1[i] + arr2[i];
    }
    cout << "Suma i-tych elementów z arr1 i arr2: " << endl;
    for(int i = 0; i < 7; i++)
    {
        cout << arr3[i] << endl;
    }
    cout << "Ujemne liczby z arr1: " << endl;
    for(int i = 0; i < 7; i++)
    {
        if(arr1[i] < 0)
        cout << arr1[i] << endl;
    }
    return 0;
}
  
  b) zdefiniuj i inicjalizuj tablice z 5 elementami typu string
  wypisz slowa o parzystym indeksie a po tym wypisz te slowa z tablicy, ilosc liter w ktorych jest wikesza od 3 

  #include <iostream>
using namespace std;

int main()
{
    string tablica[5] = {"komputer","monitor","mysz","klawiatura","głośnik"};
    cout << "Słowa o parzystym indeksie: " << endl;
    for (int i = 0; i < 5; i++) {
        if (i % 2 == 0) {
            cout << tablica[i] << endl;
        }
    }
    cout << "Słowa z tablicy, ilość liter w których jest większa od 3: " << endl;
    for (int i = 0; i < 5; i++) {
        if (tablica[i].size() > 3) {
            cout << tablica[i] << endl;
        }
    }
    return 0;
}

  2 a) zdefiniuj i incjalizuj wektor z 10 liczbami double wypisz na konsoli wartosc bezwgledna wszystkich liczb wektora przy pomocy petli a po tym wypisz na konsoli dodatnie liczby wektora przy pomocy for_each
  
  #include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main()
{
    vector<double> wektor {1.1,-2.2,3.3,-4.4,5.5,-6.6,7.7,-8.8,9.9,-10.10};
    cout << "Wartość bezwzględna liczb wektora: " << endl;
    for (int i = 0; i < wektor.size(); i++)
    {
        cout << abs(wektor[i]) << endl;
    }
    cout << "Dodatnie liczby wektora: " << endl;
    for_each(wektor.begin(), wektor.end(), [](double x) {
        if (x > 0) {
            cout << x << endl;
        }
    });
    return 0;
}
 b) 
#include <iostream>
#include <iostream>
#include <vector>
using namespace std;

int main()
{
    vector<int> wektor {1,2,3,4,5,6,7,8,9,10,11,12,13,14,15};
    int max_elem = wektor[0];
    int max_elem_idx = 0;
    for (int i = 1; i < wektor.size(); i++) {
        if (wektor[i] > max_elem) {
            max_elem = wektor[i];
            max_elem_idx = i;
        }
    }
    cout << "Maksymalny element wektora: " << max_elem << endl;
    cout << "Indeks ostatniego wystąpienia maksymalnego elementu: " << max_elem_idx << endl;
    return 0;
}

________________________________________________poprawa

#include <iostream>
using namespace std;

int main() {
    double num1, num2, num3;
    double max, sumAbs;

    cout << "Wprowadz trzy liczby typu double: ";
    cin >> num1 >> num2 >> num3;

    // Obliczanie maksymalnej liczby
    max = num1;
    if (num2 > max) {
        max = num2;
    }
    if (num3 > max) {
        max = num3;
    }

    // Obliczanie sumy wartości bezwzględnych
    sumAbs = 0;
    if (num1 < 0) sumAbs -= num1; else sumAbs += num1;
    if (num2 < 0) sumAbs -= num2; else sumAbs += num2;
    if (num3 < 0) sumAbs -= num3; else sumAbs += num3;
    cout << "Maksymalna liczba: " << max << endl;
    cout << "Suma wartosci bezwzglednych: " << sumAbs << endl;
    return 0;
}



#include <iostream>
using namespace std;

bool check_triangle(double a, double b, double c) {
    if (a <= 0 || b <= 0 || c <= 0) {
        cout << "Error: number should be positive" << endl;
        return false;
    }
    if (a + b > c && a + c > b && b + c > a) {
        return true;
    } else {
        return false;
    }
}

int main() {
    double a, b, c;
    cout << "Wprowadz 3 boki trojkata: ";
    cin >> a >> b >> c;
    if (check_triangle(a, b, c)) {
        cout << "Podane liczby moga byc bokami trojkata" << endl;
    } else {
        cout << "Podane liczby nie moga byc bokami trojkata" << endl;
    }
    return 0;
}



#include <iostream>
using namespace std;

string encrypt(string s, int n) {
    string encrypted = "";
    for (int i = 0; i < s.length(); i++) {
        encrypted += char(int(s[i]) + n);
    }
    return encrypted;
}

int main() {
    string s;
    int n;
    cout << "Wprowadz tekst: ";
    cin >> s;
    cout << "Wprowadz liczbe: ";
    cin >> n;
    cout << "Zaszyfrowany tekst: " << encrypt(s, n) << endl;
    return 0;
}


#include <iostream>
using namespace std;

int f(int n) {
    if (n == 0) return 0;
    if (n == 1) return 1;
    return 2 * f(n-1) + f(n-2);
}

int main() {
    int n;
    cout << "Wprowadz n: ";
    cin >> n;
    cout << "f(" << n << ") = " << f(n) << endl;
    return 0;
}





  
  
                                              


