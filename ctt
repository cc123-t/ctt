#include<stdio.h>
#include<windows.h>  
#include<conio.h>   
#include<stdlib.h>
#include<time.h>

char map[9][12]=
{   
"*#*********",
"***###*###*",
"###**#****#",
"*#**###**#*",
"***********",
"#####*##*##",
"**#****##*E",
"***#*###**#",
"*#*********",
};


int curX=0,curY=0;  

void printPerson()
{
	COORD pos;  
	pos.X = curX ;
	pos.Y = curY ;
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),pos);
}
void printMap()
{
	int i,j;
	for(i=0;i<9;i++)
	{
		for(j=0;j<12;j++)
		{
			printf("%c",map[i][j]);
		}
		printf("\n");
	}
}
void Move(char dir)
{
	switch(dir)
	{
		case 'w':
			curY--;
			if(curY<0) curY=0;
			if(map[curY][curX]=='#') curY++;
			break;
		case 's':
			curY++;
			if(curY>=9) curY=9-1;
			if(map[curY][curX]=='#') curY--;
			break;
		case 'a':
			curX--;
			if(curX<0) curX=0;
			if(map[curY][curX]=='#') curX++;
			break;
		case 'd':
			curX++;
			if(curX>=12) curX=12-1;
			if(map[curY][curX]=='#') curX--;
			break;	
	}
}
void main()
{
	char t;
	while(1)
	{
		system("cls");
		printMap();
		printPerson();		
		t=getch();        
		Move(t);
		if(map[curY][curX]=='E')
		{
			printf("恭喜，成功通过！");
			break; 
		} 
	}
}
