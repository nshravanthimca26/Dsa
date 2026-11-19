def display(arr, n):
    for i in range(n):
        print(arr[i], end=" ")
    print()


def bubble_sort(arr, n):
    comparisons = 0
    swaps = 0

    for i in range(n - 1):
        for j in range(n - i - 1):
            comparisons += 1

            if arr[j] > arr[j + 1]:
                temp = arr[j]
                arr[j] = arr[j + 1]
                arr[j + 1] = temp
                swaps += 1

    return comparisons, swaps


def selection_sort(arr, n):
    comparisons = 0
    swaps = 0

    for i in range(n - 1):
        min_index = i

        for j in range(i + 1, n):
            comparisons += 1

            if arr[j] < arr[min_index]:
                min_index = j

        if min_index != i:
            temp = arr[i]
            arr[i] = arr[min_index]
            arr[min_index] = temp
            swaps += 1

    return comparisons, swaps


def binary_search(arr, low, high, key, count):
    if low > high:
        return -1, count

    mid = (low + high) // 2
    count += 1

    if arr[mid] == key:
        return mid, count

    elif arr[mid] < key:
        return binary_search(arr, mid + 1, high, key, count)

    else:
        return binary_search(arr, low, mid - 1, key, count)


n = int(input("Enter number of elements: "))

arr = [0] * n

for i in range(n):
    arr[i] = int(input("Enter element: "))

b = [0] * n
s = [0] * n

for i in range(n):
    b[i] = arr[i]
    s[i] = arr[i]

print("\nOriginal Array:")
display(arr, n)

bc, bs = bubble_sort(b, n)

print("\nBubble Sort:")
display(b, n)
print("Comparisons:", bc)
print("Swaps:", bs)

sc, ss = selection_sort(s, n)

print("\nSelection Sort:")
display(s, n)
print("Comparisons:", sc)
print("Swaps:", ss)

key = int(input("\nEnter element to search: "))

pos, count = binary_search(b, 0, n - 1, key, 0)

if pos == -1:
    print("Element not found")
else:
    print("Element found at index:", pos)

print("Binary Search comparisons:", count)
