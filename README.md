# File-Compression-Tool-using-Huffman-Coding

A complete **lossless file compression and decompression tool** implemented in **C++** using the Huffman Coding algorithm.

This project compresses a text file into a compact binary format and reconstructs the original file without any data loss.

---

## 🚀 Features

* Lossless compression using Huffman Coding
* Binary bit-level encoding (real compression, not 0/1 text)
* Automatic decompression
* Stores frequency table inside file header
* Rebuilds exact Huffman Tree during decoding
* Handles padding bits safely
* CLI based menu system

---

## 🧠 How It Works

### Compression

1. Read input file
2. Count character frequencies
3. Build Huffman Tree (Min Heap + Greedy algorithm)
4. Generate binary codes
5. Pack bits into bytes
6. Store:

   * Original file size
   * Frequency table
   * Encoded binary data

### Decompression

1. Read header (size + frequency table)
2. Rebuild identical Huffman tree
3. Read binary bits
4. Traverse tree
5. Restore original text

---

## 📂 Project Structure

```
Huffman-File-Compressor/
│
├── include/
│   ├── HuffmanNode.h
│   ├── HuffmanTree.h
│   ├── Compressor.h
│   └── Decompressor.h
│
├── src/
│   ├── HuffmanTree.cpp
│   ├── Compressor.cpp
│   └── Decompressor.cpp
│
├── input/
│   └── test.txt
│
├── output/
│   ├── compressed.bin
│   └── decompressed.txt
│
├── build/
│
└── main.cpp
```

---

## ⚙️ Compilation & Run

### Compile

```bash
g++ src/*.cpp main.cpp -o build/app
```

### Run

```bash
build/app
```

---

## ▶️ Menu

```
1 → Compress File
2 → Decompress File
3 → Exit
```

---

## 📊 Example

Input:

```
hello huffman compression project
this is my first compressor
```

Compressed → `compressed.bin`
Decompressed → `decompressed.txt` (identical to input)

---

## 🧩 Concepts Used

* Greedy Algorithms
* Priority Queue (Min Heap)
* Binary Trees
* Bit Manipulation
* File Handling (Binary I/O)
* Object Oriented Programming
* Data Structures & Algorithms

---

## 🎯 Learning Outcomes

This project demonstrates understanding of:

* Real file compression
* Memory-efficient encoding
* Serialization & deserialization
* Tree reconstruction
* Practical DSA implementation

---

## 📜 License

Open for learning and educational use.
