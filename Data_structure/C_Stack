// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>

// #define MAX_STACK_SIZE 100
// #define MAZE_SIZE 6

// typedef struct{
//   short r;
//   short c;
// }element;

// element here = {1,0}, entry = {1,0};
// char maze[MAZE_SIZE][MAZE_SIZE]={
// {'1','1','1','1','1','1'},
// {'e','0','1','0','0','1'},
// {'1','0','0','0','1','1'},
// {'1','0','1','0','1','1'},
// {'1','0','1','0','0','x'},
// {'1','1','1','1','1','1'}
// };

// typedef struct{
//   element data[MAX_STACK_SIZE];
//   int top;
// }StackType;

// void InitStack(StackType* s){
//   s->top = -1;
// }

// int IsEmpty(StackType *s){
//   return (s->top == -1);
// }

// int IsFull(StackType *s){
//   return (s->top == (MAX_STACK_SIZE)-1);
// }

// void Push(StackType *s, element item){
//   if(IsFull(s)){
//     printf("스택 포화 에러\n");
//     return;
//   }
//   else s->data[++(s->top)] = item;
// }

// element Pop(StackType *s){
//   if(IsEmpty(s)){
//     printf("스택 공백 에러\n");
//     exit(1);
//   }
//   else return s->data[s->top--];
// }

// element Peek(StackType *s){
//   if(IsEmpty(s)){
//     printf("스택 공백 에러\n");
//     exit(1);
//   }
//   else return s->data[s->top];
// }

// void PushLocate(StackType *s,int row,int column){
//   if(maze[row][column] == '0' || maze[row][column] == 'e' || maze[row][column] == 'x'){
//     element tmp;
//     tmp.r = row;
//     tmp.c = column;
//     Push(s,tmp);
//   }
// }

// void PrintMaze(void){
//   for(int i = 0;i<MAZE_SIZE;i++){
//     for(int j = 0;j<MAZE_SIZE;j++){
//       printf("%c ",maze[i][j]);
//     }
//     printf("\n");
//   }
// }

// void MoveLocate(StackType *s,int row,int column){
//   maze[row][column]='*';
//   element des = Pop(s);
//   here.r = des.r;
//   here.c = des.c;
//   maze[here.r][here.c] = 'm';
// }

// void EscapeMaze(StackType *s){
//   PrintMaze();
//   while(here.c != 5){
//     if((here.r == entry.r) && (here.c == entry.c)){
//       PushLocate(s, here.r, here.c+1);
//     }
//     else{
//       PushLocate(s,here.r+1,here.c);
//       PushLocate(s,here.r-1,here.c);
//       PushLocate(s,here.r,here.c+1);
//       PushLocate(s,here.r,here.c-1);
//     }
//     MoveLocate(s,here.r,here.c);
//     printf("\n\n");
//     PrintMaze();
//   }
//   MoveLocate(s, here.r, here.c);
//   printf("Success to escape from the maze");
// }

// int main(void) {
//   StackType s;
//   InitStack(&s);
//   EscapeMaze(&s);
//   return 0;
// }
// // 한가지 변수
// // typedef int element;
// // element stack[MAX_STACK_SIZE];
// // int top = -1;

// // // 공백 상태 검출 함수
// // int is_empty(){
// //   return (top==-1);
// // }

// // // 포화 상태 검출 함수
// // int is_full(){
// //   return (top == (MAX_STACK_SIZE-1));
// // }

// // // 삽입 함수
// // void push(element item){
// //   if(is_full()){
// //     printf("스택 포화 에러\n");
// //     return;
// //   }
// //   else stack[++top] = item;
// // }

// // // 삭제 함수
// // element pop(){
// //   if(is_empty()){
// //     printf("스택 공백 에러\n");
// //     exit(1);
// //   }
// //   else return stack[top--];
// // }

// // // 피크 함수
// // element peek(){
// //   if(is_empty()){
// //     printf("스택 공백 에러\n");
// //     exit(1);
// //   }
// //   else return stack[top];
// // }

