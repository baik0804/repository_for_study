#include <stdio.h>
#include <stdlib.h> // dynamic allocate header
#include <time.h>
#define MAX_QUEUE_SIZE 10

typedef struct {
  int id;
  int arrivedTime;
  int serviceTime;
} element;

typedef struct {
  element data[MAX_QUEUE_SIZE];
  int front;
  int rear;
} QueueType;

void error(char *message) {
  fprintf(stderr, "%s", message);
  exit(1);
}

void initQueue(QueueType *q) {
  q->front = 0;
  q->rear = 0;
}

int isEmpty(QueueType *q) { return (q->rear == q->front); }

int isFull(QueueType *q) {
  return (q->front == (q->rear + 1) % MAX_QUEUE_SIZE);
}

void enqueue(QueueType *q, element item) {
  if (isFull(q))
    error("스택 포화 에러");
  q->rear = (q->rear + 1) % MAX_QUEUE_SIZE;
  q->data[q->rear] = item;
}

element dequeue(QueueType *q) {
  if (isEmpty(q))
    error("스택 공백 에러");
  q->front = (q->front + 1) % MAX_QUEUE_SIZE;
  return q->data[q->front];
}

element peek(QueueType *q) {
  if (isEmpty(q))
    error("스택 공백 에러");
  return q->data[(q->front + 1) % MAX_QUEUE_SIZE];
}

int main(void) {
  QueueType queue;
  int minutes = 60;
  int g_serviceTime1 = 0;
  int g_serviceTime2 = 0;
  int g_serviceCustomer1;
  int g_serviceCustomer2;
  int g_totalWaitingTime = 0;
  int g_totalCustomer = 0;
  element customer;

  initQueue(&queue);

  srand(time(NULL));
  for (int clock = 0; clock < minutes; clock++) {
    printf("Current time: %d\n", clock);
    if ((rand() % 11 < 3)) {
      customer.id = ++g_totalCustomer;
      customer.arrivedTime = clock;
      customer.serviceTime = rand() % 4 + 1;
      enqueue(&queue, customer);
      printf("Customer %d enter at %d. Turnaround: %d\n", customer.id, clock,
             customer.serviceTime);
    }
    if (g_serviceTime1 > 0) {
      printf("Customer %d is dealing with business\n", g_serviceCustomer1);
      g_serviceTime1--;
    } else {
      if (!isEmpty(&queue) && g_serviceTime1 == 0) {
        element currentCustomer1 = dequeue(&queue);
        g_serviceCustomer1 = currentCustomer1.id;
        printf("Customer %d start to deal with business. Waitig time: %d\n",
               currentCustomer1.id, clock - currentCustomer1.arrivedTime);
        g_totalWaitingTime += clock - currentCustomer1.arrivedTime;
        g_serviceTime1 = currentCustomer1.serviceTime;
      }
    }
    if (g_serviceTime2 > 0) {
      printf("Customer %d is dealing with business\n", g_serviceCustomer2);
      g_serviceTime2--;
    } else {
      if (!isEmpty(&queue) && g_serviceTime2 == 0) {
        element currentCustomer2 = dequeue(&queue);
        g_serviceCustomer2 = currentCustomer2.id;
        printf("Customer %d start to deal with business. Waitig time: %d\n",
               currentCustomer2.id, clock - currentCustomer2.arrivedTime);
        g_totalWaitingTime += clock - currentCustomer2.arrivedTime;
        g_serviceTime2 = currentCustomer2.serviceTime;
      }
    }
  }
  printf("Total waiting time: %d\n", g_totalWaitingTime);
  return 0;
}

// Deque
// typedef int element;
// typedef struct{
//   element data[MAX_QUEUE_SIZE];
//   int rear, front;
// }DequeType;

// //error function
// void error(char *message){
//   fprintf(stderr,"%s",message);
//   exit(1);
// }

// void initDeque(DequeType *q){
//   q->front = 0;
//   q->rear = 0;
// }

// int isEmpty(DequeType *q){
//   return (q->rear == q->front);
// }

// int isFull(DequeType *q){
//   return (q->front == (q->rear+1)%MAX_QUEUE_SIZE);
// }

