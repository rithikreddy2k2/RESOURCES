# RESOURCES

## JAVA TC's for in-built functions
### Worst-case time complexities of all Java built-in methods including String, StringBuilder, List classes, Set classes, Map classes, Queue classes, Stack, Arrays, and Collections classes:

### String

#### new String("str") instantiation with value -> O(n)
#### "str1" + "str2" concatenation -> O(n), better solution is String concat(String str) with O(n)
#### int length() -> O(1)
#### char charAt(int index) -> O(1)
#### int indexOf(int ch), int indexOf(int ch, int fromIndex), int indexOf(String str), int indexOf(String str, int fromIndex), int lastIndexOf(int ch), int lastIndexOf(int ch, int fromIndex), int lastIndexOf(String str), int lastIndexOf(String str, int fromIndex) -> O(n)
#### String substring(int beginIndex), String substring(int beginIndex, int endIndex) -> O(n)
#### String toLowerCase(), String toUpperCase() -> O(n)
#### boolean contains(CharSequence charSeq) -> O(n)
#### boolean equals(Object obj), boolean equalsIgnoreCase(String str) -> O(n)
#### boolean startsWith(String prefix), boolean endsWith(String suffix) -> O(n)
#### String replace(char oldChar, char newChar), String replace(CharSequence target, CharSequence replacement), String replaceAll(String regex, String replacement) -> O(n)
#### String[] split(String regex), String[] split(String regex, int limit) -> O(n)
#### char[] toCharArray() -> O(n)
#### boolean isEmpty() -> O(1)
#### boolean isBlank() -> O(n)
#### String strip(), String stripLeading(), String stripTrailing(), String trim(), String indent(int numberSpaces), String stripIndent(), String translateEscapes() -> O(n)
#### String format(String format, Object args...), String formatted(Object args...) -> O(n)

### StringBuilder

#### new StringBuilder("sb") instantiaton with value -> O(n)
#### StringBuilder append(String str) -> O(n)
#### StringBuilder append(int i), StringBuilder append(double d), etc. other append methods -> O(1)
#### StringBuilder insert(int offset, String str) -> O(n)
#### StringBuilder delete(int startIndex, int endIndex), StringBuilder deleteCharAt(int index) -> O(n)
#### StringBuilder replace(int startIndex, int endIndex, String newString) -> O(n)
#### StringBuilder reverse() -> O(n)
#### void setCharAt(int index, char ch) -> O(1)
#### String substring(int beginIndex), String substring(int beginIndex, int endIndex) -> O(n)
#### int length() - O(1)
#### char charAt(int index) -> O(1)
#### String toString() -> O(n)

### ArrayList (implements List interface)

#### E get(int index) -> O(1)
#### E remove(int index) -> O(n) with n/2 steps on average
#### boolean remove(E element) -> O(n)
#### Iterator.remove() -> O(n) with n/2 steps on average
#### void add(int index, E element) -> O(n) with n/2 steps on average
#### boolean add(E element) appending -> O(1)
#### ListIterator.add(E element) -> O(n) with n/2 steps on average
#### boolean contains(Object o) -> O(n)
#### E set(int index, E Element) -> O(1)
#### int indexOf(Object o), int lastIndexOf(Object o) -> O(n)
#### void clear() -> O(n)
#### int size() -> O(1)
#### boolean isEmpty() -> O(1)

### LinkedList (implements List and Deque interfaces)

#### E get(int index) -> O(n) with n/4 steps on average, O(1) when index=0 or index=list.size()-1
#### E remove(int index) -> O(n) with n/4 steps on average, O(1) when index=0 or index=list.size()-1
#### boolean remove(E element) -> O(n)
#### Iterator.remove() -> O(1)
#### void add(int index, E element) -> O(n) with n/4 steps on average, O(1) when index=0 or index=list.size()-1
#### boolean add(E element) appending -> O(1)
#### ListIterator.add(E element) -> O(1)
#### boolean contains(Object o) -> O(n)
#### E set(int index, E Element) -> O(n)
#### int indexOf(Object o), int lastIndexOf(Object o) -> O(n)
#### void clear() -> O(n)
#### int size() -> O(1)
#### boolean isEmpty() -> O(1)

### In summary ArrayList vs LinkedList:

#### access to front -> O(1) vs O(1)
#### access to back -> O(1) vs O(1)
#### access to middle -> O(1) vs O(n)
#### insert at front -> O(n) vs O(1)
#### insert at back (appending) -> O(1) vs O(1)
#### insert at middle using add(int index, E element) method -> O(n) with n/2 steps on average vs O(n) with n/4 steps on average

### HashSet (implements Set interface)