// // #define MAX_STACK_SIZE 100
// // #define MAX_STRING 100

// // typedef struct element{
// //   int student_no;
// //   char name[MAX_STRING];
// //   char address[MAX_STRING];
// // }element;

// // 다양한 변수
// // element stack[MAX_STACK_SIZE];
// // int top = -1;

// // // 공백상태 검출 함수
// // int is_empty(void){
// //   return (top == -1);
// // }

// // // 포화상태 검출 함수
// // int is_full(void){
// //   return (top == (MAX_STACK_SIZE-1));
// // }

// // // 삽입 함수
// // void push(element a){
// //   if(is_full()){
// //     printf("스택 포화 에러\n");
// //     return;
// //   }
// //   stack[++top] = a;
// // }

// // // 삭제 함수
// // element pop(void){
// //   if(is_empty()){
// //     printf("스택 공백 에러\n");
// //     exit(1);
// //   }
// //   return stack[top--];
// // }

// // // 피크함수
// // element peek(void){
// //   if(is_empty()){
// //     printf("스택 공백 에러");
// //     exit(1);
// //   }
// //   return stack[top];
// // }

// // 스택 동적할당
// // typedef int element;
// // typedef struct{
// //   element *data;
// //   int top;
// //   int capacity;
// // }stackType;

// // // stack reset function
// // void init_stack(stackType *s){
// //   s->top = -1;
// //   s->capacity = 1;
// //   s->data = (element *)malloc(s->capacity*sizeof(element));
// // }

// // // 공백 상태 검출 함수
// // int is_empty(stackType *s){
// //   return (s->top==-1);
// // }

// // // 포화 상태 검출 함수
// // int is_full(stackType *s){
// //   return (s->top == s->capacity-1);
// // }

// // // 삽입함수
// // void push(stackType *s,element item){
// //   if(is_full(s)){
// //     s->capacity *=2;
// //     s->data = (element *)realloc(s->data,s->capacity*sizeof(element));
// //   }
// //   else s->data[++s->top]= item;
// // }

// // // 제거함수
// // element pop(stackType *s){
// //   if(is_empty(s)){
// //     printf("스택 포화 에러");
// //     exit(1);
// //   }
// //   else return s->data[s->top--];
// // }

// // element peek(stackType *s){
// //   if(is_empty(s)){
// //     printf("스택 포화 에러");
// //     exit(1);
// //   }
// //   else return s->data[s->top];
// // }

// // 괄호 검사 함수
// // typedef struct{
// //   element data[MAX_STACK_SIZE];
// //   int top;
// // }StackType;

// // void init_stack(StackType* s){
// //   s->top = -1;
// // }

// // int is_full(StackType *s){
// //   return (s->top == (MAX_STACK_SIZE-1));
// // }

// // int is_empty(StackType *s){
// //   return (s->top == -1);
// // }

// // void push(StackType *s,element item){
// //   if(is_full(s)){
// //     printf("스택 포화 에러");
// //     return;
// //   }
// //   else
// //     s->data[++(s->top)] = item;
// // }

// // element pop(StackType *s){
// //   if(is_empty(s)){
// //     printf("스택 공백 에러");
// //     exit(1);
// //   }
// //   else return s->data[(s->top)--];
// // }

// // element peek(StackType *s){
// //   if(is_empty(s)){
// //     printf("스택 공백 에러");
// //     exit(1);
// //   }
// //   else return s->data[s->top];
// // }

// // int check_matching(char* in){
// //   StackType s;
// //   int i,n=strlen(in);
// //   init_stack(&s);

// //   printf("%d\n",s.top);

