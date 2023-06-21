# Graphs in C
\toc
## ``struct`` definition
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
```c
void initialize_graph(graph *g) {
    g->nvertices=0; g->nedges=0;
    rep (i,0,MAXV) g->edges[i]=NULL;
    rep (i,0,MAXV) g->degree[i]=0;
}
```

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
        insert_Edge(g,x,y,1);
    }
}
```