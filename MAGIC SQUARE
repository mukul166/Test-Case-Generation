import os,sys 
import random
import string 
import networkx as nx 
import math
import numpy as np 
def read():
	sys.stdout = open('output.txt', 'w') 
def solve():
	T=100
	print(T)
	for i in range(T):
		n = random.randrange(1,100) 
		print(n)
		x = n 
		m = n 
		table = [[0 for i in range(n)] for i in range(n)]
		matrix =[[0 for i in range(n)] for i in range(n)]
		for i in range(n):
			for j in range(n):
				matrix[i][j] = random.randrange(1,n*n+1)
		k=m*n
		mi = math.floor((float(m)/2))
		middle = int(mi)
		n = n-1
		table[middle][n] = 1
		for i in range(2, k+1):
			try:
				middle = middle + 1
				n = n + 1
				if(table[middle][n] == 0):
					table[middle][n] = i
				else:
					middle = middle - 1
					n = n -2
					table[middle][n] = i;
			except:
				try:
					if(table[middle][0] == 0):
						n = 0
						table[middle][n] = i 
					else:
						table[middle][n-1] = i 
				except:
					try:
						middle = 0 
						table[middle][n] = i 
					except:
						middle  = middle - 1
						n = n - 1
						table[middle][n - 1] = i
		# print(table)
		p = random.choice([0,1])
		if(p == 1):
			table = matrix
		row = random.randrange(0,x)
		col = random.randrange(0,x)
		table[row][col] = 0
		for i in range(x):
			for j in range(x):
				print(table[i][j], end = " ")
			print()
		print('~')
if __name__=="__main__":
	read()
	solve() 
