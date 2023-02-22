def bfs(graph, source):
    visited = set()  # to keep track of already visited nodes
    bfs_traversal = list()  # the BFS traversal result
    queue = list()  # queue

    # push the root node to the queue and mark it as visited
    queue.append(source)
    visited.add(source)

    # loop until the queue is empty
    while queue:
        # pop the front node of the queue and add it to bfs_traversal
        current_node = queue.pop(0)
        bfs_traversal.append(current_node)

        # check all the neighbour nodes of the current node
        for neighbour_node in graph[current_node]:
            # if the neighbour nodes are not already visited,
            # push them to the queue and mark them as visited
            if neighbour_node not in visited:
                visited.add(neighbour_node)
                queue.append(neighbour_node)

    return bfs_traversal


if __name__ == '__main__':
    graph = {
        'A': ['B', 'C', 'D'],
        'B': ['A', 'D', 'E'],
        'C': ['A', 'D'],
        'D': ['B', 'C', 'A', 'E'],
        'E': ['B', 'D']
    }

    bfs_traversal = bfs(graph, 'A')
    print(bfs_traversal)
