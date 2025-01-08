# Minimum-Value-Transformation

In a mystical land, Dev was given two integers, N and K, by a wise sage. Starting with a number A = 1, Dev had to perform exactly N operations to transform A. In each move, he could either double the value of A or add K to it. The challenge was to find the minimum possible value of A after completing exactly N operations. Can you help Dev figure out the smallest value of A at the end of the journey?

def minimum_value_transformation(N, K):

    # Start with A = 1
    A = 1
    # Perform the operations
    for _ in range(N):
        # Decide the best operation: double or add K
        if A < K:
            A *= 2
        else:
            A += K
    return A

# Input reading
N, K = map(int, input().split())
# Output the result
print(minimum_value_transformation(N, K))
