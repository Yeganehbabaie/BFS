from collections import defaultdict 
class UnDirectedGraph: 
      
    def __init__(self): 
   
        
        self.graph = defaultdict(list)
        self.E = 0
   
    
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


 #for example:
# if __name__ == '__main__':
    
    #g = UnDirectedGraph()
    #g.addEdge(0, 1) 
    #g.addEdge(0, 4) 
    #g.addEdge(1, 4) 
    #g.addEdge(1, 3) 
    #g.addEdge(1, 2) 
    #g.addEdge(2, 3) 
    #g.addEdge(3, 4) 
    #print('print Graph:')
    #g.printGraph()
    
    #print('BFS:',end=' ')
    #g.BFS(0)
    
#Use the example above to test bfs.
The output is as follows:
print Graph:

0 : 1 4

1 : 0 4 3 2

4 : 0 1 3

3: 1 2 4

2:1 3

BFS: 0 1 4 3 2
