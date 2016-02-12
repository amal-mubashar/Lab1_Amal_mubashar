# Lab1_Amal_mubashar

#ifndef ALGORITHM_H
#define ALGORITHM_H

#include<iostream>
#include<conio.h>
#include <stdio.h>

using namespace std;

int algorithm(){

	int a[100][100], b[100][100], c[100][100];

	int g;

	int m1, m2, m3, m4, m5, m6, m7;
	int c11, c12, c21, c22;

	int i, j;
	int x = 2;
	int y = 2;
	int m = 2;
	int n = 2;

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

	cout << "\n\n";


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



	m1 = (a[0][0] + a[1][1]) * (b[0][0] + b[1][1]);
	m2 = (a[1][0] + a[1][1]) * b[0][0];
	m3 = a[0][0] * (b[0][1] - b[1][1]);
	m4 = a[1][1] * (b[1][0] - b[0][0]);
	m5 = (a[0][0] + a[0][1]) * b[1][1];
	m6 = (a[1][0] - a[0][0]) * (b[0][0] + b[0][1]);
	m7 = (a[0][1] - a[1][1]) * (b[1][0] + b[1][1]);


	c[0][0] = m1 + m4 - m5 + m7;
	c[0][1] = m3 + m5;
	c[1][0] = m2 + m4;
	c[1][1] = m1 - m2 + m3 + m6;


	cout << "\n\nMultiplication of Matrix A and Matrix B :\n\n";

	for (i = 0; i<x; i++)
	{
		for (j = 0; j<n; j++)
		{
			cout << "\t" << c[i][j];
		}
		cout << "\n\n";
	}
	cin >> g;
	//getchar();
	return 0;

}

#endif