// void dequePrint(DequeType *q){
//   printf("DEQUE(front = %d rear = %d) ",q->front,q->rear);
//   if(!isEmpty(q)){
//     int i = q->front;
//     do{
//       i = (i+1)%MAX_QUEUE_SIZE;
//       printf("%d | ",q->data[i]);
//       if(i==q->rear)
//         break;
//     }while(i != q->front);
//   }
//   printf("\n");
// }

// void addRear(DequeType *q, element item){
//   if(isFull(q)){
//     error("큐 포화 에러");
//   }
//   q->rear = (q->rear+1)%MAX_QUEUE_SIZE;
//   q->data[q->rear] = item;
// }

// element deleteRear(DequeType *q){
//   if(isEmpty(q)){
//     error("큐 공백 에러");
//   }
//   int prevrear = q->rear;
//   q->rear = (q->rear + MAX_QUEUE_SIZE -1)%MAX_QUEUE_SIZE;
//   return q->data[prevrear];
// }

// element getRear(DequeType *q){
//   if(isEmpty(q)){
//     error("큐 공백 에러");
//   }
//   return q->data[q->rear];
// }

// void addFront(DequeType *q, element item){
//   if(isFull(q)){
//     error("큐 포화 에러");
//   }
//   q->data[q->front]=item;
//   q->front = (q->front -1 + MAX_QUEUE_SIZE) % MAX_QUEUE_SIZE;
// }

// element deleteFront(DequeType *q){
//   if(isEmpty(q)){
//     error("큐 공백 에러");
//   }
//   q->front = (q->front+1)%MAX_QUEUE_SIZE;
//   return q->data[q->front];
// }

// element getFront(DequeType *q){
//   if(isEmpty(q)){
//     error("큐 공백 에러");
//   }
//   return q->data[(q->front+1)%MAX_QUEUE_SIZE];
// }

// int main(void){
//   DequeType queue;

//   initDeque(&queue);
//   for(int i=0; i<3; i++){
//     addFront(&queue,i);
//     dequePrint(&queue);
//   }
//   for(int i=0;i<3;i++){
//     deleteRear(&queue);
//     dequePrint(&queue);
//   }
// }
// Linear queue
// typedef int element;
// typedef struct{  // queue type
//   int front;
//   int rear;
//   element data[MAX_QUEUE_SIZE];
// }QueueType;

// // error funcion
// void error(char *message){
//   fprintf(stderr,"%s\n",message);
//   exit(1);
// }

// // queue reset function
// void init_queue(QueueType* q){
//   q->rear = -1;
//   q->front = -1;
// }

// void QueuePrint(QueueType *q){
//   for(int i=0;i<MAX_QUEUE_SIZE;i++){
//     if(i<=q->front || i>q->rear)
//       printf("  | ");
//     else
//       printf("%d| ",q->data[i]);
//   }
//   printf("\n");
// }

// int is_full(QueueType *q){
//   if(q->rear == MAX_QUEUE_SIZE-1)
//     return 1;
//   else
//     return 0;
// }

// int is_empty(QueueType *q){
//   if(q->front == q->rear)
//     return 1;
//   else
//     return 0;
// }

// void enqueue(QueueType *q, int item){
//   if(is_full(q)){
//     error("queue is full");
//     return;
//   }
//   else
//     q->data[++(q->rear)] = item;
// }

// int dequeue(QueueType *q){
//   if(is_empty(q)){
//     printf("queue is empty");
//     exit(1);
//   }
//   else
//     return q->data[++(q->front)];
// }

// int main(void){
//   int item = 0;
//   QueueType q;

//   init_queue(&q);

//   enqueue(&q, 10); QueuePrint(&q);
//   enqueue(&q, 20); QueuePrint(&q);
//   enqueue(&q, 30); QueuePrint(&q);

//   item = dequeue(&q); QueuePrint(&q);
//   item = dequeue(&q); QueuePrint(&q);
//   item = dequeue(&q); QueuePrint(&q);
//   return 0;
// }

// circular queue
// void error(char *message){
//   fprintf(stderr,"%s\n",message);
//   exit(1);
// }

// void initQueue(QueueType *q){
//   q->front = 0;
//   q->rear = 0;
// }

// int is_empty(QueueType *q){
//   return (q->front == q->rear);
// }

