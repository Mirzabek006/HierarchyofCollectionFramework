# HierarchyofCollectionFramework
ListandMapandSetandIteratorQuery
Quyidagi kodda:

List

Set

Queue

Map

va ularning asosiy implementatsiyalari ishlatiladi

🔥 1. List (ArrayList, LinkedList)
import java.util.*;

public class ListExample {
    public static void main(String[] args) {

        // ArrayList
        List<String> list = new ArrayList<>();
        list.add("Ali");
        list.add("Vali");
        list.add("Ali"); // duplicate allowed

        System.out.println("ArrayList: " + list);

        // LinkedList
        List<String> linkedList = new LinkedList<>();
        linkedList.add("Java");
        linkedList.add("Spring");

        System.out.println("LinkedList: " + linkedList);
    }
}

📌 Xususiyatlari:

Tartib saqlanadi

Duplicate bo‘lishi mumkin

🔥 2. Set (HashSet, TreeSet)
import java.util.*;

public class SetExample {
    public static void main(String[] args) {

        // HashSet
        Set<String> set = new HashSet<>();
        set.add("Ali");
        set.add("Vali");
        set.add("Ali"); // duplicate ignored

        System.out.println("HashSet: " + set);

        // TreeSet (sorted)
        Set<Integer> treeSet = new TreeSet<>();
        treeSet.add(5);
        treeSet.add(1);
        treeSet.add(3);

        System.out.println("TreeSet: " + treeSet);
    }
}

📌 Xususiyatlari:

Duplicate YO‘Q

TreeSet → sorted

🔥 3. Queue (PriorityQueue)
import java.util.*;

public class QueueExample {
    public static void main(String[] args) {

        Queue<Integer> queue = new PriorityQueue<>();

        queue.add(10);
        queue.add(5);
        queue.add(20);

        System.out.println("Queue: " + queue);

        System.out.println("Remove: " + queue.poll()); // smallest chiqadi
        System.out.println("After remove: " + queue);
    }
}

📌 Xususiyatlari:

FIFO (ba’zida priority asosida ishlaydi)

PriorityQueue → sort qiladi

🔥 4. Deque (ArrayDeque)
import java.util.*;

public class DequeExample {
    public static void main(String[] args) {

        Deque<String> deque = new ArrayDeque<>();

        deque.addFirst("A");
        deque.addLast("B");
        deque.addFirst("C");

        System.out.println("Deque: " + deque);

        deque.removeLast();
        System.out.println("After remove: " + deque);
    }
}

📌 Xususiyatlari:

Ikki tomondan ishlaydi (stack + queue)

🔥 5. Map (HashMap, TreeMap)
import java.util.*;

public class MapExample {
    public static void main(String[] args) {

        // HashMap
        Map<Integer, String> map = new HashMap<>();
        map.put(1, "Ali");
        map.put(2, "Vali");
        map.put(1, "Gani"); // override

        System.out.println("HashMap: " + map);

        // TreeMap (sorted by key)
        Map<Integer, String> treeMap = new TreeMap<>();
        treeMap.put(3, "C");
        treeMap.put(1, "A");
        treeMap.put(2, "B");

        System.out.println("TreeMap: " + treeMap);
    }
}

📌 Xususiyatlari:

Key-Value

TreeMap → sort qiladi

🔥 6. Iterator ishlatish
import java.util.*;

public class IteratorExample {
    public static void main(String[] args) {

        List<String> list = new ArrayList<>();
        list.add("Java");
        list.add("Spring");

        Iterator<String> iterator = list.iterator();

        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
    }
}
🧠 SENIOR LEVEL TUSHUNCHA

👉 Hierarchy qanday ishlaydi:

Iterable → eng yuqori

Collection → List, Set, Queue

Map → alohida (Collection emas!)

💥 REAL PROJECTDA QAYERDA ISHLATILADI
Strukturasi	Qaerda ishlatiladi
List	API response (DTO list)
Set	Unique role/permission
Map	Cache, config
Queue	Task processing
Deque	Logging / history

