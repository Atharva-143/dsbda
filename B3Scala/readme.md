AIM:
To write and execute a simple Scala program using Apache Spark framework for performing addition of numbers.

DESCRIPTION:
Apache Spark is a fast distributed data processing framework used for big data analytics. Spark applications are commonly written using Scala programming language. In this practical, a simple Spark program is executed using Spark Shell to perform addition of numbers.

The program creates a distributed dataset using Spark RDD and calculates the sum of all elements using the reduce() operation.

PROGRAM:

val numbers = sc.parallelize(Array(10, 20, 30, 40))

val sum = numbers.reduce(_ + _)

println("Sum = " + sum)

OUTPUT:
Sum = 100

WORKING OF PROGRAM:

1. Spark Shell:
   The program is executed inside Spark Shell using Scala language.

Command used:
spark-shell

2. Creating RDD:
   The following statement creates a distributed dataset called RDD:

val numbers = sc.parallelize(Array(10, 20, 30, 40))

Here:

* sc → Spark Context
* parallelize() → converts array into distributed dataset
* Array(10,20,30,40) → input data

3. Reduce Operation:
   The reduce() function performs addition on all elements.

val sum = numbers.reduce(_ + _)

Working:
10 + 20 + 30 + 40 = 100

4. Display Output:
   The result is displayed using println() function.

println("Sum = " + sum)

COMMANDS USED:

1. Open Spark Shell
   spark-shell

2. Execute Scala Program

val numbers = sc.parallelize(Array(10, 20, 30, 40))

val sum = numbers.reduce(_ + _)

println("Sum = " + sum)

VIVA QUESTIONS AND ANSWERS:

Q1. What is Apache Spark?
Apache Spark is a fast distributed big-data processing framework.

Q2. What is Scala?
Scala is a programming language used for Spark applications.

Q3. What is Spark Shell?
Spark Shell is an interactive environment used to execute Scala programs in Apache Spark.

Q4. What is RDD?
RDD stands for Resilient Distributed Dataset.
It is the basic data structure in Spark.

Q5. What does parallelize() do?
It converts a collection or array into distributed dataset (RDD).

Q6. What does reduce() do?
It combines all elements of RDD into a single value.

Q7. What is the role of Spark Context (sc)?
Spark Context is used to interact with Spark cluster and create RDDs.

Q8. Why is Spark faster than Hadoop?
Spark performs in-memory processing, which makes it faster.

Q9. What is the output of this program?
Sum = 100

Q10. Is Spark a distributed framework?
Yes, Spark processes data in distributed manner across multiple systems.

CONCLUSION:
The simple Scala program using Apache Spark framework was successfully executed and the addition of numbers was performed using RDD and reduce() operation.
