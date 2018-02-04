#include<windows.h>
#include<stdio.h>
#include<GL/glut.h>
int n = 0, i, j, f;
int n1 = 0;
int n2 = 0;
int n3 = 0;
int n4 = 0;
int n5 = 0;
int count2 = 0;
int count3 = 0;
int counts = 0;
char buffer[10] = {'\0' };
/*struct arr
{
	int counts;
	//int q;
}ar;*/
int done111=0,done1 = 0, done2 = 0, done3 = 0, done4 = 0,done5=0,done6=0,done7=0,done8=0,done9=0,done10=0,done11=0,done12=0,done13=0,done14=0,done15=0,done16=0,done17=0,done18=0,done19=0,done20=0,done21=0,done22=0,done23=0,done24=0;
int level = 0;
int flag[25];
int flag2[25];
int flag3[25];
int flag4[25];
int flag5[25];
int end1 = 0;
int end2 = 0;
int end3 = 0;
int end4 = 0;
int end5 = 0;
int *e5 = &end5;
int *e4 = &end4;
int *e3 = &end3;
int *e2 = &end2;
int *e1 = &end1;
//int result1[25];
int firstcall = 0;
int *fc = &firstcall;
int fin = 1; ///for level 3........
//int *h=&n;
int *p = &level;
int *q = flag;
void *currentfont;
int result1[25] = { 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1 };
int result2[25] = { 1, 0, 1, 0, 0, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 0, 0, 1, 0 };
//int result3[25]={1,0,0,0,0,1,1,0,1,0,1,0,0,1,0,1,0,1,0,1,1,0,0,0,0};
int result3[25] = { 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 0, 0, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1 };
int result4[25] = { 1, 1, 0, 1, 1, 1, 1, 1, 1, 0, 1, 0, 0, 0, 0, 1, 0, 1, 1, 1, 1, 1, 1, 0, 1 };
//int result4[25]={1,0,0,0,0,1,1,0,1,0,1,0,0,0,0,1,0,1,0,1,1,0,0,0,0};
int result5[25] = { 1, 1, 1, 1, 1, 0, 0, 1, 0, 1, 0, 1, 1, 1, 1, 0, 1, 0, 1, 0, 0, 1, 1, 1, 1 };
//int result5[25]={1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0};
int win = 0;
int win1 = 0, win2 = 0, win3 = 0, win4 = 0, win5 = 0;
int *w1 = &win1;
int *w2 = &win2;
int *w3 = &win3;
int *w4 = &win4;
int *w5 = &win5;



//int check(int x,int y,int m,int count);//declaration..............

int check(int x, int y, int m, int count);





void setFont(void *font)
{
	currentfont = font;
}


void myInit(void)
{

	glClearColor(0.0, 0.0, 0.0, 0.0);
	glColor3f(1.0f, 1.0f, 1.0f);
	glPointSize(6.0);
	gluOrtho2D(0.0, 640.0, 0.0, 480.0);
	setFont(GLUT_BITMAP_HELVETICA_18);

}

void drawstring(float x, float y, float z, char *str)
{
	char *c;
	glRasterPos3f(x, y, z);

	for (c = str; *c != '\0'; c++)
	{
		//	printf("%s",c);
		glutBitmapCharacter(currentfont, *c);
		//return ;
	}
}


