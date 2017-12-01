import java.util.Collection;

import java.util.HashSet;

import java.util.Iterator;

import java.util.Set;
 
public class HashSetImpl<E>

{

    private Set<E> hashSet;
 
    public HashSetImpl()
    
    {

        hashSet = new HashSet<E>();

    }
 
   
    public HashSetImpl(Collection<? extends E> c)
    {
        hashSet = new HashSet<E>(c);
    }
 
    public HashSetImpl(int initialCapacity, float loadFactor)
    
    {
        
        hashSet = new HashSet<E>(initialCapacity, loadFactor);

    }
 
    
    public HashSetImpl(int initialCapacity)

    {

        hashSet = new HashSet<E>(initialCapacity);

    }
 
    
    public boolean add(E eobj)

    {

        return hashSet.add(eobj);

    }
 
    

    public boolean contains(Object obj)

    {

        return hashSet.contains(obj);

    }
 
    

    public boolean isEmpty()

    {

        return hashSet.isEmpty();

    }
 
    /* returns an iterator over the elements in the set */

    public Iterator<E> iterator()

    {

        return hashSet.iterator();

    }
 
    /* removes the specified element from this set if present */

    public boolean remove(Object obj)

    {

        return hashSet.remove(obj);

    }
 
    /* returns the number of elements in set */

    public int size()

    {

        return hashSet.size();

    }
 
    /* removes all elements from this set */

    public void clear()

    {

        hashSet.clear();

    }
 
    /* Returns an array containing all of the elements in this set. */

    public Object[] toArray()

    {

        return hashSet.toArray();

    }

  

    public boolean addAll(Collection<? extends E> c)  

      throws UnsupportedOperationException, ClassCastException,NullPointerException,IllegalArgumentException      

    {

        return hashSet.addAll(c);

    }
 
    

    public boolean retainAll(Collection<?> c)

      throws UnsupportedOperationException, ClassCastException,NullPointerException

   {

        return hashSet.retainAll(c);

    }

    public boolean removeAll(Collection<?> c)

      throws UnsupportedOperationException, NullPointerException,ClassCastException

    {

        return hashSet.retainAll(c);

    }
 
    

    public <T> T[] toArray(T[] a)

      throws ArrayStoreException,NullPointerException

    {

        return hashSet.toArray(a);

    }
 
    public static void main(String... arg)

    {

        HashSet<Integer> hashSet = new HashSet<Integer>();

        if (hashSet.add(10))

            System.out.println("element 10 added");

        if (hashSet.add(20))

            System.out.println("element 20 added");

        if (hashSet.add(30))

            System.out.println("element 30 added");
 
        System.out.println("the size of set is " + hashSet.size());
 
        if (hashSet.contains(40))

            System.out.println("set contains 40");

        else

            System.out.println("set does not contain 40");
 
        if (hashSet.remove(20))

            System.out.println("element 20 removed");

        else

            System.out.println("element 20 not removed");
 
        System.out.println("the element of set are");

        Iterator<Integer> iterator = hashSet.iterator();

        while (iterator.hasNext())

        {

            System.out.print(iterator.next() + "\t");

        }

        System.out.println();
 
        Set<Integer> removedSet = new HashSet<Integer>();

        removedSet.add(10);

        removedSet.add(20);
 
        System.out.println("the elements after removing");

        hashSet.removeAll(removedSet);

        Iterator<Integer> riterator = hashSet.iterator();

        while(riterator.hasNext())

        {

            System.out.print(riterator.next() + "\t");

        }

        System.out.println();
 
        hashSet.clear();

        System.out.println("hashSet cleared");

        if (hashSet.isEmpty())

            System.out.println("hashSet is empty");

        else

            System.out.println("hashSet is not empty");

    }

}

