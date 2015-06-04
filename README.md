# ScalaC-JNIExample

Steps to build and run:

1) Build Scala code file:

<Linux>
scalac Sample1.scala

2) Build C++ code file:

<Linux>
g++ -sharedlib -O3 \ -I <Path to JNI Header files> \ Sample1.cpp -o libSample1.so

3) Ensure that libSample1.so is in same directory as Scala code file

4) Run Scala Code

<Linux>
scala -Djava.library.path=$(pwd) -cp Sample1 Sample1