void drawline(int x, int y)//**************************DRAW LINE***************************************************
{
//PlaySound("Shot.wav", NULL, SND_ASYNC);
	//glClear(GL_COLOR_BUFFER_BIT);
	printf("\n%d %d\n", x, y);
	if (y <= 30)//item 1...horizontal
	{
		if (y >= 20)
		{
			if (x >= 105)
			{
				if (x <= 155)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(105, 455);
					glVertex2i(155, 455);
					glEnd();
					glFlush();

					q += 1;
					*q = 0;
					q = flag;
				}
			}
		}
//		y++;

	}

	if (x <= 215)//item 2
	{
		if (x >= 165)
		{
			if (y <= 30)
			{
				if (y >= 20)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(165, 455);
					glVertex2i(215, 455);
					glEnd();
					glFlush();
					q += 2;
					*q = 0;
					q = flag;
				}
			}//e o while
		}
		x++;


	}

	if (x <= 275)//item 3
	{
		if (x >= 225)
		{
			if (y >= 20)
			{
				if (y <= 30)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(225, 455);
					glVertex2i(275, 455);
					glEnd();
					glFlush();
					q += 3;
					*q = 0;
					q = flag;
				}
			}// e o while
		}
		x++;

	}

	if (x <= 105)//item 4....30 to 80>>y
	{
		if (x >= 95)
		{
			if (y >= 30)
			{
				if (y <= 80)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(100, 400);
					glVertex2i(100, 450);
					glEnd();
					glFlush();
					q += 4;
					*q = 0;
					q = flag;
				}
			}// e o while
		}
		x++;

	}

	if (x <= 165)//item 5....30 to 80>>y
	{
		if (x >= 155)
		{
			if (y >= 30)
			{
				if (y <= 80)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(160, 400);
					glVertex2i(160, 450);
					glEnd();
					glFlush();
					q += 5;
					*q = 0;
					q = flag;
				}
			}
		}
		x++;

	}

	if (x <= 225)//item 6....30 to 80>>y
	{
		if (x >= 215)
		{
			if (y >= 30)
			{
				if (y <= 80)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(220, 400);
					glVertex2i(220, 450);
					glEnd();
					glFlush();
					q += 6;
					*q = 0;
					q = flag;
				}//e o while
			}
		}
		x++;

	}

	if (x <= 285)//item 7....30 to 80>>y
	{
		if (x >= 275)
		{
			if (y >= 30)
			{
				if (y <= 80)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(280, 400);
					glVertex2i(280, 450);
					glEnd();
					glFlush();
					q += 7;
					*q = 0;
					q = flag;
				}
			}
		}//e o while
		x++;

	}

	if (y <= 90)//item 8...horiz..
	{
		if (y >= 80)
		{
			if (x >= 105)
			{
				if (x <= 155)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(105, 395);
					glVertex2i(155, 395);
					glEnd();
					glFlush();
					q += 8;
					*q = 0;
					q = flag;
				}
			}
		}
		y++;

	}

	if (x <= 215)//item 9...horiz
	{
		if (x >= 165)
		{
			if (y >= 80)
			{
				if (y <= 90)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(165, 395);
					glVertex2i(215, 395);
					glEnd();
					glFlush();
					q += 9;
					*q = 0;
					q = flag;
				}
			}//e o while
		}
		x++;

	}

	if (x <= 275)//item 10
	{
		if (x >= 225)
		{
			if (y >= 80)
			{
				if (y <= 90)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(225, 395);
					glVertex2i(275, 395);
					glEnd();
					glFlush();
					q += 10;
					*q = 0;
					q = flag;
				}
			}// e o while
		}
		x++;

	}

	if (y >= 90)//item 11....90 to 140>>y
	{
		if (y <= 140)
		{
			if (x >= 100 || x <= 110)
			{
				if (x <= 110)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(100, 390);
					glVertex2i(100, 340);
					glEnd();
					glFlush();
					q += 11;
					*q = 0;
					q = flag;
				}
			}// e o while
		}
		x++;


	}

	if (x <= 170)//item 12....90 to 140>>y
	{
		if (x >= 160)
		{
			if (y >= 90)
			{
				if (y <= 140)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(160, 390);
					glVertex2i(160, 340);
					glEnd();
					glFlush();
					q += 12;
					*q = 0;
					q = flag;
				}
			}
		}
		x++;

	}

	if (x <= 230)//item 13...90 to 140>>y
	{
		if (x >= 215)
		{
			if (y >= 90)
			{
				if (y <= 140)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(220, 390);
					glVertex2i(220, 340);
					glEnd();
					glFlush();
					q += 13;
					*q = 0;
					q = flag;
				}
			}
		}//e o while
		x++;

	}

	if (x <= 285)//item 14....90 to 140>>y
	{
		if (x >= 275)
		{
			if (y >= 90)
			{
				if (y <= 140)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(280, 390);
					glVertex2i(280, 340);
					glEnd();
					glFlush();
					q += 14;
					*q = 0;
					q = flag;
				}
			}//e o while
		}
		x++;

	}

	if (y <= 150)//item 15...horiz.y>>140 to 150
	{
		if (y >= 140)
		{
			if (x >= 105)
			{
				if (x <= 155)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(105, 335);
					glVertex2i(155, 335);
					glEnd();
					glFlush();
					q += 15;
					*q = 0;
					q = flag;
				}//e o while
			}
		}
		y++;

	}

	if (x <= 215)//item 16...horiz
	{
		if (x >= 165)
		{
			if (y >= 140)
			{
				if (y <= 150)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(165, 335);
					glVertex2i(215, 335);
					glEnd();
					glFlush();
					q += 16;
					*q = 0;
					q = flag;
				}
			}//e o while
		}
		x++;

	}

	if (x <= 275)//item 17...horiz
	{
		if (x >= 225)
		{
			if (y >= 140)
			{
				if (y <= 150)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(225, 335);
					glVertex2i(275, 335);
					glEnd();
					glFlush();
					q += 17;
					*q = 0;
					q = flag;
				}
			} // e o while
		}
		x++;

	}

	if (x >= 105)  //item 18....150 to 200>>y
	{
		if (x <= 115)
		{
			if (y >= 150)
			{
				if (y <= 200)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(100, 330);
					glVertex2i(100, 280);
					glEnd();
					glFlush();
					q += 18;
					*q = 0;
					q = flag;
				}
			}// e o while
		}
		x++;


	}

	if (x <= 180)//item 19....150 to 200>>y
	{
		if (x >= 170)
		{
			if (y >= 150)
			{
				if (y <= 200)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(160, 330);
					glVertex2i(160, 280);
					glEnd();
					glFlush();
					q += 19;
					*q = 0;
					q = flag;
				}
			}
		}
		x++;

	}

	if (x <= 230)//item 20...150 to 200>>y
	{
		if (x >= 220)
		{
			if (y >= 150)
			{
				if (y <= 200)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(220, 330);
					glVertex2i(220, 280);
					glEnd();
					glFlush();
					q += 20;
					*q = 0;
					q = flag;
				}
			}
		}//e o while
		x++;

	}

	if (x <= 285)//item 21....150 to 200>>y
	{
		if (x >= 275)
		{
			if (y >= 150)
			{
				if (y <= 200)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(280, 330);
					glVertex2i(280, 280);
					glEnd();
					glFlush();
					q += 21;
					*q = 0;
					q = flag;
				}
			}//e o while
		}
		x++;

	}

	if (y <= 220)//item 22...horiz.y>>190 to 210
	{
		if (y >= 200)
		{
			if (x >= 105)
			{
				if (x <= 155)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(105, 275);
					glVertex2i(155, 275);
					glEnd();
					glFlush();
					q += 22;
					*q = 0;
					q = flag;
				}//e o while
			}
		}
		y++;

	}

	if (x <= 215)//item 23...horiz..y>>190to 210
	{
		if (x >= 165)
		{
			if (y >= 190)
			{
				if (y <= 210)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(165, 275);
					glVertex2i(215, 275);
					glEnd();
					glFlush();
					q += 23;
					*q = 0;
					q = flag;
				}
			}//e o while
		}
		x++;

	}


	if (x <= 275)//item 24...horiz.. y>>190 to 210
	{
		if (x >= 225)
		{
			if (y >= 200)
			{
				if (y <= 210)
				{
					glColor3f(0.0, 0.0, 0.0);
					glLineWidth(10.0);
					glBegin(GL_LINES);
					glVertex2i(225, 275);
					glVertex2i(275, 275);
					glEnd();
					glFlush();
					q += 24;
					*q = 0;
					q = flag;
				}
			} // e o while
		}
		x++;

	}
}




void box()
{
	glLineWidth(5.0);
	glColor3f(0.0f, 1.0f, 1.0f);
	glBegin(GL_LINE_LOOP);

	glVertex2i(500, 420);
	glVertex2i(580, 420);

	glVertex2i(580, 250);
	glVertex2i(500, 250);

	glEnd();

	glBegin(GL_LINES);
	glVertex2i(500, 284);
	glVertex2i(580, 284);

	glVertex2i(500, 318);
	glVertex2i(580, 318);

	glVertex2i(500, 352);
	glVertex2i(580, 352);

	glVertex2i(500, 386);
	glVertex2i(580, 386);
	glEnd();
	//glLineWidth(4.0);
	//glColor3f(0.0, 0.0, 1.0);
	/*	glBegin(GL_LINE_LOOP);
	glVertex2i(40,160);
	glVertex2i(40,190);
	glVertex2i(500,190);
	glVertex2i(500,160);
	glEnd();*/


	glFlush();

}

void rite1()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(0, 1, 0);
	glVertex2i(520, 410);
	glVertex2i(525, 400);

	glVertex2i(525, 400);
	glVertex2i(555, 412);
	glEnd();
}

void rite2()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(0, 1, 0);
	glVertex2i(520, 375);
	glVertex2i(525, 365);

	glVertex2i(525, 365);
	glVertex2i(555, 377);
	glEnd();
}

void rite3()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(0, 1, 0);

	glVertex2i(520, 340);
	glVertex2i(525, 330);

	glVertex2i(525, 330);
	glVertex2i(555, 342);
	glEnd();
}


void rite4()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(0, 1, 0);

	glVertex2i(520, 305);
	glVertex2i(525, 295);

	glVertex2i(525, 295);
	glVertex2i(555, 307);
	glEnd();
}

void rite5()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(0, 1, 0);
	glVertex2i(520, 270);
	glVertex2i(525, 260);

	glVertex2i(525, 260);
	glVertex2i(555, 272);
	glEnd();
}

void wrong1()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(1, 0, 0);
	glVertex2i(520, 410);
	glVertex2i(555, 395);

	glVertex2i(520, 395);
	glVertex2i(555, 410);
	glEnd();
}

