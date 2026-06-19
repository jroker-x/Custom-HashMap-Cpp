# Custom HashMap

A hash map implementation built from scratch in C++ for learning data structures and template programming.

## Features

* Template-based key/value storage
* Custom hash function
* Separate chaining collision handling
* Dynamic rehashing
* Automatic load factor tracking
* insert()
* find()
* contains()
* operator[]
* size()
* bucketCount()
* loadFactor()

## Example

```cpp
HashMap<std::string, int> map;

map["apple"] = 5;
map["banana"] = 10;

std::cout << map["apple"] << '\n';

if (map.contains("banana"))
{
    std::cout << "Found banana\n";
}
```

## Concepts Practiced

* Templates
* References and pointers
* Hashing
* Collision resolution
* Dynamic resizing (rehashing)
* STL containers
* Move semantics

## Implementation Details

Collisions are handled using separate chaining with:

```cpp
std::vector<
    std::vector<
        std::pair<K, V>
    >
>
```

When the load factor reaches 1.0, the container automatically doubles the number of buckets and rehashes all stored elements.

## Future Improvements

* erase()
* Custom hash functors
* Iterators
* Const-correct find()
* Better hash function
* Exception safety

## What I Learned

This project helped me understand how hash maps work internally, including bucket allocation, collision handling, load factors, and rehashing.