#### boolean add(E element) appending -> O(1)
#### boolean contains(Object o) -> O(1)
#### boolean remove(Object o) -> O(1)
#### int size() -> O(1)
#### boolean isEmpty() -> O(1)
#### void clear() -> O(n)
#### Object[] toArray() -> O(n)

### TreeSet (implements Set interface)

#### boolean add(E element) appending -> O(logn)
#### boolean contains(Object o) -> O(logn)
#### boolean remove(Object o) -> O(logn)
#### int size() -> O(1)
#### boolean isEmpty() -> O(1)
#### void clear() -> O(n)
#### E first() -> O(logn)
#### E last() -> O(logn)
#### E lower(E element) -> O(logn)
#### E higher(E element) -> O(logn)
#### E floor(E element) -> O(logn)
#### E ceiling(E element) -> O(logn)
#### Object[] toArray() -> O(n)

### HashMap (implements Map interface)
 
#### boolean containsKey(Object key) -> O(n), average-case complexity is Θ(1)
#### boolean containsValue(Object value) -> O(n)
#### V get(Object key), V getOrDefault(Object key, V defaultValue) -> O(n), average-case complexity is Θ(1)
#### V put(K key, V value), V putIfAbsent(K key, V value) -> O(n), average-case complexity is Θ(1)
#### V remove(Object key) -> O(n), average-case complexity is Θ(1)
#### boolean remove(Object key, Object value) -> O(n), average-case complexity is Θ(1)
#### V replace(K key, V value) -> O(n), average-case complexity is Θ(1)
#### boolean replace(K key, V oldValue, V newValue) -> O(n), average-case complexity is Θ(1)
#### int size() -> O(1)
#### boolean isEmpty() -> O(1)
#### void clear() -> O(n)
#### Set keySet() -> O(1)
#### Collection values() -> O(1)
#### Set<Map.Entry<K, V>> entrySet() -> O(1)

### TreeMap (implements Map interface)

#### boolean containsKey(Object key) -> O(logn)
#### boolean containsValue(Object value) -> O(n)
#### V get(Object key), V getOrDefault(Object key, V defaultValue) -> O(logn)
#### V put(K key, V value), V putIfAbsent(K key, V value) -> O(logn)
#### V remove(Object key) -> O(logn)
#### int size() -> O(1)
#### boolean isEmpty() -> O(1)
#### void clear() -> O(n)
#### Set keySet() -> O(1)
#### Collection values() -> O(1)
#### Set<Map.Entry<K, V>> entrySet() -> O(1)
#### K firstKey() -> O(logn)
#### K lastKey() -> O(logn)
#### K lowerKey(K key) -> O(logn)
#### K floorKey(K key) -> O(logn)
#### K ceilingKey(K key) -> O(logn)
#### K higherKey(K key) -> O(logn)

### PriorityQueue (implements Queue interface)

#### boolean add(E element), boolean offer(E element) appending -> O(logn)
#### E element(), E peek() read from front -> O(1)
#### E remove(), E poll() get and remove from front -> O(logn)
#### int size() -> O(1)

### ArrayDeque (implements Deque interface)

#### void addFirst(E element), boolean offerFirst(E element), void push(E element) add to front -> O(1)
#### boolean add(E element), boolean offer(E element), void addLast(E element), boolean offerLast(E element) add to back -> O(1)
#### E element(), E peek(), E getFirst(), E peekFirst() read from front -> O(1)
#### E getLast(), E peekLast() read from back -> O(1)
#### E remove(), E poll(), E removeFirst(), E pollFirst(), E pop() get and remove from front -> O(1)
#### E removeLast(), E pollLast() get and remove from back -> O(1)
#### int size() -> O(1)
#### Stack (extends Vector class and implements List interface)
#### 
#### E push(E item) -> O(1)
#### E pop() -> O(1)
#### E peek() -> O(1)
#### boolean empty() -> O(1)
#### int search(Object o) -> O(n)

### Arrays

#### void sort(int[] a) -> O(nlogn)
#### void sort(int[] a, int fromIndex, int toIndex) -> O(nlogn)
#### int binarySearch(int[] a, int key) -> O(logn)
#### List asList(T... arr) -> O(1)
#### void fill(int[] a, int val) -> O(n)
#### int compare(int[] a, int[] b) -> O(n)
#### String toString(int[] a) -> O(n)
#### int[] copyOf(int[] original, int newLength) -> O(n)
#### int[] copyOfRange(int[] original, int from, int to) -> O(n)

### Collections

#### void sort(List list) -> O(nlogn)
#### T max(Collection<? extends T> coll) -> O(n)
#### T min(Collection<? extends T> coll) -> O(n)
#### void shuffle(List<?> list) -> O(n)
#### void fill(List<? super T> list, T obj) -> O(n)
#### void rotate(List<?> list, int distance) -> O(n)