void wrong2()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(1, 0, 1);
	glVertex2i(520, 375);
	glVertex2i(555, 360);

	glVertex2i(520, 360);
	glVertex2i(555, 375);
	glEnd();
}

void wrong3()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(1, 0, 1);
	glVertex2i(520, 340);
	glVertex2i(555, 325);

	glVertex2i(520, 325);
	glVertex2i(555, 342);
	glEnd();
}


void wrong4()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(1, 0, 1);
	glVertex2i(520, 307);
	glVertex2i(555, 292);

	glVertex2i(520, 292);
	glVertex2i(555, 309);
	glEnd();
}

void wrong5()
{
	glLineWidth(5.0);
	glBegin(GL_LINES);
	glColor3f(1, 0, 1);
	glVertex2i(520, 272);
	glVertex2i(555, 257);

	glVertex2i(520, 257);
	glVertex2i(555, 274);
	glEnd();
}









void drawgrid1()//............................to display grid in first menu................
{
	//glClear(GL_COLOR_BUFFER_BIT);

	//glColor3i(1,0,0); 
	//glPointSize(3.0);
	//glBegin(GL_POINTS);
	//glVertex2i(550,550);
	//glEnd();
	// glFlush();
	//printf("jhdbcwguefkj");


	//	glColor3f(1.0,1.0,1.0);
	//drawstring(350.0,200.0,0.0,"LEVEL1");
	glClear(GL_COLOR_BUFFER_BIT);

	glColor3f(1.0, 1.0, 0.0);//yellow color for text
	//glFlush();
	drawstring(200.0, 200.0, 0.0, "TASK 1");
	glColor3f(1.0, 0.5, 0.0);
	drawstring(30.0, 170.0, 0.0, "Remove four lines to stay with five same squares");

	box();

	glFlush();



	glLineWidth(10.0);
	glColor3f(1.0, 0.0, 1.0);



	glBegin(GL_LINES);
	glVertex2i(100, 450);
	glVertex2i(100, 400);

	glVertex2i(105, 455);
	glVertex2i(155, 455);

	glVertex2i(160, 450);
	glVertex2i(160, 400);

	glVertex2i(105, 395);
	glVertex2i(155, 395);

	glVertex2i(165, 455);
	glVertex2i(215, 455);

	glVertex2i(220, 450);
	glVertex2i(220, 400);

	glVertex2i(165, 395);
	glVertex2i(215, 395);

	glVertex2i(225, 455);
	glVertex2i(275, 455);

	glVertex2i(280, 450);
	glVertex2i(280, 400);

	glVertex2i(225, 395);
	glVertex2i(275, 395);


	glVertex2i(100, 390);
	glVertex2i(100, 340);

	glVertex2i(160, 390);
	glVertex2i(160, 340);

	glVertex2i(105, 335);
	glVertex2i(155, 335);

	glVertex2i(165, 335);
	glVertex2i(215, 335);

	glVertex2i(220, 390);
	glVertex2i(220, 340);

	glVertex2i(225, 335);
	glVertex2i(275, 335);

	glVertex2i(280, 390);
	glVertex2i(280, 340);

	glVertex2i(100, 330);
	glVertex2i(100, 280);

	glVertex2i(105, 275);
	glVertex2i(155, 275);

	glVertex2i(160, 330);
	glVertex2i(160, 280);


	glVertex2i(165, 275);
	glVertex2i(215, 275);

	glVertex2i(220, 330);
	glVertex2i(220, 280);

	glVertex2i(225, 275);
	glVertex2i(275, 275);

	glVertex2i(280, 330);
	glVertex2i(280, 280);

	glEnd();
	glBegin(GL_POLYGON);//to give the box for next
	glColor3f(1.0, 0.0, 0.0);
	glVertex2i(510.0, 190.0);
	glVertex2i(555.0, 190.0);

	glVertex2i(555.0, 160.0);
	glVertex2i(510.0, 160.0);
	glEnd();

	glColor3f(0.0, 1.0, 1.0);
	
	drawstring(510.0, 130.0, 0.0, "NEXT");
	glFlush();
	glBegin(GL_POLYGON);//to give the box for exit
	glColor3f(1.0, 1.0, 0.0);
	glVertex2i(510.0, 100.0);
	glVertex2i(555.0, 100.0);

	glVertex2i(555.0, 70.0);
	glVertex2i(510.0, 70.0);
	glEnd();

	glColor3f(1.0, 1.0, 1.0);
	
	drawstring(510.0, 40.0, 0.0, "EXIT");
	glFlush();
	//glVertex2i(580.0,200.0);



	//glVertex2i(580.0,170.0);
	//glVertex2i(500.0,170.0);
	//glVertex2i(500.0,170.0);





	glFlush();
	//glPointSize(5);
	//glColor3f(1.0,1.0,1.0);
	//drawstring(240.0,100.0,0.0,"LOGIC GRID");
	//glFlush();
	//drawstring(500.0,380.0,0.0,"1 HELP");
	//drawstring(500.0,340.0,0.0,"2 PLAY");
	//drawstring(500.0,300.0,0.0,"3 EXIT");
	//glFlush();
	//drawstring(


}


void drawgrid2()//.........................for 2nd level...to display grid in first menu................
{
	//glClear(GL_COLOR_BUFFER_BIT);

	glColor3i(0, 0, 1);
	glPointSize(3.0);
	glBegin(GL_POINTS);
	glVertex2i(550, 550);
	glEnd();
	glFlush();

	//glClear(GL_COLOR_BUFFER_BIT);
	glColor3f(1.0, 1.0, 1.0);
	//drawstring(350.0,200.0,0.0,"LEVEL1");

	glColor3f(1.0, 1.0, 0.0);
	glFlush();
	drawstring(215.0, 200.0, 0.0, "TASK 2");
	glColor3f(1.0, 0.5, 0.5);
	drawstring(50.0, 170.0, 0.0, "Remove eight lines to stay with five same squares");
	//drawstring(510.0,150.0,0.0,"NEXT");
	box();

	glFlush();



	glLineWidth(10.0);
	glColor3f(0.0, 0.6, 0.0);



	glBegin(GL_LINES);
	glVertex2i(100, 450);
	glVertex2i(100, 400);

	glVertex2i(105, 455);
	glVertex2i(155, 455);

	glVertex2i(160, 450);
	glVertex2i(160, 400);

	glVertex2i(105, 395);
	glVertex2i(155, 395);

	glVertex2i(165, 455);
	glVertex2i(215, 455);

	glVertex2i(220, 450);
	glVertex2i(220, 400);

	glVertex2i(165, 395);
	glVertex2i(215, 395);

	glVertex2i(225, 455);
	glVertex2i(275, 455);

	glVertex2i(280, 450);
	glVertex2i(280, 400);

	glVertex2i(225, 395);
	glVertex2i(275, 395);


	glVertex2i(100, 390);
	glVertex2i(100, 340);

	glVertex2i(160, 390);
	glVertex2i(160, 340);

	glVertex2i(105, 335);
	glVertex2i(155, 335);

	glVertex2i(165, 335);
	glVertex2i(215, 335);

	glVertex2i(220, 390);
	glVertex2i(220, 340);

	glVertex2i(225, 335);
	glVertex2i(275, 335);

	glVertex2i(280, 390);
	glVertex2i(280, 340);

	glVertex2i(100, 330);
	glVertex2i(100, 280);

	glVertex2i(105, 275);
	glVertex2i(155, 275);

	glVertex2i(160, 330);
	glVertex2i(160, 280);


	glVertex2i(165, 275);
	glVertex2i(215, 275);

	glVertex2i(220, 330);
	glVertex2i(220, 280);

	glVertex2i(225, 275);
	glVertex2i(275, 275);

	glVertex2i(280, 330);
	glVertex2i(280, 280);

	glEnd();
	glFlush();

	glLineWidth(5.0);
	glBegin(GL_POLYGON);
	//glBegin(GL_POLYGON);
	glColor3f(0.8, 0.7, 0.0);
	glVertex2i(510.0, 190.0);
	glVertex2i(555.0, 190.0);

	glVertex2i(555.0, 160.0);
	glVertex2i(510.0, 160.0);
	glEnd();

	glColor3f(0.0, 0.5, 0.5);
	glFlush();
	drawstring(510.0, 130.0, 0.0, "NEXT");



	glFlush();
	glBegin(GL_POLYGON);//to give the box for next
	glColor3f(1.0, 0.0, 0.0);
	glVertex2i(510.0, 100.0);
	glVertex2i(555.0, 100.0);

	glVertex2i(555.0, 70.0);
	glVertex2i(510.0, 70.0);
	glEnd();

	glColor3f(1.0, 1.0, 1.0);

	drawstring(510.0, 40.0, 0.0, "EXIT");
	glFlush();
}


