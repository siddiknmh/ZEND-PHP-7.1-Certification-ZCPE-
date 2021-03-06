#### Datastructures
http://php.net/manual/en/spl.datastructures.php

--------------------------------------

##### SplDoublyLinkedList

http://php.net/manual/en/class.spldoublylinkedlist.php

<p>The SplDoublyLinkedList class provides the main functionalities of a doubly linked list.</p>

```PHP
SplDoublyLinkedList implements Iterator , ArrayAccess , Countable
```

- SplDoublyLinkedList::add — Add/insert a new value at the specified index
- SplDoublyLinkedList::bottom — Peeks at the node from the beginning of the doubly linked list
- SplDoublyLinkedList::__construct — Constructs a new doubly linked list
- SplDoublyLinkedList::count — Counts the number of elements in the doubly linked list.
- SplDoublyLinkedList::current — Return current array entry
- SplDoublyLinkedList::getIteratorMode — Returns the mode of iteration
- SplDoublyLinkedList::isEmpty — Checks whether the doubly linked list is empty.
- SplDoublyLinkedList::key — Return current node index
- SplDoublyLinkedList::next — Move to next entry
- SplDoublyLinkedList::offsetExists — Returns whether the requested $index exists
- SplDoublyLinkedList::offsetGet — Returns the value at the specified $index
- SplDoublyLinkedList::offsetSet — Sets the value at the specified $index to $newval
- SplDoublyLinkedList::offsetUnset — Unsets the value at the specified $index
- SplDoublyLinkedList::pop — Pops a node from the end of the doubly linked list
- SplDoublyLinkedList::prev — Move to previous entry
- SplDoublyLinkedList::push — Pushes an element at the end of the doubly linked list
- SplDoublyLinkedList::rewind — Rewind iterator back to the start
- SplDoublyLinkedList::serialize — Serializes the storage
- SplDoublyLinkedList::setIteratorMode — Sets the mode of iteration
- SplDoublyLinkedList::shift — Shifts a node from the beginning of the doubly linked list
- SplDoublyLinkedList::top — Peeks at the node from the end of the doubly linked list
- SplDoublyLinkedList::unserialize — Unserializes the storage
- SplDoublyLinkedList::unshift — Prepends the doubly linked list with an element
- SplDoublyLinkedList::valid — Check whether the doubly linked list contains more nodes

<dd>

<p class="para">
There are two orthogonal sets of modes that can be set:
</p>
<ul class="itemizedlist">
<li class="listitem">
<span class="simpara">The direction of the iteration (either one or the other):</span>
<ul class="itemizedlist">
 <li class="listitem"><span class="simpara"><strong><code>SplDoublyLinkedList::IT_MODE_LIFO</code></strong> (Stack style)</span></li>
 <li class="listitem"><span class="simpara"><strong><code>SplDoublyLinkedList::IT_MODE_FIFO</code></strong> (Queue style)</span></li>
</ul>
</li>
<li class="listitem">
<span class="simpara">The behavior of the iterator (either one or the other):</span>
<ul class="itemizedlist">
 <li class="listitem"><span class="simpara"><strong><code>SplDoublyLinkedList::IT_MODE_DELETE</code></strong> (Elements are deleted by the iterator)</span></li>
 <li class="listitem"><span class="simpara"><strong><code>SplDoublyLinkedList::IT_MODE_KEEP</code></strong> (Elements are traversed by the iterator)</span></li>
</ul>
</li>
</ul>

<p class="para">
The default mode is: <strong><code>SplDoublyLinkedList::IT_MODE_FIFO</code></strong> | <strong><code>SplDoublyLinkedList::IT_MODE_KEEP</code></strong>
</p>
</dd>

---------------------------------

##### SplStack
http://php.net/manual/en/class.splstack.php

<p>The SplStack class provides the main functionalities of a stack implemented using a doubly linked list.</p>

`SplStack extends SplDoublyLinkedList implements Iterator , ArrayAccess , Countable`

<dd>
<p class="para">
There is only one iteration parameter you can modify.
</p>
<ul class="itemizedlist">
<li class="listitem">
<span class="simpara">The behavior of the iterator (either one or the other):</span>
<ul class="itemizedlist">
 <li class="listitem"><span class="simpara">SplDoublyLinkedList::IT_MODE_DELETE (Elements are deleted by the iterator)</span></li>
 <li class="listitem"><span class="simpara">SplDoublyLinkedList::IT_MODE_KEEP (Elements are traversed by the iterator)</span></li>
