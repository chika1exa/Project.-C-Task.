# Project.-C-Task.
Неупорядочеченный массив может иметь соответствующие элементы. Из каждой группы одинаковых элементов оставьте только один, удалив остальные и «прижимая» массив к его началу. Данный массив надо остортировать методом вставками. 

'#include <iostream>
#include <conio.h>
#include <cstdlib>
#include <ctime>
#include <iomanip> 


using namespace std;

int main() {
int N = 10;



setlocale(LC_ALL, "Russian");
srand(time(NULL));

int arr[N];


cout << "Исходный массив:" << endl;
for (int i = 0; i < N; i++) {
arr[i] = rand() % N; 
cout << setw(4) << arr[i] << " ";
}
cout << endl << endl;

int k = 0;

for(int i = 0; i < N; i++){
	int m = i;
	k = arr[i];
	for(int j = i + 1; j < N; j++){
		if(arr[j] == k){
		m = j;
		k = arr[j];
		N--;	
			
			
		}
	}
arr[m] = arr[i];
arr[i] = k;
}
	cout << endl << endl;
	cout << "Исходный массив:" << endl;
	for(int i = 0; i < N; i++){
		cout << setw(4) << arr[i] <<"  " ;
	}
getch();
return 0;


}'





