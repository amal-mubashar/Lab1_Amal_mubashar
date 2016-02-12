# Lab1_Amal_mubashar

#ifndef ITERATIVE_H
#define ITERATIVE_H

#include<iostream>
#include<conio.h>

using namespace std;

int iterative(){

	
	int a[100][100], b[100][100], c[100][100];

	int g;

	int m1, m2, m3, m4, m5, m6, m7;
	int c11, c12, c21, c22;

	int x, y, i, j, m, n;

	cout << "\nEnter the number of rows and columns for Matrix A:\n\n";
	cin >> x >> y;



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

	cout << "\nEnter the number of rows and columns for Matrix B:::\n\n";
	cin >> m >> n;

	// m denotes number rows in matrix B
	// n denotes number columns in matrix B


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

	if (y == m)
	{

		for (i = 0; i<x; i++)
		{
			for (j = 0; j<n; j++)
			{
				c[i][j] = 0;
				for (int k = 0; k<m; k++)
				{
					c[i][j] = c[i][j] + a[i][k] * b[k][j];
				}
			}
		}

		cout << "\n-----------------------------------------------------------\n";

		cout << "\n\nMultiplication of Matrix A and Matrix B :\n\n";

		for (i = 0; i<x; i++)
		{
			for (j = 0; j<n; j++)
			{
				cout << "\t" << c[i][j];
			}
			cout << "\n\n";
		}
	}

	else
	{
		cout << "\n\nMultiplication is not possible";
	}

	
	//getch();
	return 0;
	cin >> g;
}

#endif
