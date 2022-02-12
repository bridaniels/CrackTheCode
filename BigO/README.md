# Big 0 
- language and metric used to describe the efficiency of algorithms 
- describes rate of increase in runtime/space

---
### O(Big O): an upper bound on time -> typically refer to Big O
### Ω(Big Omega): lower bound on time 
### Θ(Big Theta): Θ means both O and Ω -> tight bound on runtime
---

### Drop non-dominant terms and constants:
- O(N² + N) becomes O(N²)
- O(N + log N) becomes O(N)
- O(5*2ᴺ + 100N¹⁰⁰) becomes O(2ᴺ)
---

### Adding VS. Multiplying w/ Multipart Algorithms
- two distinct loops: addition
    - one chunk of work happens, then the next chunk of work happens
    - do this, then do that
- two nested loops: multiplication
    - do second chunk of work for each element in first chunk of work 
    - do this every time you do that 
--- 

### Amortized Time
- ArrayList is a dynamically resizing array 
    - benefits of an array while offering size flexibility 
    - implemented within an array 
    - array hits capacity, the ArrayList class will create a new array with double the capcity and copy elements over into the new array 
- Full array with N elements
    - adding a new element = O(N) time 
    - having to create a new array of size 2N + copy N elements over 
- Majority of adding in O(1) time
    - 1+2+4+8+16+32+.... adding elements and doubling capcity 
    - array size power of 2 
    - after x elements, array size doubles in capcity 
    - going backwards... x + x/2 + x/4 + x/8 +.... = 2x
- X adds take O(X) time -> amortized time for each addition to the array = O(1)
---

### Log N Runtime
- Number of elements in the problem space gets halved each time 
    - often recurisve algorithms 
- Base of log does not matter in regards to Big O ("Bases of Logs" pg. 631)
- Nodes per level = xʲ
    - x = number of recurisve calls 
    - j = level of recursion tree
    - O(branchesᴰᴱᴾᵀᴴ)
- Space Complexity = O(N) for O(2ᴺ) 
    - only O(N) nodes exist at any given time due to splitting into smaller arrays at each level
---