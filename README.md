from collections import defaultdict 
class UnDirectedGraph: 
     # Constructor 
    def __init__(self): 
   
        # default dictionary to store graph 
        self.graph = defaultdict(list)
        self.E = 0
   
    # function to add an edge to graph 
    def addEdge(self,u,v): 
        if v in self.graph[u]:
            return
        if u == v:
            self.graph[u].append(v)
            return
         
        self.graph[u].append(v)
        self.graph[v].append(u)
        self.E+=1
    def V(self):
        return len(self.graph)
    def Edge(self):
        return self.E
     
    def printGraph(self):
        for i in self.graph: 
            print(i,':',end=' ')
            for j in self.graph[i]:
                print(j, end= ' ')
            print()


    
