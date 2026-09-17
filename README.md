# graphs_cviramon Library


## features

Uses Dijkstra's algorithm that computes the shortest distance or path from sorce vertex to other vertices

## Development setup 
'''powershell 
git clone https://github.com/Barlos1233/homework5.git
cd homework5
python -m venv venv
.\venv\Scripts\Activate.ps1
pip install .
'''

## Usage 
 '''Python
 In test.py: 

 from graphs_tmota import sp
import sys

if __name__ == '__main__':
    
    if len(sys.argv) != 2:
        print(f'Use: {sys.argv[0]} graph_file')
        sys.exit(1)

    graph = {}
    with open(sys.argv[1], 'rt') as f:
        for line in f:
            line = line.strip()
            s, d, w = line.split()
            s = int(s)
            d = int(d)
            w = int(w)
            if s not in graph:
                graph[s] = {}
            graph[s][d] = w
    
    s = 0
    dist, path = sp.dijkstra(graph, s)
    print(f'Shortest distances from {s}:')
    print(dist)
    for d in path: 
        print(f'spf to {d}: {path[d]}')

## Project Structures 
src
|__graphs_cviramon
   |__ __init__.py
   |__ heapq.py
   |__ sp.py
|__test.py
|__README.md
|__pyproject.toml

##e Branch workflows 
- 'main' - protectied and stable branch
- 'dev' - active devoplement branch
Contributions should me made from pull request

## Contributing 
This is a public repo. contributions are welcome, open a pull request against the 'dev' branch. 



## (USED CLAUDE FOR README.md FORMAT) - README.md was referenced from claude format on how it should look like. **Typed out and overviewed by Author (ME, CARLOS VIRAMONTES)**

## SOURCES 
- Other sources such as code and structure given by course. 