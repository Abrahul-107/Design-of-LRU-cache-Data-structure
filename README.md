# Design-of-LRU-cache-Data-structure
LRU Caching Data Structure Design with Different Data Structure

# What is caching ?
- Caching is the process of copies of files in a cache or temporary storage location so that we can access more quicky for our use .
- A cache is a temporary storage location for copes of data .

# What does a browser cache do ?
- Every time a user loads a webpage, their browser has to download quite a lot of data in order to display that webpage. To shorten page load times, browsers cache most of the content that appears on the webpage, saving a copy of the webpage's content on the device's hard drive. This way, the next time the user loads the page, most of the content is already stored locally and the page will load much more quickly.

- Browsers store these files until their time to live (TTL) expires or until the hard drive cache is full. (TTL is an indication of how long content should be cached.) Users can also clear their browser cache if desired.


# What is LRU-cache ?
- LRU stands for least recently used which is an algorithm used for caching .

- As the name suggests when the cache memory is full LRU picks the data that is least recently used and removes it in order to make space for the new data. 
- The priority of the data in the cache changes according to the need of that data,  i.e. if some data is fetched or updated recently then the priority of that data would be changed and assigned to the highest priority, and the priority of the data decreases if it remains unused operations after operations.

# Operations on LRU Cache:
- **LRUCache (Capacity c):** Initialize LRU cache with positive size capacity c.

- **get (key):** Returns the value of Key ‘k’ if it is present in the cache otherwise it returns -1. Also updates the priority of data in the LRU cache.
- **put (key, value):** Update the value of the key if that key exists, Otherwise, add key-value pair to the cache. If the number of keys exceeded the capacity of LRU cache then dismiss the least recently used key.

# Working of LRU Cache:
Let’s suppose we have an LRU cache of capacity 3, and we would like to perform following operations:

- Put (key=1, value=A) into the cache
- Put (key=2, value=B) into the cache
- Put (key=3, value=C) into the cache
- Get (key=2) from the cache
- Get (key=4) from the cache
- Put (key=4, value=D) into the cache
- Put (key=3, value=E) into the cache
- Get (key=4) from the cache
- Put (key=1, value=A) into the cache

# Diagram representation
- ![alt text](Working-of-LRU-Cache-(1).png)

# Real-World Application of LRU Cache:
- In Database Systems for fast query results.

- In Operating Systems to minimize page faults.
- Text Editors and IDEs to store frequently used files or code snippets
- Network routers and switches use LRU to increase the efficiency of computer network
- In compiler optimizations
- Text Prediction and autocompletion tools

# Advantages of LRU cache:
- Fast Access: It takes O(1) time to access the data from the LRU cache.

- Fast Update: It takes O(1) time to update a key-value pair in the LRU cache.
- Fast removal of Least recently used data: It takes O(1) delete that which has not been recently used.
- No thrashing: LRU is less susceptible to thrashing compared to FIFO because it considers the usage history of pages. It can detect which pages are being used frequently and prioritize them for memory allocation, reducing the number of page faults and disk I/O operations.
# Disadvantages of LRU cache:
- It requires large cache size to increase efficiency.
- It requires additional Data Structure to be implemented.
- Hardware assistance is high.
- In LRU error detection is difficult as compared to other algorithms.
- It has limited acceptability.
