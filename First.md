Задача с рандомизатором чисел C++
{
	#include <iostream>
	using namespace std;
	bool Delete(int *array, int &lenAr, int nom);
	int main()
	{
		int k, i, j, g;
		g = 10;
		int const num = 10;
		int arr[num];
		int randomDigits[10] = {};
		for (int i = 0; i < num; i++) {
			randomDigits[i] = rand(); // запись случайного числа, которое вернет rand()
			cout << randomDigits[i] << endl;
			cout << "Value of " << i << " element is " << arr[i] << endl;
		}
	
		cout << "Enter - k " << endl;
		cin >> k;
		cout << " Array with removed element " << endl;
		if (k <= num)
		{
			Delete(arr, g, k);
	
			for (int i = 0; i < num; i++)
			{
				cout << arr[i] << "  "; // вывод сгенерированного числа
			}
	
			cout << endl;
		}
		else if (k > num)
		{
			for (int i = 0; i < num; i++)
			{
				if (!(arr[i] % 2 == 0) && (arr[i] < k))
				{
	
					cout << arr[i] << " element " << endl;
	
				}
	
			}
		}
		
	
		system("pause>nul");
		return 0;
	}
	bool Delete(int *array, int &lenAr, int nom)
	{
		if (nom > lenAr || nom < 1)
		{
			cout << "Ошибка удаления" << endl;
			return false;
		}
	
		for (int ix = nom - 1; ix < lenAr - 1; ix++)
		{
			array[ix] = array[ix + 1];
		}
		lenAr--;
		return true;
	}
}
