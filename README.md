## DAA
### 1.BFS
````
#include<stdio.h>
#define MAXSIZE 20
struct queue
{
int data[MAXSIZE];
int front,rear;
};
void initq(struct queue *pq)
{
pq->front=pq->rear = -1;
}
void addq(struct queue *pq, int n)
{
pq->data[++pq->rear]=n;
}
int removeq (struct queue *pq)
{
return pq->data[++pq->front];
}
int isempty (struct queue *pq)
{
return (pq->front==pq->rear);
}
int isfull(struct queue *pq)
{
return (pq->rear==MAXSIZE-1);
}
void bfs(int m[10][10],int n)
{
int i,j,v,w;
int visited[20]={0};
struct queue q;
initq(&q);
printf("The BFS traversal is:\n");
v=1;
visited[v]=1;
addq(&q,v);
while(!isempty(&q))
{
v=remove(&q);
printf("v%d",v);
for(w=1;w<=n;w++)
{
if((m[v][w]==1)&&(!visited[w]))
{
addq(&q,w);
visited[w]=1;
}
}
}
}
int main()
{
int m[5][5]={{0,0,1,1,0},{0,0,1,0,1},{0,1,0,0,0},{0,0,0,0,1},{0,0,0,0,0}};
bfs(m,5);
}
````


### 2.DFS
````
#include <stdio.h>
#define MAX 100
int visited[MAX] = {0};
int adjacency_matrix[MAX][MAX];
int n;
void DFS(int vertex) {
int i;
visited[vertex] = 1;
printf("%d ", vertex);
for(i = 0; i < n; i++) {
if(adjacency_matrix[vertex][i] && !visited[i]) {
DFS(i);
}
}
}
int main() {
int i, j, start_vertex;
printf("Enter the number of vertices: ");
scanf("%d", &n);
printf("Enter the adjacency matrix: \n");
for(i = 0; i < n; i++) {
for(j = 0; j < n; j++) {
scanf("%d", &adjacency_matrix[i][j]);
}
}
printf("Enter the starting vertex: ");
scanf("%d", &start_vertex);
printf("DFS traversal: ");
DFS(start_vertex);
return 0;
}
````

### 3. Dijkstraj
````
````




### 4. Heap Sort
````
````
### 5. Insertion
````
````
### 6. Kruskal
````
````

### 7. Prims
````
````
### 8. Selection
````
````

### 9. Topological Sort
````
````

