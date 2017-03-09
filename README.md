# 9.1


Give a brief answer to the questions below:

1.Why MapReduce program is needed in Pig Programming?

2.What are advantages of pig over MapReduce?

3.What is pig engine and what is its importance?

4.What are the modes of Pig execution?

5.What is grunt shell in Pig?

6.What are the features of Pig Latin language?

7.Is Pig latin commands case sensitive?

8.What is a data flow language? 





Q1.Why MapReduce program is needed in Pig Programming?

Pig Latin is Pig's language that allows developers to sort, join, parse, transform and calculate unstructured and semi-structured data in MapReduce all while using a language similar to SQL versus Java. Pig is an application that works on top of MapReduce, Yarn or Tez. Pig is written in Java and compiles Pig Latin scripts into to MapReduce jobs. Pig is a compiler that takes Pig Latin scripts and transforms them into Java. This is why Mapreduce is needed in Pig Programming.



Q2.What are advantages of pig over MapReduce?

Advantages

1.Decrease in development time. This is the biggest advantage especially considering vanilla map-reduce jobs' complexity, time-spent and maintenance of the programs.

2.Learning curve is not steep, anyone who does not know how to write vanilla map-reduce or SQL for that matter could pick up and can write map-reduce jobs; not easy to master, though.

3.Procedural, not declarative unlike SQL, so easier to follow the commands and provides better expressiveness in the transformation of data every step. Comparing to vanilla map-reduce, it is much more like an english language. It is concise and unlike Java but more like Python.
I really liked the idea of dataflow where everything is about data even though we sacrifice control structures like for loop or if structures. This enforces the developer to think about the data but nothing else. In Python or Java, you create the control structures(for loop and ifs) and get the data transformation as a side effect. In here, data and because of data, data transformation is a first class citizen. Without data, you cannot create for loops, you need to always transform and manipulate data. But if you are not transforming data, what are you doing in the very first place?
Since it is procedural, you could control of the execution of every step. If you want to write your own UDF(User Defined Function) and inject in one specific part in the pipeline, it is straightforward.
Speaking of UDFs, you could write your UDFs in Python thanks to Jython. How awesome is that!
Lazy evaluation: unless you do not produce an output file or does not output any message, it does not get evaluated. This has an advantage in the logical plan, it could optimize the program beginning to end and optimizer could produce an efficient plan to execute.
Enjoys everything that Hadoop offers, parallelization, fault-tolerancy with many relational database features.
It is quite effective for unstructured and messy large datasets. Actually, Pig is one of the best tool to make the large unstructured data to structured.
You have UDFs which you want to parallellize and utilize for large amounts of data, then you are in luck. Use Pig as a base pipeline where it does the hard work and you just apply your UDF in the step that you want.