// int is_full(QueueType *q){
//   return (q->front == (q->rear+1)%MAX_QUEUE_SIZE);
// }

// void queuePrint(QueueType *q){
//   printf("QUEUE(front = %d rear = %d) ",q->front,q->rear);
//   if(!is_empty(q)){
//     int i = q->front;
//     do{
//       i = (i + 1)%MAX_QUEUE_SIZE;
//       printf("%d |",q->data[i]);
//       if(i == q->rear)
//         break;
//     }
//     while(i != q->front);
//   }
//   printf("\n");
// }

// void enqueue(QueueType *q, element item){
//   if(is_full(q)){
//     printf("queue is full");
//     return;
//   }
//   else{
//     q->rear = (q->rear+1)%MAX_QUEUE_SIZE;
//     q->data[q->rear] = item;
//   }
// }

// element dequeue(QueueType *q){
//   if(is_empty(q)){
//     printf("queue is empty");
//     exit(1);
//   }
//   else{
//     q->front = (q->front+1) % MAX_QUEUE_SIZE;
//     return q->data[q->front];
//   }
// }

// element peek(QueueType *q){
//   if(is_empty(q)){
//     printf("queue is empty");
//     exit(1);
//   }
//   else
//     return q->data[(q->front+1)%MAX_QUEUE_SIZE];
// }

// int main(void){
//   QueueType queue;
//   int element;

//   initQueue(&queue);
//   printf("--데이터 추가 단계--\n");
//   while(!is_full(&queue)){
//     printf("정수를 입력하시오: ");
//     scanf("%d",&element);
//     enqueue(&queue,element);
//     queuePrint(&queue);
//   }
//   printf("큐가 포화상태 입니다.\n\n");

//   printf("--데이터 삭제 단계--\n");
//   while(!is_empty(&queue)){
//     element = dequeue(&queue);
//     printf("꺼내진 정수: %d \n",element);
//     queuePrint(&queue);
//   }
//   printf("큐는 공백상태입니다.");
//   return 0;
// }

// buffer
//  typedef int element;
//  typedef struct{
//    element data[MAX_QUEUE_SIZE];
//    int front,rear;
//  }QueueType;

// //error function
// void error(char* message){
//   fprintf(stderr,"%s",message);
//   exit(1);
// }

// //reset queue
// void initQueue(QueueType* q){
//   q->front = 0;
//   q->rear = 0;
// }

// //check empty state
// int isEmpty(QueueType* q){
//   return (q->front == q->rear);
// }

// // check full state
// int isFull(QueueType* q){
//   return (q->front == ((q->rear+1)%MAX_QUEUE_SIZE));
// }

// // print queue
// void queuePrint(QueueType *q){
//   printf("QUEUE(front = %d rear = %d) ",q->front,q->rear);
//   if(!isEmpty(q)){
//     int i = q->front;
//     do{
//       i = (i+1)%MAX_QUEUE_SIZE;
//       printf("%d | ",q->data[i]);
//       if(i == q->rear)
//         break;
//     }while(i != q->front);
//   }
//   printf("\n");
// }

// // push function
// void enqueue(QueueType *q, element item){
//   if(isFull(q))
//     error("큐 포화 에러");
//   q->rear = (q->rear + 1)%MAX_QUEUE_SIZE;
//   q->data[q->rear] = item;
// }

// // pop function
// element dequeue(QueueType *q){
//   if(isEmpty(q)){
//     error("큐 공백 에러");
//   }
//   q->front = (q->front + 1)%MAX_QUEUE_SIZE;
//   return q->data[q->front];
// }

// //peek function
// element peek(QueueType* q){
//   if(isEmpty(q))
//     error("큐 공백 에러");
//   return q->data[(q->front+1)%MAX_QUEUE_SIZE];
// }

// int main(void){
//   QueueType queue;
//   int element;

//   initQueue(&queue);
//   srand(time(NULL));

//   for(int i = 0;i<100;i++){
//     if(rand()%5 == 0){
//       enqueue(&queue,rand()%100);
//     }
//     queuePrint(&queue);
//     if(rand()%10 ==0){
//       int data = dequeue(&queue);
//     }
//     queuePrint(&queue);
//   }
//   return 0;
// }