void drawgrid3()//.........................for 3rd level...to display grid in first menu................
{
	//glClear(GL_COLOR_BUFFER_BIT);

	glColor3i(0, 0, 1);
	glPointSize(3.0);
	glBegin(GL_POINTS);
	glVertex2i(550, 550);
	glEnd();
	glFlush();

	//glClear(GL_COLOR_BUFFER_BIT);
	glColor3f(1.0, 1.0, 1.0);


	glColor3f(1.0, 1.0, 0.0);
	glFlush();
	drawstring(200.0, 200.0, 0.0, "TASK 3");
	drawstring(50.0, 170.0, 0.0, "Remove 4 lines to stay with 1 big square");
	drawstring(120.0, 140.0, 0.0, "& 4 small squares");
	//drawstring(510.0,150.0,0.0,"NEXT");
	box();

	glFlush();



	glLineWidth(10.0);
	glColor3f(1.0, 0.0, 0.0);



	glBegin(GL_LINES);
	glVertex2i(100, 450);
	glVertex2i(100, 400);

	glVertex2i(105, 455);
	glVertex2i(155, 455);

	glVertex2i(160, 450);
	glVertex2i(160, 400);

	glVertex2i(105, 395);
	glVertex2i(155, 395);

	glVertex2i(165, 455);
	glVertex2i(215, 455);

	glVertex2i(220, 450);
	glVertex2i(220, 400);

	glVertex2i(165, 395);
	glVertex2i(215, 395);

	glVertex2i(225, 455);
	glVertex2i(275, 455);

	glVertex2i(280, 450);
	glVertex2i(280, 400);

	glVertex2i(225, 395);
	glVertex2i(275, 395);


	glVertex2i(100, 390);
	glVertex2i(100, 340);

	glVertex2i(160, 390);
	glVertex2i(160, 340);

	glVertex2i(105, 335);
	glVertex2i(155, 335);

	glVertex2i(165, 335);
	glVertex2i(215, 335);

	glVertex2i(220, 390);
	glVertex2i(220, 340);

	glVertex2i(225, 335);
	glVertex2i(275, 335);

	glVertex2i(280, 390);
	glVertex2i(280, 340);

	glVertex2i(100, 330);
	glVertex2i(100, 280);

	glVertex2i(105, 275);
	glVertex2i(155, 275);

	glVertex2i(160, 330);
	glVertex2i(160, 280);


	glVertex2i(165, 275);
	glVertex2i(215, 275);

	glVertex2i(220, 330);
	glVertex2i(220, 280);

	glVertex2i(225, 275);
	glVertex2i(275, 275);

	glVertex2i(280, 330);
	glVertex2i(280, 280);

	glEnd();
	glFlush();

	glLineWidth(5.0);
	glBegin(GL_POLYGON);

	glVertex2i(510.0, 190.0);
	glVertex2i(555.0, 190.0);

	glVertex2i(555.0, 160.0);
	glVertex2i(510.0, 160.0);
	glEnd();

	glColor3f(0.0, 0.0, 1.0);
	glFlush();
	drawstring(510.0, 130.0, 0.0, "NEXT");

	glFlush();
	glBegin(GL_POLYGON);//to give the box for next
	glColor3f(1.0, 1.0, 0.0);
	glVertex2i(510.0, 100.0);
	glVertex2i(555.0, 100.0);

	glVertex2i(555.0, 70.0);
	glVertex2i(510.0, 70.0);
	glEnd();

	glColor3f(1.0, 1.0, 1.0);

	drawstring(510.0, 40.0, 0.0, "EXIT");
	glFlush();
}//end of drawgrid3......................................................................


