# Heap Data Structures in C++

## Introduction to Heaps

A heap is a specialized tree-based data structure that satisfies the heap property. There are two types of heaps:

1. **Min Heap**: The parent node is always smaller than or equal to its children
2. **Max Heap**: The parent node is always greater than or equal to its children

## Basic Heap Implementation

### Min Heap Class
Here's a basic implementation of a Min Heap:

\`\`\`cpp
class MinHeap {
    int* arr;
    int size;        // Total elements in heap
    int total_size;  // Total capacity

public:
    MinHeap(int n) {
        arr = new int[n];
        size = 0;
        total_size = n;
    }

    void insertval(int value) {
        if (size == total_size) {
            cout << "\\nHeap is full" << endl;
            return;
        }
        
        arr[size] = value;
        int index = size;
        size++;
        
        // Bubble up to maintain min-heap property
        while (index > 0 && arr[(index - 1) / 2] > arr[index]) {
            swap(arr[index], arr[(index - 1) / 2]);
            index = (index - 1) / 2;
        }
    }

    ~MinHeap() {
        delete[] arr;
    }
};
\`\`\`

### Max Heap Implementation

For the Max Heap implementation:

\`\`\`cpp
void heapify(int arr[],int index,int n){
    int largest=index;
    int left=2*index+1;
    int right=2*index+2;
    if(left<n && arr[largest]<arr[left]){
        largest=left;
    }
    if(right<n && arr[largest]<arr[right]){
        largest=right;
    }
    if(largest!=index){
        swap(arr[index],arr[largest]);
        heapify(arr,largest,n);
    }
}
\`\`\`

This shows the heapify function that maintains the max heap property.

## Key Operations

### 1. Insertion
The insertion process involves:
1. Adding the element at the end
2. Bubbling up until heap property is satisfied

### 2. Deletion
For deletion implementation:

\`\`\`cpp
void deleteval(int arr[],int &n){
    if(n<=0){
        cout<<"empty ha bsdk\\n";
        return;
    }
    arr[0]=arr[n-1];
    n--;
    heapify(arr,0,n);
}
\`\`\`

### 3. Heap Sort
The heap sort implementation:

\`\`\`cpp
void sorting(int arr[],int n){
    for(int i=n-1;i>0;i--){
        swap(arr[i],arr[0]);
        heapify(arr,0,i);
    }
}
\`\`\`

## Memory Management

Since heaps are typically implemented using dynamic arrays, proper memory management is crucial:

1. Allocation during initialization:
\`\`\`cpp
arr = new int[n];
\`\`\`

2. Deallocation in destructor:
\`\`\`cpp
~MinHeap() {
    delete[] arr;
}
\`\`\`

## Special Applications

### 1. Finding Minimum Distance
For finding minimum distance between elements in a BST using heap properties:

\`\`\`cpp
void print_cube(){
    for(int i=0;i<size;i++){
        cout<<arr[i]*arr[i]*arr[i]<<" ";
    }
}
\`\`\`

### 2. Building Heap from Array
To build a heap from an existing array:

\`\`\`cpp
void buildMinHeap(int heap[], int size) {
    for (int i = size / 2 - 1; i >= 0; i--) {
        minHeapify(heap, size, i);
    }
}
\`\`\`

## Time Complexities

- Insertion: O(log n)
- Deletion: O(log n)
- Build Heap: O(n)
- Heapify: O(log n)
- Heap Sort: O(n log n)

## Best Practices

1. Always check for heap overflow before insertion
2. Properly manage memory with destructors
3. Use heapify for maintaining heap property
4. Consider using STL's priority_queue for built-in heap functionality