// //   for(i=0;i<n;i++){
// //     switch(in[i]){
// //       case '(': case '[': case '{':
// //         push(&s,in[i]);
// //         printf("%d\n",s.top);
// //         break;
// //       case ')': case ']': case '}':
// //         if(is_empty(&s)){
// //           printf("스택 공백 에러");
// //           return 0;
// //         }
// //         else{
// //           element open_ch = pop(&s);
// //           if((open_ch == '(' && in[i] == ')')||(open_ch == '[' && in[i] ==
// //           ']')||(open_ch == '{' && in[i] == '}'))
// //             break;
// //           return 0;
// //         }
// //     }
// //   }
// //   if(!is_empty(&s)){
// //     printf("%d\n",s.top);
// //     return 0;
// //   }
// //   return 1;
// // }

// // prefix_natation
// // typedef int operand;
// // typedef char operator;

// // typedef struct {
// //   operand data[MAX_STACK_SIZE];
// //   int top;
// // } StackType;

// // void init_stack(StackType *s) { s->top = -1; }

// // int is_empty(StackType *s) { return (s->top == -1); }

// // int is_full(StackType *s) { return (s->top == (MAX_STACK_SIZE - 1)); }

// // void push(StackType *s, int item) {
// //   if (is_full(s)) {
// //     printf("스택 포화 에러");
// //     return;
// //   } else
// //     s->data[++(s->top)] = item;
// // }

// // int pop(StackType *s) {
// //   if (is_empty(s)) {
// //     printf("스택 공백 에러");
// //     exit(1);
// //   } else
// //     return s->data[(s->top)--];
// // }

// // int peek(StackType *s) {
// //   if (is_empty(s)) {
// //     printf("스택 공백 에러");
// //     exit(1);
// //   } else
// //     return s->data[s->top];
// // }

// // int prefix_notation(char in[]) {
// //   StackType s;
// //   int len, op1, op2;
// //   char ch;
// //   len = strlen(in);
// //   init_stack(&s);

// //   for (int i = 0; i < len; i++) {
// //     if (in[i] == '+' || in[i] == '-' || in[i] == '*' || in[i] == '/') {
// //       if (s.top < 1) {
// //         printf("prefix notation error");
// //         exit(1);
// //       }
// //       ch = in[i];
// //       op2 = pop(&s);
// //       op1 = pop(&s);
// //       switch (ch) {
// //       case '+':
// //         push(&s, op1 + op2);
// //         //printf("%d\n", op1 + op2);
// //         break;
// //       case '-':
// //         push(&s, op1 - op2);
// //         //printf("%d\n", op1 - op2);
// //         break;
// //       case '*':
// //         push(&s, op1 * op2);
// //         //printf("%d\n", op1 * op2);
// //         break;
// //       case '/':
// //         push(&s, op1 / op2);
// //         //printf("%d\n", op1 / op2);
// //         break;
// //       }
// //     } else {
// //       operator value = in[i] - '0';
// //       //printf("value: %d\n",value);
// //       push(&s, value);
// //     }
// //   }
// //   return pop(&s);
// // }


// // // prefix_natation
// // typedef int operand;
// // typedef char operator;
// // typedef struct {
// //   operand data[MAX_STACK_SIZE];
// //   int top;
// // } StackType1;
// // void init_stack_(StackType1 *s) { s->top = -1; }
// // int is_empty_(StackType1 *s) { return (s->top == -1); }
// // int is_full_(StackType1 *s) { return (s->top == (MAX_STACK_SIZE - 1)); }
// // void push_(StackType1 *s, int item) {
// //   if (is_full_(s)) {
// //     printf("스택 포화 에러");
// //     return;
// //   } else
// //     s->data[++(s->top)] = item;
// // }
// // int pop_(StackType1 *s) {
// //   if (is_empty_(s)) {
// //     printf("스택 공백 에러");
// //     exit(1);
// //   } else
// //     return s->data[(s->top)--];
// // }
// // int peek_(StackType1 *s) {
// //   if (is_empty_(s)) {
// //     printf("스택 공백 에러");
// //     exit(1);
// //   } else
// //     return s->data[s->top];
// // }

// // // infix_to_prefix
// // typedef char element;
// // typedef struct {
// //   element data[MAX_STACK_SIZE];
// //   int top;
// // } StackType;