//drawgrid44444444444444444444444444444444444444444
void drawgrid4()//.........................for 4th level...to display grid in first menu................
{
	//glClear(GL_COLOR_BUFFER_BIT);

	glColor3i(0, 0, 1);
	glPointSize(3.0);
	glBegin(GL_POINTS);
	glVertex2i(550, 550);
	glEnd();
	glFlush();

	//glClear(GL_COLOR_BUFFER_BIT);
	glColor3f(1.0, 1.0, 1.0);


	glColor3f(1.0, 1.0, 0.0);
	glFlush();
	drawstring(200.0, 200.0, 0.0, "TASK 4");
	drawstring(50.0, 170.0, 0.0, "Remove 8 lines to stay with  4 same squares");
	//drawstring(510.0,150.0,0.0,"NEXT");
	box();

	glFlush();



	glLineWidth(10.0);
	glColor3f(1.0, 0.0, 0.0);



	glBegin(GL_LINES);
	glVertex2i(100, 450);
	glVertex2i(100, 400);

	glVertex2i(105, 455);
	glVertex2i(155, 455);

	glVertex2i(160, 450);
	glVertex2i(160, 400);

	glVertex2i(105, 395);
	glVertex2i(155, 395);

	glVertex2i(165, 455);
	glVertex2i(215, 455);

	glVertex2i(220, 450);
	glVertex2i(220, 400);

	glVertex2i(165, 395);
	glVertex2i(215, 395);

	glVertex2i(225, 455);
	glVertex2i(275, 455);

	glVertex2i(280, 450);
	glVertex2i(280, 400);

	glVertex2i(225, 395);
	glVertex2i(275, 395);


	glVertex2i(100, 390);
	glVertex2i(100, 340);

	glVertex2i(160, 390);
	glVertex2i(160, 340);

	glVertex2i(105, 335);
	glVertex2i(155, 335);

	glVertex2i(165, 335);
	glVertex2i(215, 335);

	glVertex2i(220, 390);
	glVertex2i(220, 340);

	glVertex2i(225, 335);
	glVertex2i(275, 335);

	glVertex2i(280, 390);
	glVertex2i(280, 340);

	glVertex2i(100, 330);
	glVertex2i(100, 280);

	glVertex2i(105, 275);
	glVertex2i(155, 275);

	glVertex2i(160, 330);
	glVertex2i(160, 280);


	glVertex2i(165, 275);
	glVertex2i(215, 275);

	glVertex2i(220, 330);
	glVertex2i(220, 280);

	glVertex2i(225, 275);
	glVertex2i(275, 275);

	glVertex2i(280, 330);
	glVertex2i(280, 280);

	glEnd();
	glFlush();

	glLineWidth(5.0);
	glBegin(GL_POLYGON);

	glVertex2i(510.0, 190.0);
	glVertex2i(555.0, 190.0);

	glVertex2i(555.0, 160.0);
	glVertex2i(510.0, 160.0);
	glEnd();

	glColor3f(0.0, 0.0, 1.0);
	glFlush();
	drawstring(510.0, 130.0, 0.0, "NEXT");


	glFlush();
	glBegin(GL_POLYGON);//to give the box for next
	glColor3f(1.0, 1.0, 0.0);
	glVertex2i(510.0, 100.0);
	glVertex2i(555.0, 100.0);

	glVertex2i(555.0, 70.0);
	glVertex2i(510.0, 70.0);
	glEnd();

	glColor3f(1.0, 1.0, 1.0);

	drawstring(510.0, 40.0, 0.0, "EXIT");
	glFlush();
}//end of drawgrid4......................................................................


void drawgrid5()//.........................for 4th level...to display grid in first menu................
{
	//glClear(GL_COLOR_BUFFER_BIT);

	glColor3i(0, 0, 1);
	glPointSize(3.0);
	glBegin(GL_POINTS);
	glVertex2i(550, 550);
	glEnd();
	glFlush();

	//glClear(GL_COLOR_BUFFER_BIT);
	glColor3f(1.0, 1.0, 1.0);


	glColor3f(1.0, 1.0, 0.0);
	glFlush();
	drawstring(200.0, 200.0, 0.0, "TASK 5");
	drawstring(50.0, 170.0, 0.0, "Remove 8 lines to stay with 2 squares");
	//drawstring(510.0,150.0,0.0,"NEXT");
	box();

	glFlush();



	glLineWidth(10.0);
	glColor3f(1.0, 0.0, 0.0);



	glBegin(GL_LINES);
	glVertex2i(100, 450);
	glVertex2i(100, 400);

	glVertex2i(105, 455);
	glVertex2i(155, 455);

	glVertex2i(160, 450);
	glVertex2i(160, 400);

	glVertex2i(105, 395);
	glVertex2i(155, 395);

	glVertex2i(165, 455);
	glVertex2i(215, 455);

	glVertex2i(220, 450);
	glVertex2i(220, 400);

	glVertex2i(165, 395);
	glVertex2i(215, 395);

	glVertex2i(225, 455);
	glVertex2i(275, 455);

	glVertex2i(280, 450);
	glVertex2i(280, 400);

	glVertex2i(225, 395);
	glVertex2i(275, 395);


	glVertex2i(100, 390);
	glVertex2i(100, 340);

	glVertex2i(160, 390);
	glVertex2i(160, 340);

	glVertex2i(105, 335);
	glVertex2i(155, 335);

	glVertex2i(165, 335);
	glVertex2i(215, 335);

	glVertex2i(220, 390);
	glVertex2i(220, 340);

	glVertex2i(225, 335);
	glVertex2i(275, 335);

	glVertex2i(280, 390);
	glVertex2i(280, 340);

	glVertex2i(100, 330);
	glVertex2i(100, 280);

	glVertex2i(105, 275);
	glVertex2i(155, 275);

	glVertex2i(160, 330);
	glVertex2i(160, 280);


	glVertex2i(165, 275);
	glVertex2i(215, 275);

	glVertex2i(220, 330);
	glVertex2i(220, 280);

	glVertex2i(225, 275);
	glVertex2i(275, 275);

	glVertex2i(280, 330);
	glVertex2i(280, 280);

	glEnd();
	glFlush();

	glLineWidth(5.0);
	/*glBegin(GL_POLYGON);

	glVertex2i(510.0, 190.0);
	glVertex2i(555.0, 190.0);

	glVertex2i(555.0, 160.0);
	glVertex2i(510.0, 160.0);
	glEnd();

	glColor3f(0.0, 0.0, 1.0);
	glFlush();
	drawstring(510.0, 130.0, 0.0, "EXIT");*/


	glFlush();
	glBegin(GL_POLYGON);//to give the box for next
	glColor3f(1.0, 1.0, 0.0);
	glVertex2i(510.0, 100.0);
	glVertex2i(555.0, 100.0);

	glVertex2i(555.0, 70.0);
	glVertex2i(510.0, 70.0);
	glEnd();

	glColor3f(1.0, 1.0, 1.0);

	drawstring(510.0, 40.0, 0.0, "EXIT");
	glFlush();

}//end of drawgrid5.....................................................................








