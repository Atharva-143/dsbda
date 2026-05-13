AIM

To implement a simple WordCount application using Hadoop MapReduce framework in Java.

WHAT THIS PRACTICAL DOES

Input text:

hello world
hello hadoop
big data hadoop

Output:

big 1
data 1
hadoop 2
hello 2
world 1

Counts how many times each word appears.

HADOOP CONCEPT

Hadoop works using:

Mapper + Reducer
1. MAPPER

Mapper reads input line by line.

It breaks sentence into words.

Then outputs:

(word, 1)

Example:

Input:

hello world hello

Mapper output:

hello 1
world 1
hello 1
2. REDUCER

Reducer receives same words together.

Then adds counts.

Example:

Input to reducer:

hello 1
hello 1
world 1

Reducer output:

hello 2
world 1
CODE EXPLANATION
IMPORT STATEMENTS
import java.io.IOException;
import java.util.StringTokenizer;
Explanation:
IOException
→ handles file errors
StringTokenizer
→ splits sentence into words
HADOOP IMPORTS
import org.apache.hadoop.conf.Configuration;
Explanation:

Used for Hadoop configuration settings.

import org.apache.hadoop.fs.Path;
Explanation:

Represents input/output file paths.

import org.apache.hadoop.io.IntWritable;
import org.apache.hadoop.io.Text;
Explanation:

Hadoop datatypes:

Text → string
IntWritable → integer
import org.apache.hadoop.mapreduce.Mapper;
import org.apache.hadoop.mapreduce.Reducer;
Explanation:

Used to create:

Mapper class
Reducer class
MAIN CLASS
public class WordCount

Main program class.

MAPPER CLASS
public static class TokenizerMapper

Creates mapper.

MAP FUNCTION
public void map(...)

Main mapper function.

Reads input and processes words.

STRING TOKENIZER
StringTokenizer itr = new StringTokenizer(value.toString());

Splits line into individual words.

CONTEXT.WRITE
context.write(word, one);

Outputs:

(word,1)
REDUCER CLASS
public static class IntSumReducer

Reducer class used for summation.

REDUCE FUNCTION
public void reduce(...)

Receives grouped words and counts.

SUM COUNTS
sum += val.get();

Adds occurrences of same word.

FINAL OUTPUT
context.write(key, result);

Writes final word count.

MAIN METHOD
public static void main(String[] args)

Program execution starts here.

CREATE JOB
Job job = Job.getInstance(conf, "word count");

Creates Hadoop job.

SET MAPPER
job.setMapperClass(TokenizerMapper.class);

Assigns mapper class.

SET REDUCER
job.setReducerClass(IntSumReducer.class);

Assigns reducer class.

INPUT PATH
FileInputFormat.addInputPath(job, new Path(args[0]));

Input folder path.

OUTPUT PATH
FileOutputFormat.setOutputPath(job, new Path(args[1]));

Output folder path.

COMMAND EXPLANATION
COMPILE
javac -classpath $(hadoop classpath) -d wordcount_classes WordCount.java
Explanation:

Compiles Java Hadoop code.

CREATE JAR
jar -cvf wordcount.jar -C wordcount_classes/ .
Explanation:

Creates executable Hadoop jar file.

RUN HADOOP JOB
hadoop jar wordcount.jar WordCount input output
Explanation:

Runs WordCount MapReduce program.

DISPLAY OUTPUT
cat output/part-r-00000
Explanation:

Shows final output file.

VERY IMPORTANT VIVA QUESTIONS
What is Hadoop?

Hadoop is an open-source framework used for distributed storage and processing of big data.

What is MapReduce?

Programming model used in Hadoop for processing large datasets.

What is Mapper?

Mapper processes input data and generates key-value pairs.

What is Reducer?

Reducer combines values having same key and produces final output.

Why WordCount is used?

It is the basic Hadoop MapReduce example used to count frequency of words.

What is Input Split?

Hadoop divides large input file into smaller blocks for parallel processing.

What is HDFS?

Hadoop Distributed File System used for storing large data across multiple machines.

What is Key-Value Pair?

Data format used in MapReduce.

Example:

hello → 1
Why use JAR file?

Hadoop executes programs through jar files.

Difference between Mapper and Reducer?
Mapper	Reducer
Generates key-value pairs	Combines values
Processes input	Produces final output
MOST IMPORTANT ONE-LINE FLOW
Input → Mapper → Shuffle/Sort → Reducer → Output

This line alone is extremely important for viva.
