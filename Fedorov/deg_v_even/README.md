# Степени всех вершин графа четные 
## Определение
Степень (валентность) вершины графа (deg(u)) — количество рёбер графа G, инцидентных вершине u.
## Алгоритм
Метод проходит по всем вершинам в списке смежности. Для каждой вершины проверяется длина (размер) списка смежных вершин (степень вершины). Если степень вершины нечетная (остаток от деления на 2 не равен 0), метод сразу возвращает false, так как это означает, что не все вершины имеют четную степень.
```Java
    public boolean execute(Graph graph) {
        Map<UUID, List<UUID>> adjacencyList = getAdjacencyList(graph);
        for (UUID vertex:adjacencyList.keySet()){
            if (adjacencyList.get(vertex).size() %2 != 0){
                return false;
            }
        }
        return true;

    }
```
## Примечания
1. Пустоф граф возвращает True
2. Одна вершина возвращает True