void mymouse(int btn, int state, int x, int y)//********************************mouse*********************************
{
	int i;
	int j;

	int count0,count1, count4, count5, count2, count3;
	//int count2;
	//int count3;
	int r = 0, r1 = 0, r3 = 0, r4 = 0, r5 = 0;





	if (btn == GLUT_LEFT_BUTTON && state == GLUT_DOWN)
	{
		if (level == 0)
		{
			level = 0;
			count0 = 1;
			r = check(x, y, level, count0);
			level = 1;
		}
		if (level == 1)
		{
		//	counts = 0;
			level = 1;
			count1 = 4;
			int done2 = 0, done11 = 0, done14 = 0, done23 = 0;
			r = check(x, y, level, count1);
			if (r == 1 && n<count1)
			{
				drawline(x, y);
				n++;
			}
			else
			{
				printf("error");

			}



			if (n == count1 && end1 == 0)//safety loop******************************
			{
				q = flag;
				//int count2;
				for (i = 0; i<25; i++)//for begins......
				{//printf("%d",flag[i]);

					if (result1[i] == flag[i])
					{
						win1 = 1;
					}
					else
					{
						win1 = -1;

						break;
					}
				}//for ends........................
				if (win1 == 1)
				{
					//int i;
					printf("\nRIGHT!");
					glFlush();
					glColor3f(0.0, 1.0, 0.0);
					rite1();
					drawstring(300.0, 400.0, 0.0, "RIGHT!!!");
					counts = counts + 10;

					glFlush();
					//q=&flag;
					//*p=2;
					//int j;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}
					end1 = 1;
			//		int done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;

					//level=2;
				}
				else if (win1 == -1)
				{

					printf("\nWRONG!");

					glFlush();
					glColor3f(0.0, 0.0, 1.0);
					wrong1();
					drawstring(300.0, 400.0, 0.0, "WRONG!!!");
					glFlush();


					//int j;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}
					//level=2;					//q=&flag;
					//*p=2;

					end1 = 1;

				}
			}//s loop ends****************************************
		}//level1 ends.........................................................................................
		//level2....................................


		if ((x >= 510 && x <= 555) && (y >= 290 && y <= 320) && (level == 1)&&(end1==1))
		//if (level==1)
	{
			int count2=0;
			level = 2;

			glClear(GL_COLOR_BUFFER_BIT);
			drawgrid2();
			if (*w1 == 1)
				rite1();
			else if (*w1 == -1)
				wrong1();

			firstcall = 1;
			r1 = check(x, y, level, count2);
			
		}

		if (level == 2)//safety loop******************************************
		{

			count2 = 8;
			//drawgrid2();
			q = flag;

			firstcall = 0;

			r1 = check(x, y, level, count2);
			if (r1 == 1 && n1<count2)
			{
				drawline(x, y);
				n1++;
				//printf("hhh %d",n1);
			}
			else
			{
				printf("error2");
			}



			if (n1 == count2 && end2 == 0)//safety loop******************************
			{
				q = flag;
				for (i = 0; i<25; i++)//for begins......
				{
					printf("%d", flag[i]);
					if (result2[i] == flag[i])
						win2 = 1;
					else
					{
						win2 = -1;
						break;
					}
				}//for ends........................
				if (win2 == 1)
				{


					printf("\nRIGHT!");
					glFlush();
					glColor3f(0.0, 1.0, 0.0);
					rite2();
					drawstring(300.0, 400.0, 0.0, "RIGHT!!!");
					counts = counts + 10;

					glFlush();
					//level=3;



					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}

					//*p=2;
					end2 = 1;
				}


				else if (win2 == -1)
				{


					printf("\nWRONG!");

					glFlush();
					glColor3f(1.0, 0.0, 0.0);
					wrong2();
					drawstring(300.0, 400.0, 0.0, "WRONG!!!");
					glFlush();
					//level=3;



					//int j;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}

					end2 = 1;
				}////end of else
			}//end of if(n==count)
		}//end of level 2


		if ((x >= 510 && x <= 555) && (y >= 290 && y <= 320) && (level == 2) && (end2 == 1))
		{
			level = 3;
			int count3 = 0;

			glClear(GL_COLOR_BUFFER_BIT);
			drawgrid3();
			if (*w1 == 1)
				rite1();
			else  if (*w1 == -1)
				wrong1();
			if (*w2 == 1)
				rite2();
			else if (*w2 == -1)
				wrong2();
			int done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;

			firstcall = 1;
			r1 = check(x, y, level, count3);//to reset n2 to 0
			

		}

		if (level == 3)//safety loop******************************************
		{

			count3 = 4;
			q = flag;
			firstcall = 0;

			//drawgrid2();
			int done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;

			r3 = check(x, y, level, count3);
			if (r3 == 1 && n3<count3)
			{
				drawline(x, y);
				n3++;
				//printf("..%d",n3);
			}
			else
			{
				printf("error");
			}



			if (n3 == count3 && end3 == 0)//safety loop******************************
			{
				q = flag;
				for (i = 0; i<25; i++)//for begins......
				{
					printf("%d", flag[i]);
					if (result3[i] == flag[i])
					{
						win3 = 1;//fin=0;
						//printf("win3=%d",win3);
					}
					else
					{
						win3 = -1;

						break;
					}
				}//for ends........................
				if (win3 == 1)
				{
					/*if(win1)
					rite1();
					else
					wrong1();
					if(win2)
					rite2();
					else
					wrong2();*/

					printf("\nRIGHT!");
					glFlush();
					glColor3f(0.0, 1.0, 0.0);
					rite3();
					drawstring(300.0, 400.0, 0.0, "RIGHT!!!");
					counts = counts + 10;

					glFlush();
					end3 = 1;
					//int j;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}
					//*p=2;
				}


				else if (win3 == -1 && *e3 == 0)
				{
					/*if(win1)
					rite1();
					else
					wrong1();
					if(win2)
					rite2();
					else
					wrong2();*/

					printf("\nWRONG!");

					glFlush();
					glColor3f(1.0, 0.0, 0.0);
					wrong3();
					drawstring(300.0, 400.0, 0.0, "WRONG!!!");
					glFlush();
					end3 = 1;

					//int j;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}

				}////end of else
			}//end of if(n==count)
		}//end of level 3

		//level44444444444444444444444444444444444***********************

		if ((x >= 510 && x <= 555) && (y >= 290 && y <= 320) && (level == 3) && (end3 == 1))
		{
			level = 4;
			int count4 = 0;
			int done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;

			glClear(GL_COLOR_BUFFER_BIT);
			drawgrid4();
			if (*w1 == 1)
				rite1();
			else if (*w1 == -1)
				wrong1();
			if (*w2 == 1)
				rite2();
			else if (*w2 == -1)
				wrong2();
			if (*w3 == 1)
				rite3();
			else if (*w3 == -1)
				wrong3();

			firstcall = 1;
			r1 = check(x, y, level, count4);
			
		}

		if (level == 4)//safety loop******************************************
		{

			count4 = 8;
			q = flag;
			firstcall = 0;

			//drawgrid2();

			r4 = check(x, y, level, count4);
			if (r4 == 1 && n4<count4)
			{
				drawline(x, y);
				n4++;
				printf("......%d", n4);
			}
			else
			{
				printf("error");
			}



			if (n4 == count4 && *e4 == 0)//safety loop******************************
			{
				q = flag;
				for (i = 0; i<25; i++)//for begins......
				{
					printf("%d", flag[i]);
					if (result4[i] == flag[i])
						win4 = 1;
					else
					{
						win4 = -1;

						break;
					}
				}//for ends........................
				if (win4 == 1)
				{
					/*if(win1)
					rite1();
					else
					wrong1();
					if(win2)
					rite2();
					else
					wrong2();
					if(win3)
					rite3();
					else
					wrong3();*/
					printf("\nRIGHT!");
					glFlush();
					glColor3f(0.0, 1.0, 0.0);
					rite4();
					drawstring(300.0, 400.0, 0.0, "RIGHT!!!");
					counts = counts + 10;

					glFlush();
					end4 = 1;
					//int ;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}
					//*p=2;
				}


				else if (win4 == -1)
				{
					/* if(win1)
					rite1();
					else
					wrong1();
					if(win2)
					rite2();
					else
					wrong2();
					if(win3)
					rite3();
					else
					wrong3();*/

					printf("\nWRONG!");

					glFlush();
					glColor3f(1.0, 0.0, 0.0);
					wrong4();
					drawstring(300.0, 400.0, 0.0, "WRONG!!!");
					glFlush();
					end4 = 1;
					//	int i;
					for (j = 0; j<25; j++)
					{
						flag[j] = 1;
					}
				}////end of else
			}//end of if(n==count)
		}//end of level 4

		//level55555555555555555555555555555555555555555555555555555555555555

		if ((x >= 510 && x <= 555) && (y >= 290 && y <= 320) && (level == 4) && (end4 == 1))
		{
			level = 5;
			int count5 = 0;
			int done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;

			glClear(GL_COLOR_BUFFER_BIT);
			drawgrid5();
			if (*w1 == 1)
				rite1();
			else if (*w1 == -1)
				wrong1();
			if (*w2 == 1)
				rite2();
			else if (*w2 == -1)
				wrong2();
			if (*w3 == 1)
				rite3();
			else if (*w3 == -1)
				wrong3();
			if (*w4 == 1)
				rite4();
			else if (*w4 == -1)
				wrong4();

			firstcall = 1;
			r1 = check(x, y, level, count5);
			
		}

		if (level == 5)//safety loop******************************************
		{

			count5 = 8;
			q = flag;
			firstcall = 0;

			//drawgrid2();

			r5 = check(x, y, level, count5);
			if (r5 == 1 && n5<count5)
			{
				drawline(x, y);
				n5++;
				printf("......%d", n5);
			}
			else
			{
				printf("error");
			}



			if (n5 >= count5 && end5 == 0)//safety loop******************************
			{
				q = flag;
				for (i = 0; i<25; i++)//for begins......
				{
					printf("%d", flag[i]);
					if (result5[i] == flag[i])
						win5 = 1;
					else
					{
						win5 = -1;

						break;
					}
				}//for ends........................
				if (win5 == 1)
				{
					/*if(win1)
					rite1();
					else
					wrong1();
					if(win2)
					rite2();
					else
					wrong2();
					if(win3)
					rite3();
					else
					wrong3();
					if(win4)
					rite4();
					else
					wrong4();*/
					printf("\nRIGHT!");
					glFlush();
					glColor3f(0.0, 1.0, 0.0);
					rite5();
					drawstring(300.0, 400.0, 0.0, "RIGHT!!!");
					counts = counts + 10;

					glFlush();
					end5 = 1;
					//*p=2;
				}


				else if (win5 == -1)
				{
					/* if(win1)
					rite1();
					else
					wrong1();
					if(win2)
					rite2();
					else
					wrong2();
					if(win3)
					rite3();
					else
					wrong3();
					if(win4)
					rite4();
					else
					wrong4();*/
					printf("\nWRONG!");

					glFlush();
					glColor3f(1.0, 0.0, 0.0);
					wrong5();
					drawstring(300.0, 400.0, 0.0, "WRONG!!!");
					glFlush();
					end5 = 1;
				}////end of else
			}//end of if(n==count)
		}//end of level 5
		glColor3f(1.0, 1.0, 0.0);
		if ((level == 5) && (end5 == 1))
		{
			drawstring(200.0, 80.0, 0.0, "TOTAL SCORE ");
			sprintf_s(buffer, "%d", counts);
			glColor3f(1.0, 0.5, 0.0);
			drawstring(370.0, 80.0, 0.0, buffer);

			//glutBitmapCharacter(GLUT_BITMAP_HELVETICA_18, buffer);

			glFlush();
		}
		glFlush();
}//end of left button


	else if (btn == GLUT_RIGHT_BUTTON && state == GLUT_DOWN)
	{
		exit(0);
	}
}


