---
title: Complexity in Data Structures & Algorithms
date: '2023-01-28'
tags: ['foundation', 'swift']
draft: true
summary: 'In this article, I will introduce complexity in terms of Data Structures & Algorithms with Swift.'
---

Apa yang dapat diskalakan dalam algoritme? Skalabilitas mengacu pada kinerja algoritme dalam hal waktu eksekusi dan penggunaan memori saat ukuran input meningkat. Kemudian memahami bagaimana mengukur input data dan eksekusinya dengan algoritma itu penting. Kita akan mempelajari notasi Big O untuk mengetahui berbagai tingkat skalabilitas dalam dua dimensi waktu eksekusi dan penggunaan memori.

Time Complexity

Time complexity is a measure of the time required to run an algorithm as the input size increases.

Constant Time

A constant time algorithm is one that has the same running time regardless of the size of the input.

```
func checkFirst(names: [String]) {
  if let first = names.first {
    print(first)
  } else {
    print("no names")
  }
}
```

Insert the constant time graph

The size of the names array has no effect on the running time of this function. Whether the input has ten items or 10 million items, this function only checks the first element of the array. As input data increases, the amount of time the algorithm takes does not change.

The Big O notation for constant time is O(1)

Linear Time

Linear time complexity is usually the easiest to understand. As the amount of data increases, the running time increases by the same amount.

```
func printNames(names: [String]) {
  for name in names {
    print(name)
  }
}
```

Insert the linear time graph

** The Big O notation for linear time is O(n). **

Quadratic Time

More commonly referred to as n squared, this time complexity refers to an algorithm that takes time proportional to the square of the input size.

```
func printNames(names: [String]) {
  for _ in names {
    for name in names {
      print(name)
    }
} }
```

Insert the quadratic time graph

Unlike the previous function, which operates in linear time, the n squared algorithm can quickly run out of control as the data size increases. As the size of the input data increases, the amount of time it takes for the algorithm to run increases drastically. Thus, n squared algorithms don’t perform well at scale.

The Big O notation for quadratic time is O(n2).

Logarithmic Time

So far, you’ve learned about the linear and quadratic time complexities wherein each element of the input is inspected at least once. However, there are scenarios in which only a subset of the input needs to be inspected, leading to a faster runtime. Algorithms that belong to this category of time complexity are ones that can leverage some shortcuts by making some assumptions about the input data.

How to optimize the O(n)? We can use this technique.

```
let numbers = [1, 3, 56, 66, 68, 80, 99, 105, 450]

// A linear time solution

func naiveContains(_ value: Int, in array: [Int]) -> Bool {
  for element in array {
    if element == value {
return true
} }
return false
}

// A logarithmic time solution by remove half of the input

func naiveContains(_ value: Int, in array: [Int]) -> Bool {
  guard !array.isEmpty else { return false }
  let middleIndex = array.count / 2
  if value <= array[middleIndex] {
    for index in 0...middleIndex {
      if array[index] == value {
return true
} }
  } else {
    for index in middleIndex..<array.count {
      if array[index] == value {
      return true
    } }
  }
return false
}
```

However, since the array is sorted, you can, right off the bat, drop half of the comparisons necessary by checking the middle value. The above function makes a small but meaningful optimization wherein it only checks half of the array to come up with a conclusion. An algorithm that can repeatedly drop half of the required comparisons will have logarithmic time complexity.

Insert the logarithmic time graph

As input data increases, the time it takes to execute the algorithm increases at a slow rate. If you look closely, you may notice that the graph seems to exhibit asymptotic behavior. This can be explained by considering the impact of halving the number of comparisons you need to do.

The Big O notation for logarithmic time complexity is O(log n)

Quasilinear Time

Quasilinear time algorithms perform worse than linear time but dramatically better than quadratic time. They are among the most common algorithms you’ll deal with which is a multiplication of linear and logarithmic time.

Insert the quasilinear time graph

** The Big-O notation for quasilinear time complexity is O(n log n) **

Other Time Complexities

polynomial time, exponential time, factorial time and more.

Space Complexity

The time complexity of an algorithm can help predict scalability, but it isn’t the only metric. Space complexity is a measure of the resources required for the algorithm to run. For computers, the resources for algorithms is memory.

```
func printSorted(_ array: [Int]) {
  let sorted = array.sorted()
  for element in sorted {
    print(element)
  }
}
```

Since array.sorted() will produce a brand new array with the same size of array, the space complexity of printSorted is O(n).

```
func printSorted(_ array: [Int]) {
  // 1
  guard !array.isEmpty else { return }
// 2
  var currentCount = 0
  var minValue = Int.min
// 3
  for value in array {
    if value == minValue {
      print(value)
      currentCount += 1
    }
  }
  while currentCount < array.count {
// 4
    var currentValue = array.max()!
    for value in array {
      if value < currentValue && value > minValue {
        currentValue = value
      }
}
// 5
    for value in array {
      if value == currentValue {
        print(value)
        currentCount += 1
      }
}
// 6
    minValue = currentValue
  }
}
```

The above algorithm only allocates memory to keep track of a few variables, so the space complexity is O(1). This is in contrast with the previous function, which allocates an entire array to create the sorted representation of the source array.

Other Notations

So far, you’ve evaluated algorithms using Big O notation. This is by far the most common measurement that programmers evaluate with. However, there exist other notations as well.

Big Omega notation is used to measure the best-case runtime for an algorithm. This isn’t as useful as Big O because getting the best case is often untenable.

Big Theta notation is used to measure the runtime for an algorithm that has the same best and worse case.

Source

https://www.raywenderlich.com

That's a Wrap! 🎁

Key Takeaways:

Time complexity is a measure of the time required to run an algorithm as the input size increases.

You should know about constant time, logarithmic time, linear time, quasilinear time and quadratic time and be able to order them by cost.

Space complexity is a measure of the resources required for the algorithm to run.

Big O notation is used to represent the general form of time and space complexity.

Time and space complexity are high-level measures of scalability; they do not measure the actual speed of the algorithm itself.

For small data sets, the time complexity is usually irrelevant. For example, a quasilinear algorithm can be slower than a quadratic algorithm when n is small.
