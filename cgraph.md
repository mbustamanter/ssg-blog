# Graphs in C
\toc
## Preamble
First, we feed the preprocessor the required libraries and definitions to work with. ``<stdlib.h>``
is included to allow the used of ``malloc()``. ``rep(i,a,b)`` is faster than writing ``for`` loops
and ``MAXV`` represents the maximum number of vertices in the graph. Note that we count from 1.
```c
#include <stdio.h>
#include <stdlib.h>
#define rep(i,a,b) for (int i=a; i<b; i++)
#define MAXV 101
```
## ``struct`` definition
The ``edgenode`` struct contains information about the node at the end of the edgde, and
the ``graph`` is defined using the adjacency list represenation, while keeping information
about each node in the form of a list that represents the number of neighbors it has.
```c
typedef struct edgenode {
    int y;
    struct edgenode *next;
} edgenode;
typedef struct {
    edgenode *edges[MAXV];
    int degree[MAXV];
    int nvertices,nedges;
} graph;
```
## Initialization and Construction
We need to make sure the graph is properly initialized, that is, each adjacency list is empty
and it node isn't pointing to any other node.
```c
void initialize_graph(graph *g) {
    g->nvertices=0; g->nedges=0;
    rep (i,0,MAXV) g->edges[i]=NULL;
    rep (i,0,MAXV) g->degree[i]=0;
}
```
Then the functions for inserting edges and reading the graph. This version of the ``inser_edge`` 
function supports directed and nod-directed insertions, and  the ``read_graph`` function
reads edges in the form of two ``int`` variables. Each variable represents one end of an edge.
```c
void insert_edge(graph *g, int x, int y, int und) {
    edgenode *p=malloc(sizeof(edgenode));
    p->y=y; p->next=g->edges[x]; g->edges[x]=p; g->degree[x]++;
    if (und==1) {
        insert_edge(g,y,x,0);
        g->nedges++;
    }
}
void read_graph(graph *g, int n, int m) {
    initialize_graph(g); g->nvertices=n;
    int x,y;
    rep (i,0,m) {
        scanf("%d %d\n",&x,&y);
        insert_edge(g,x,y,1);
    }
}
```