//***************************************************************************end of mouse*********************************

int check(int x, int y, int m, int count)
//*************************CHECK********************************
{


	printf(".................................jjkjkl........................%d\n", n2);
	//to prevent arbitrary clicks........................................................
	//printf("hvjhegkgwjkvw");
	//if(*p==2)
	//*h=0;

	if (level == 2 && firstcall == 1)
	{
		n2 = 0;
		done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;
	}
	if (*p == 3 && firstcall == 1)
	{
		n2 = 0;
		done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;
	}
	if (level == 4 && firstcall == 1)
	{
		n2 = 0;
	    done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;
	}
	if (level == 5 && firstcall == 1)
	{
		n2 = 0;
		done1 = 0, done2 = 0, done3 = 0, done4 = 0, done5 = 0, done6 = 0, done7 = 0, done8 = 0, done9 = 0, done10 = 0, done11 = 0, done12 = 0, done13 = 0, done14 = 0, done15 = 0, done16 = 0, done17 = 0, done18 = 0, done19 = 0, done20 = 0, done21 = 0, done22 = 0, done23 = 0, done24 = 0;
	}
	if (done1 == 0)
		{
			if (y <= 30)//item 1...horizontal
			{
				if (y >= 20)
				{
					if (x >= 105)
					{
						if (x <= 155)
						{
							if ((n2 <= count))
							{//printf("hvjhegkgwjkvw");
								n2++;
								printf("1n2====%d", n2);
								done1 = 1;
								return 1;//drawline(x,y);
							}
						}
					}
				}
			}
		}
	if (done2 ==0)
	{
		if (x <= 215)//item 2
		{
			if (x >= 165)
			{
				if (y <= 30)
				{
					if (y >= 20)
					{
						if ((n2 <= count))
						{
							n2++;

							printf("2n2=====%d", n2);
							done2 = 1;
							return 1;//drawline(x,y);(n)++;
							
						}
					}
				}
			}
		}
	}
	if (done3 == 0)
	{
		if (x <= 275)//item 3
		{
			if (x >= 225)
			{
				if (y >= 20)
				{
					if (y <= 30)
					{
						if ((n2 <= count))
						{
							n2++;
							printf("3n2=====%d", n2);
							done3 = 1;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done4 == 0)
	{
		if (x <= 105)//item 4....30 to 80>>y
		{
			if (x >= 95)
			{
				if (y >= 30)
				{
					if (y <= 80)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("4n2=====%d", n2);
							done4 = 1;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done5 == 0)
	{
		if (x <= 165)//item 5....30 to 80>>y
		{
			if (x >= 155)
			{
				if (y >= 30)
				{
					if (y <= 80)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("5n2=====%d", n2);

							//						(n2)++;
							done5 = 1;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done6 == 0)
	{
		if (x <= 225)//item 6....30 to 80>>y
		{
			if (x >= 215)
			{
				if (y >= 30)
				{
					if (y <= 80)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("6n2=====%d", n2);
							done6 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done7 == 0)
	{
		if (x <= 285)//item 7....30 to 80>>y
		{
			if (x >= 275)
			{
				if (y >= 30)
				{
					if (y <= 80)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("7n2=====%d", n2);
							done7 = 1;
							//						(n2)++;
							return 1;
						}
					}
				}
			}
		}
	}
	if (done8 == 0)
	{
		if (y <= 90)//item 8...horiz..
		{
			if (y >= 80)
			{
				if (x >= 105)
				{
					if (x <= 155)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("8n2=====%d", n2);
							done8 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done9 == 0)
	{
		if (x <= 215)//item 9...horiz
		{
			if (x >= 165)
			{
				if (y >= 80)
				{
					if (y <= 90)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("9n2=====%d", n2);
							done9 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done10 == 0)
	{
		if (x <= 275)//item 10
		{
			if (x >= 225)
			{
				if (y >= 80)
				{
					if (y <= 90)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("10n2=====%d", n2);
							done10 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;

						}
					}
				}
			}
		}
	}
	if (done11 == 0)
	{
		if (y >= 90)//item 11....90 to 140>>y
		{
			if (y <= 140)
			{
				if (x >= 95 || x <= 105)
				{
					if (x <= 105)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("11n2=====%d", n2);
							//						(n2)++;
							done11 = 1;
							return 1;//drawline(x,y);(n)++;
							
						}
					}
				}
			}
		}
	}
	if (done12 == 0)
	{
		if (x <= 165)//item 12....90 to 140>>y
		{
			if (x >= 155)
			{
				if (y >= 90)
				{
					if (y <= 140)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("12n2=====%d", n2);
							done12 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done13 == 0)
	{
		if (x <= 225)//item 13...90 to 140>>y
		{
			if (x >= 215)
			{
				if (y >= 90)
				{
					if (y <= 140)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("13n2=====%d", n2);
							done13 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}

	if (done14 == 0)
	{
		if (x <= 285)//item 14....90 to 140>>y
		{
			if (x >= 275)
			{
				if (y >= 90)
				{
					if (y <= 140)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("14n2=====%d", n2);
							done14 = 1;
							//						(n2)++;
							//	printf("3n2=====%d", n2);
							return 1;//drawline(x,y);(n)++;
							//done14 = 1;
						}
					}
				}
			}
		}
	}
	if (done15 == 0)
	{
		if (y <= 150)//item 15...horiz.y>>140 to 150
		{
			if (y >= 140)
			{
				if (x >= 105)
				{
					if (x <= 155)
					{
						if ((n2 <= count))
						{
							(n2)++;
							done15 = 1;
							printf("15n2=====%d", n2);

							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done16 == 0)
	{
		if (x <= 215)//item 16...horiz
		{
			if (x >= 165)
			{
				if (y >= 140)
				{
					if (y <= 150)
					{
						if ((n2 <= count))
						{
							(n2)++;
							//done16 = 1;
							printf("16n2=====%d", n2);
							done16 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done17 == 0)
	{
		if (x <= 275)//item 17...horiz
		{
			if (x >= 225)
			{
				if (y >= 140)
				{
					if (y <= 150)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("17n2=====%d", n2);
							done17 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done18 == 0)
	{
		if (x >= 95)  //item 18....150 to 200>>y
		{
			if (x <= 105)
			{
				if (y >= 150)
				{
					if (y <= 200)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("18n2=====%d", n2);
							done18 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done19 == 0)
	{
		if (x <= 165)//item 19....150 to 200>>y
		{
			if (x >= 155)
			{
				if (y >= 150)
				{
					if (y <= 200)
					{

						if ((n2 <= count))
						{
							(n2)++;

							printf("19n2=====%d", n2);
							done19 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done20 == 0)
	{

		if (x <= 225)//item 20...150 to 200>>y
		{
			if (x >= 215)
			{
				if (y >= 150)
				{
					if (y <= 200)
					{

						if ((n2 <= count))
						{
							(n2)++;

							printf("20n2=====%d", n2);
							done20 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done21 == 0)
	{
		if (x <= 285)//item 21....150 to 200>>y
		{
			if (x >= 275)
			{
				if (y >= 150)
				{
					if (y <= 200)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("21n2=====%d", n2);
							done21 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done22 == 0)
	{
		if (y <= 210)//item 22...horiz.y>>190 to 210
		{
			if (y >= 190)
			{
				if (x >= 105)
				{
					if (x <= 155)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("22n2=====%d", n2);
							done22 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (done23 ==0)
	{
		if (x <= 215)//item 23...horiz..y>>190to 210
		{
			if (x >= 165)
			{
				if (y >= 190)
				{
					if (y <= 210)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("23n2=====%d", n2);
							//						(n2)++;
							done23 = 1;
							return 1;//drawline(x,y);(n)++;
							
						}
					}
				}
			}
		}
	}
	if (done24 == 0)
	{
		if (x <= 275)//item 24...horiz.. y>>190 to 210
		{
			if (x >= 225)
			{
				if (y >= 200)
				{
					if (y <= 210)
					{
						if ((n2 <= count))
						{
							(n2)++;

							printf("24n2=====%d", n2);
							done24 = 1;
							//						(n2)++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	}
	if (y >= 380)
	{
		if (y <= 410)
		{
			if (x <= 550)
			{
				if (x >=510)
				{
					exit(0);
				}
			}
		}
	}
	if (done111 == 0)
	{
		if (x <= 420)//item 5....30 to 80>>y
		{
			if (x >=200)
			{
				if (y >= 330)
				{
					if (y <= 380)
					{
						//if (*p==1)
						drawgrid1();
						done111++;
							return 1;//drawline(x,y);(n)++;
						}
					}
				}
			}
		}
	
	return -1;
}


void myDisplay(void)
{
	glClear(GL_COLOR_BUFFER_BIT);
	glClearColor(0.0,0.0, 0.0, 0.0);
	glColor3f(1.0, 1.0, 1.0);
	drawstring(260.0, 420.0, 0.0, "LOGIC GRID");
	glColor3f(1.0, 1.0, 0.0);
	drawstring(140.0, 300.0, 0.0, "APURVA G KATTI");
	drawstring(360.0, 300.0, 0.0, "1MV12CS011");
	drawstring(140.0, 250.0, 0.0, "NEHA S");
	drawstring(360.0, 250.0, 0.0, "1MV12CS060");
	//drawstring(255.0, 420.0, 0.0, "LOGIC GRID");
	glBegin(GL_POLYGON);
	glColor3f(0.0, 1.0, 1.0);
	glVertex2f(200, 100);
	glVertex2f(420, 100);
	glVertex2f(420, 150);
	glVertex2f(200, 150);
	glEnd();
	glColor3f(0.0, 0.0, 0.0);
	drawstring(252.0, 120.0, 0.0, "START GAME");

	glFlush();

	//glFlush();

	/*if (*p == 1)
		drawgrid1();
		*/
	/*	else if(*p==2)
	{printf("hbchjd");
	glClear(GL_COLOR_BUFFER_BIT);
	drawgrid2();
	return;
	*/



}
void main()
{


	int i;
	for (i = 0; i<25; i++)
	{
		flag[i] = 1;
	}
	//glClear(GL_COLOR_BUFFER_BIT);
	glutInitDisplayMode(GLUT_SINGLE | GLUT_RGB);
	glutInitWindowSize(640, 480);
	glutInitWindowPosition(100, 150);
	glutCreateWindow("logicgrid");
	glutDisplayFunc(myDisplay);
	glutMouseFunc(mymouse);
	//glutDisplayFunc(myDisplay);
	myInit();
	glutMainLoop();//cause the execution of the pgm to begin an event processing loop
}

