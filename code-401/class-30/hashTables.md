# Hash Tables

## Overview

Hash tables are a fundamental data structure in computer science, designed to store key-value pairs for efficient retrieval. They leverage a hash function to compute an index into an array where the value associated with the key is stored, enabling quick lookups.

## In Simple Terms

Imagine a library where books are stored not by their titles but by a unique code derived from the title. When you need a book, you simply provide the title, the library computes the code, and directs you exactly where the book is, without needing to search the entire collection. Hash tables work similarly in storing and retrieving data.

## Key Terms

- **Hash**: A function that converts a key into an array index.
- **Buckets**: Array indices where key-value pairs are stored.
- **Collisions**: When two keys hash to the same index.

## Creating a Simple Hash Function

```js
function simpleHash(key, tableSize) {
  let hash = 0;
  for (let i = 0; i < key.length; i++) {
    hash += key.charCodeAt(i);
  }
  return hash % tableSize;
}
```

## Example: Using a Hash Table

Using a hash table to store and retrieve zip codes for neighborhoods:

```js
const hashTableSize = 1024; // Size of the hash table

let hashTable = new Array(hashTableSize); // Initializing the hash table

// Hash function
function hashKey(key) {
  let hash = 0;
  for (let i = 0; i < key.length; i++) {
    hash = (hash + key.charCodeAt(i) * i) % hashTableSize;
  }
  return hash;
}

// Set value in hash table
function set(key, value) {
  const index = hashKey(key);
  if (!hashTable[index]) {
    hashTable[index] = [];
  }
  hashTable[index].push([key, value]);
}

// Get value from hash table
function get(key) {
  const index = hashKey(key);
  const bucket = hashTable[index];
  if (bucket) {
    for (let i = 0; i < bucket.length; i++) {
      if (bucket[i][0] === key) {
        return bucket[i][1]; // Return the value
      }
    }
  }
  return undefined; // Key not found
}

// Adding neighborhoods and their zip codes
set("Greenwood", "98103");
set("Downtown", "98101");

// Retrieving a zip code
console.log(get("Greenwood")); // Outputs: 98103
```

### Breakdown

- The `hashKey` function computes an array index based on a key.
- The `set` function adds a key-value pair to the hash table, handling collisions by storing multiple entries at the same index in a nested array (bucket).
- The `get` function retrieves a value by its key, iterating through the bucket at the computed index if necessary.

## Summary

Hash tables are an efficient data structure for storing and accessing data via key-value pairs, using a hash function to compute the storage index. They are widely used in software development for tasks that require quick data retrieval, such as databases, caching, and lookup tables. Handling collisions and ensuring an even distribution of hash values are critical for maintaining their performance.
