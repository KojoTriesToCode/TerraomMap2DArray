# 1DArrays 

### Ways to declare them:

Integer Arrays 

```java
int [] myArray = new int[10]; 

int[] map; //declared, but not initialized (don't know the size of it) 

int[] terrain;
terrain = new int[100]; 
```

Object 

```java 
String[] myString = new String[10]; 
Player[] players = new Student[100]; 
Student students[] = new Student[1000]; 
```

Array Initializers 

```java
int a[] = {3,4,5,6,7,1,4,6,8}; 
```

### Accessing Elements 

- Elements start at 0 and go to length-1 

```java 
int a[] = new int[10]; 
String b[] = new String[100]; 
Student c[] = new Student[1000]; 

System.out.println(a.length); 
System.out.println(b.length);
System.out.println(c.length);

Output 

10
100
1000

//access the 20th element 
int temp1 = a[20]; 
String temp2 = b[20];
Student temp3 = c[20]; 
```

### Replacing(change) Array Elements 
```java 
int a[] = new int[10]; 
String b[] = new String[100]; 
Student c[] = new Student[1000];

//chnage the 5th element 
a[5] = 10; 
b[5] = "Hello";  
c[5] = new Student("John Doe"); 
```

### For loop through an Array

```java 
int a[] = new int[10]; 

for(int i=0; i < a.length; i++) {
    int temp = a[i]; //current element  
}

//identical to loop above
for(int temp: a) {

}
```

- Two things to know about for-each looping 
- There is no i...so you never know WHERE you are
- No changing the structure of the array 

Example: Find the highest GPA student in an array of Students 

- Side notes: capital letters are name of objects and other methods
- Lower case letters are the actual names of an array 
```java 
public Student bestGPA(Student[] students) {
    //max algorithim 
    int currentMax = 0; 
    for (int i=0; i < students.length; i++){
        Student temp = students[i]; 
        if(temp.getGpa() > students[currentMax].getGPA()) {
            currentMax = i; 
        }
    }
    return stduents[currentMax]; 
}

//or 

public Student bestGPA(Student[] students) {
    //max algorithim
    Student currentMax = students[0]; 
    for (int i=0; i < students.length; i++){
        Student temp = students[i]; 
        if(temp.getGpa() > currentMax.getGPA()) {
            currentMax = temp; 
        }
    }
    return currentMax; 
}
```

Example: Do all students have above a 2.0 

```java 
public boolean allAbove2(Student[] arr){
    for(int i=0; i < arr.length; i++) {
        Student curr = arr[i]; 
        if(curr.getGPA() < 2.0)
            return false; 
    }
    return true; 
}

//or 

public boolean allAbove2(Student[] arr){
    for(Student s: arr) 
        if(s.getGPA() < 2.0)
            return false; 
    }
    return true; 
} 
```

# ArrayLists

- Why have ArrayLists?
- When you don't know the size of the array needed

### Declaring ArrayLists
```java 
ArrayList<Student> list = new ArrayList<>();
ArrayList<Student> list2 = new ArrayList<Student>(); 
List<Student> list3 = new ArrayList<>(); 
list<Student> lsit4 = new ArrayList<Student>(); 

//use wrapper classes to create 
ArrayList<Integer> list = new ArrayList<>();
ArrayList<Double> list = new ArrayList<>();
ArrayList<Boolean> list = new ArrayList<>();
```

### Accessing Elements 
```java 
List<Student> list3 = new ArrayList<>(); 

//get the 7th student 
Student temp = list3.get(7); 
```

How many things are in the ArrayList 

```java 
List<Student> list3 = new ArrayList<>();

System.out.println(list3.size());
```

Output 

??? The number of items in the list 

### Change an element in the ArrayList

```java 
Lisr<Student> list3 = new ArrayList<>(); 

//change student 3's name to "Jason"

list3.get(3).setName("Jason"); 





