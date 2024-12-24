// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>
// #include <math.h>

// #define MAX(a,b) ((a)>(b)?(a):(b))
// #define Max_degree 101
// #define MAXTERMS 100
// #define ROWS 3
// #define COLUMNS 3
// #define SIZE 10

// int matrix1[ROWS][COLUMNS] = {{2,3,0},{8,9,1},{7,0,5}};

// typedef struct{
//   int row; 
//   int col;
//   int value;
// }element;

// typedef struct sparseMatrix{
//   element data[MAXTERMS];
//   int rows;
//   int cols;
//   int terms;
// } sparseMatrix;

// typedef struct{
//   double x;
//   double y;
// }Point;

// typedef struct{
// int degree;
// int coef[Max_degree];
// }polynomial1;

// typedef struct{
// int coef;
// int expon;
// }polynomial2;
// polynomial2 terms[Max_degree] = {{8,3}, {7,1}, {1,0}, {10,3}, {3,2}, {1,0}};

// typedef struct student{
//   char name[10];
//   int age;
//   double gpa;
// }student;

// double get_distance(Point,Point);
// polynomial1 polynomial_add(polynomial1,polynomial1);
// void polynomial_print(polynomial1);
// int poly_add();
// void poly_print();
// void matrix1_transpose();
// void matrix_print();
// sparseMatrix matrix2_transpose();
// void matrix_print2();

// int main(void){
//   student* s;

//   s=(student*)malloc(sizeof(student));
//   if(s==NULL){
//     printf("메모리가 부족해서 할당할 수 없습니다.");
//     exit(1);
//   }

//   strcpy(s->name,"park");
//   s->age = 20;

//   free(s);
//   return 0;
// } 

// polynomial1 polynomial_add(polynomial1 a,polynomial1 b){
//   polynomial1 c;
//   c.degree = MAX(a.degree,b.degree);
//   int apos=0, bpos=0, cpos=0;
//   int degree_a = a.degree;
//   int degree_b = b.degree;

//   while(apos<=a.degree && bpos<=b.degree){
//     if(degree_a>degree_b){
//       c.coef[cpos++] = a.coef[apos++];
//       degree_a--;
//     }
//     else if(degree_a==degree_b){
//       c.coef[cpos++] = a.coef[apos++] + b.coef[bpos++];
//       degree_a--; degree_b--;
//     }
//     else{
//       c.coef[cpos++] = b.coef[bpos++];
//       degree_b--;
//     }
//   }  
//   return c;
// }

// void polynomial_print(polynomial1 A){
//   int degree_A = A.degree;
//   for(int i = 0;i<=A.degree;i++){
//     if(A.coef[i] == 0){
//       degree_A--;
//       continue;
//     }
//     printf("%dx^%d",A.coef[i],degree_A--);
//     if(A.degree != i)
//       printf(" + ");
//   }
// }

// double get_distance(Point p1,Point p2){
//   double result;
//   result = sqrt(pow((p1.x-p2.x),2)+pow((p1.y-p2.y),2));
//   return result;
// }

// int poly_add(int As, int Ae, int Bs, int Be){
//   int Apos = As, Bpos = Bs, Cpos = Be+1;
//   while(Apos <= Ae && Bpos <= Be){
//     if(Apos>Ae)
//       Apos = Ae;
//     if(Bpos>Be)
//       Bpos=Be;
//     if(terms[Apos].expon > terms[Bpos].expon){
//       terms[Cpos].expon = terms[Apos].expon;
//       terms[Cpos].coef = terms[Apos].coef;
//       Cpos++; Apos++;
//     }
//     else if(terms[Apos].expon == terms[Bpos].expon){
//       terms[Cpos].expon = terms[Apos].expon;
//       terms[Cpos].coef = terms[Apos].coef + terms[Bpos].coef;
//       Apos++; Bpos++; Cpos++;
//     }
//     else{
//       terms[Cpos].expon = terms[Bpos].expon;
//       terms[Cpos].coef = terms[Bpos].coef;
//       Cpos++; Bpos++;
//     }
//   }
//   return Cpos;
// }

// void poly_print(int Cs, int Ce){
//   for(int i=Cs;i<=Ce;i++){
//     if(i==Ce)
//       printf("%d",terms[i].coef);
//     else
//       printf("%dx^%d",terms[i].coef,terms[i].expon);
//     if(i != Ce)
//       printf(" + ");
//   }
// }

// void matrix1_transpose(int A[ROWS][COLUMNS]){
//   int temp;
//   for(int i = 0;i<ROWS;i++){
//     for(int j = 0;j<i;j++){
//       temp = A[i][j];
//       A[i][j] = A[j][i];
//       A[j][i] = temp;
//     }
//   }
// }

// void matrix_print(int A[ROWS][COLUMNS]){
//   for(int i = 0;i<ROWS;i++){
//     for(int j = 0;j<COLUMNS;j++){
//       printf("%d ",A[i][j]);
//     if(j==COLUMNS-1)
//       printf("\n");
//     }
//   }
// }

// sparseMatrix matrix2_transpose(sparseMatrix A){
//   sparseMatrix B;
//   int bindex;
//   B.rows = A.rows;
//   B.cols = A.cols;
//   B.terms = A.terms;
  
//   if(A.terms>0){
//     bindex = 0;
//     for(int a = 0;a<A.cols;a++){
//       for(int i=0;i<A.terms;i++){
//         if(A.data[i].col == a){
//           B.data[bindex].col = A.data[i].row;
//           B.data[bindex].row = A.data[i].col;
//           B.data[bindex].value = A.data[i].value;
//           bindex++;
//         }
//       }
//     }
//   }
//   return B;
// }

// void matrix_print2(sparseMatrix A){
//   for(int i = 0;i<A.terms;i++)
//     printf("(%d %d %d)\n",A.data[i].row,A.data[i].col,A.data[i].value);
// }