</ul>
</li>
</ul>

<p class="para">
The default mode is 0x2 : SplDoublyLinkedList::IT_MODE_LIFO | SplDoublyLinkedList::IT_MODE_KEEP
</p>

<div class="warning"><strong class="warning">Warning</strong>
<p class="para">
The direction of iteration can no longer be changed for SplStacks. 
Trying to do so will result in a <a href="class.runtimeexception.php" class="classname">RuntimeException</a> being thrown.
</p>
</div>
</dd>

--------------------------------------------------

##### SplQueue
http://php.net/manual/en/class.splqueue.php

<p>The SplQueue class provides the main functionalities of a queue implemented using a doubly linked list.</p>

`SplQueue extends SplDoublyLinkedList implements Iterator , ArrayAccess , Countable`

<ul class="chunklist chunklist_reference">
    <li>
        <span>SplQueue::__construct</span>
         — Constructs a new queue implemented using a doubly linked list
     </li>
     <li>
        <span>SplQueue::dequeue</span> 
        — Dequeues a node from the queue
    </li>
    <li>
        <span>SplQueue::enqueue</span> 
        — Adds an element to the queue.
    </li>
    <li>
        <span>SplQueue::setIteratorMode</span>
         — Sets the mode of iteration
     </li>
</ul>

---------------------------------------------

##### SplHeap
<p>The SplHeap class provides the main functionalities of a Heap.</p>

<ul class="chunklist chunklist_reference">
    <li>
        <strong>abstract</strong> - <span>SplHeap::compare</span>
        — Compare elements in order to place them correctly in the heap while sifting up.</li>
    <li>
        <span>SplHeap::__construct</span> 
        — Constructs a new empty heap
    </li>
    <li>
        <span>SplHeap::count</span> 
        — Counts the number of elements in the heap.</li>
    <li>
        <span>SplHeap::current</span> 
        — Return current node pointed by the iterator</li>
    <li>
        <span>SplHeap::extract</span> 
        — Extracts a node from top of the heap and sift up.
    </li>
    <li>
        <span>SplHeap::insert</span> 
        — Inserts an element in the heap by sifting it up.</li>
    <li>
        <span>SplHeap::isEmpty</span> 
        — Checks whether the heap is empty.
    </li>
    <li>
        <span>SplHeap::key</span> 
        — Return current node index
    </li>
    <li>
        <span>SplHeap::next</span> 
        — Move to the next node
    </li>
    <li>
        <span>SplHeap::recoverFromCorruption</span> 
        — Recover from the corrupted state and allow further actions on the heap.
    </li>
    <li>
        <span>SplHeap::rewind</span> 
        — Rewind iterator back to the start (no-op)
    </li>
    <li>
        <span>SplHeap::top</span> 
        — Peeks at the node from the top of the heap
    </li>
    <li>
        <span>SplHeap::valid</span>
         — Check whether the heap contains more nodes
     </li>
</ul>

------------------------------------------------------

##### SplMaxHeap
http://php.net/manual/en/class.splmaxheap.php

<p>The SplMaxHeap class provides the main functionalities of a heap, keeping the maximum on the top.</p>

- SplMaxHeap::compare — Compare elements in order to place them correctly in the heap while sifting up.

-------------------------------------------------------

##### SplMinHeap
http://php.net/manual/en/class.splminheap.php

<p>The SplMinHeap class provides the main functionalities of a heap, keeping the minimum on the top. </p>

----------------------------------------------------

##### SplPriorityQueue
http://php.net/manual/en/class.splpriorityqueue.php

<p>The SplPriorityQueue class provides the main functionalities of a prioritized queue, implemented using a max heap</p>

`SplPriorityQueue implements Iterator , Countable`

