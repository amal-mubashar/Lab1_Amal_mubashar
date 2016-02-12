# Lab1_Amal_mubashar

#include<iostream>
#include<conio.h>
#include "algorithm.h""
#include "Iterative.h"

using namespace std;

int test();

int main()
{


	int a[100][100], b[100][100], c[100][100];

	int g;

	int m1, m2, m3, m4, m5, m6, m7;
	int c11, c12, c21, c22;

	int i, j;
	int option;
	int x = 2;
	int y = 2;
	int m = 2;
	int n = 2;

///////////////////////////////////////////////////////////////////////////////

	cout << "\n\nEnter 1 - iterative method :\n\n";
	cout << "\n\nEnter 2 - strassens method :\n\n";
	cout << "\n\nEnter 3 - test results :\n\n";
	cin >> option;

	switch (option){
	
	case 1: iterative();
	case 2: algorithm();
	case 3: test();

	}
	
	cin >> g;
	return 0;
}


int test()
{


	int a[100][100], b[100][100], c[100][100];

	int g;

	int m1, m2, m3, m4, m5, m6, m7;
	int c11, c12, c21, c22;

	int i, j;
	int option;
	int x = 2;
	int y = 2;
	int m = 2;
	int n = 2;


	//cout << "\nEnter the number of rows and columns for Matrix A:\n\n";
	//cin >> x >> y;

	for (int i = 0; i < x; ++i)
	{

		for (int j = 0; j < y; ++j)
			a[i][j] = rand() % (x*y);
	}

	cout << "\n\nMatrix A :\n\n";

	for (i = 0; i<x; i++)
	{
		for (j = 0; j<y; j++)
		{
			cout << "\t" << a[i][j];
		}
		cout << "\n\n";
	}

	cout << "\n-----------------------------------------------------------\n";

	//cout << "\nEnter the number of rows and columns for Matrix B:::\n\n";
	//cin >> m >> n;

	for (int i = 0; i < m; ++i)
	{

		for (int j = 0; j < n; ++j)
			b[i][j] = rand() % (x*y);
	}


	cout << "\n\nMatrix B :\n\n";

	for (i = 0; i<m; i++)
	{
		for (j = 0; j<n; j++)
		{
			cout << "\t" << b[i][j];
		}
		cout << "\n\n";
	}

	if (iterative() == algorithm()){

		cout << "\nTest successful :\n\n";
	}

	else {
		cout << "\nTest failed :\n\n";
	}

	return 0;

	///////////////////////////////////////////////////////////////////////////////
}