// // void init_stack(StackType *s) { s->top = -1; }

// // int is_full(StackType *s) { return (s->top == (MAX_STACK_SIZE - 1)); }

// // int is_empty(StackType *s) { return (s->top == -1); }

// // void push(StackType *s, element item) {
// //   if (is_full(s)) {
// //     printf("스택 포화 에러");
// //     return;
// //   } else
// //     s->data[++(s->top)] = item;
// // }

// // element pop(StackType *s) {
// //   if (is_empty(s)) {
// //     printf("스택 공백 에러");
// //     exit(1);
// //   } else
// //     return s->data[(s->top)--];
// // }

// // element peek(StackType *s) {
// //   if (is_empty(s)) {
// //     printf("스택 공백 에러");
// //     exit(1);
// //   } else
// //     return s->data[s->top];
// // }

// // int priority(char op) {
// //   switch (op) {
// //   case '(':
// //   case ')':
// //     return 0;
// //     break;
// //   case '*':
// //   case '/':
// //     return 1;
// //     break;
// //   case '+':
// //   case '-':
// //     return 2;
// //     break;
// //   }
// //   return 3;
// // }

// // void infix_to_prefix(char in[], char *str) {
// //   int len, top_op = 3, num = 0;
// //   char ch, op;
// //   StackType s;

// //   init_stack(&s);
// //   len = strlen(in);

// //   for (int i = 0; i < len; i++) {
// //     ch = in[i];
// //     switch (ch) {
// //     case '+':
// //     case '-':
// //     case '*':
// //     case '/':
// //       if (priority(ch) < top_op) {
// //         push(&s, ch);
// //         top_op = priority(ch);
// //       } else if (top_op != 0) {
// //         str[num++] = peek(&s);
// //         printf("%c", pop(&s));
// //         push(&s, ch);
// //         top_op = priority(ch);
// //       } else {
// //         push(&s, ch);
// //         top_op = priority(ch);
// //       }
// //       break;
// //     case '(':
// //       push(&s, ch);
// //       top_op = priority(ch);
// //       break;
// //     case ')':
// //       op = pop(&s);
// //       while (op != '(') {
// //         str[num++] = op;
// //         printf("%c", op);
// //         op = pop(&s);
// //       }
// //       top_op = priority(peek(&s));
// //       break;
// //     default:
// //       str[num++] = ch;
// //       printf("%c", ch);
// //       break;
// //     }
// //   }
// //   while (!is_empty(&s)) {
// //     str[num++] = peek(&s);
// //     printf("%c", pop(&s));
// //   }
// // }

// // int prefix_notation(char in[]) {
// //   StackType1 s;
// //   int len, op1, op2;
// //   char ch;
// //   len = strlen(in);
// //   init_stack_(&s);
// //   for (int i = 0; i < len; i++) {
// //     if (in[i] == '+' || in[i] == '-' || in[i] == '*' || in[i] == '/') {
// //       if (s.top < 1) {
// //         printf("prefix notation error");
// //         exit(1);
// //       }
// //       ch = in[i];
// //       op2 = pop_(&s);
// //       op1 = pop_(&s);
// //       switch (ch) {
// //       case '+':
// //         push_(&s, op1 + op2);
// //         // printf("%d\n", op1 + op2);
// //         break;
// //       case '-':
// //         push_(&s, op1 - op2);
// //         // printf("%d\n", op1 - op2);
// //         break;
// //       case '*':
// //         push_(&s, op1 * op2);
// //         // printf("%d\n", op1 * op2);
// //         break;
// //       case '/':
// //         push_(&s, op1 / op2);
// //         // printf("%d\n", op1 / op2);
// //         break;
// //       }
// //     } else if (in[i] == '0') {
// //       s.data[s.top] *= 10;
// //     } else {
// //       int value = in[i] - '0';
// //       // printf("value: %d\n",value);
// //       push_(&s, value);
// //     }
// //   }
// //   return pop_(&s);
// // }