<ul class="chunklist chunklist_reference">
    <li>
        <span>SplPriorityQueue::compare</span> 
        — Compare priorities in order to place elements correctly in the heap while sifting up.
    </li>
    <li>
        <span>SplPriorityQueue::__construct</span> 
        — Constructs a new empty queue
    </li>
    <li>
        <span>SplPriorityQueue::count</span>
         — Counts the number of elements in the queue.
     </li>
     <li>
        <span>SplPriorityQueue::current</span> 
        — Return current node pointed by the iterator
    </li>
    <li>
        <span>SplPriorityQueue::extract</span> 
        — Extracts a node from top of the heap and shift up.
    </li>
    <li>
        <span>SplPriorityQueue::insert</span> 
        — Inserts an element in the queue by sifting it up.
    </li>
    <li>
        <span>SplPriorityQueue::isEmpty</span> 
        — Checks whether the queue is empty.
    </li>
    <li>
        <span>SplPriorityQueue::key</span> 
        — Return current node index
    </li>
    <li>
        <span>SplPriorityQueue::next</span> 
        — Move to the next node
    </li>
    <li>
        <span>SplPriorityQueue::recoverFromCorruption</span> 
        — Recover from the corrupted state and allow further actions on the queue.
    </li>
    <li>
        <span>SplPriorityQueue::rewind</span> 
        — Rewind iterator back to the start (no-op)
    </li>
    <li>
        <span>SplPriorityQueue::setExtractFlags</span> 
        — Sets the mode of extraction
    </li>
    <li>
        <span>SplPriorityQueue::top</span> 
        — Peeks at the node from the top of the queue
    </li>
    <li>
        <span>SplPriorityQueue::valid</span> 
        — Check whether the queue contains more nodes
    </li>
</ul>
    
`public void SplPriorityQueue::setExtractFlags ( int $flags )`    

<ul class="itemizedlist">
<li class="listitem"><span class="simpara"><strong><code>SplPriorityQueue::EXTR_DATA</code></strong> (0x00000001): Extract the data</span></li>
<li class="listitem"><span class="simpara"><strong><code>SplPriorityQueue::EXTR_PRIORITY</code></strong> (0x00000002): Extract the priority</span></li>
<li class="listitem"><span class="simpara"><strong><code>SplPriorityQueue::EXTR_BOTH</code></strong> (0x00000003): Extract an array containing both</span></li>
</ul>

The default mode is `SplPriorityQueue::EXTR_DATA`.

---------------------------------------

##### SplFixedArray
http://php.net/manual/en/class.splfixedarray.php

##### SplObjectStorage
http://php.net/manual/en/class.splobjectstorage.php

<p>The SplObjectStorage class provides a map from objects to data or, by ignoring data, an object set. This dual purpose can be useful in many cases involving the need to uniquely identify objects.</p>
SplObjectStorage::addAll — Добавляет все объекты из другого контейнера
SplObjectStorage::attach — Добавляет объект в контейнер
SplObjectStorage::contains — Проверяет, содержит ли контейнер заданный объект
SplObjectStorage::count — Возвращает количество объектов в контейнере
SplObjectStorage::current — Возвращает текущий объект
SplObjectStorage::detach — Удаляет объект object из контейнера
SplObjectStorage::getHash — Вычисляет уникальный идентификатор для объектов контейнера
SplObjectStorage::getInfo — Возвращает данные ассоциированные с текущим объектом
SplObjectStorage::key — Возвращает индекс текущего положения итератора
SplObjectStorage::next — Переход к следующему объекту
SplObjectStorage::offsetExists — Проверяет, существует ли объект в контейнере
SplObjectStorage::offsetGet — Возвращает данные ассоциированные с объектом object
SplObjectStorage::offsetSet — Ассоциирует данные с объектом в контейнере
SplObjectStorage::offsetUnset — Удаляет объект из контейнера
SplObjectStorage::removeAll — Удаляет из текущего контейнера объекты, которые есть в другом контейнере
SplObjectStorage::removeAllExcept — Удаляет из текущего контейнера все объекты, которых нет в другом контейнере
SplObjectStorage::rewind — Переводит итератор на первый элемент контейнера
SplObjectStorage::serialize — Сериализует контейнер
SplObjectStorage::setInfo — Ассоциирует данные с текущим объектом контейнера
SplObjectStorage::unserialize — Восстанавливает сериализованый контейнер из строки
SplObjectStorage::valid — Определяет, допустимо ли текущее значение итератора

<hr/>
