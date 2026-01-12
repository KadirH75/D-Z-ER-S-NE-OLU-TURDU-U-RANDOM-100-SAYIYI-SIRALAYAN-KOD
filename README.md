#include <iostream>
#include <cstdlib>
#include <time.h>
using namespace std;
int main()
{int x, dizi[100];
srand(time(0));
for (int i = 0; i < 100; i++) {
	dizi[i] = rand()%1000;
	cout << dizi[i] << " - ";
}
cout << "\n";

for (int j = 0; j < 100; j++) {
	for (int y = 0; y < 100; y++) {
		if (dizi[j] < dizi[y]) {
			x = dizi[j];
			dizi[j] = dizi[y];
			dizi[y] = x;
		}
	}
}
for (int t = 0; t < 100; t++) {
	cout << dizi[t] << "-";
}
}
