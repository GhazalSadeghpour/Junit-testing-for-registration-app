# Junit-testing-for-registration-app
This repository contains the code for the Junit tests written for a given registration web application.
First thing I did was testing to make sure all the code compiles and runs without any error.
note: I used Java 16 and Junit 5 (on a windows 10)

To compile the application

    javac -encoding UTF-8 --source-path src -d dist src/*.java
    
To Compile the tests

    javac -encoding UTF-8 --source-path test -d dist -cp lib/junit-platform-console-standalone-1.7.1.jar test/*.java src/*.java

To run the application.

    java --add-opens java.base/java.lang=ALL-UNNAMED -jar  user-registration-app-0.1.0.jar
    
 To run the tests:
 
    java -jar lib/junit-platform-console-standalone-1.7.1.jar --class-path dist --scan-class-path
     
     
View of running the app:
![image](https://user-images.githubusercontent.com/64787873/119402530-10125b00-bcab-11eb-97ca-6f0af0f3f00c.png)

View of opening the app in   http://localhost:8080/

![image](https://user-images.githubusercontent.com/64787873/119401184-261f1c00-bca9-11eb-8e22-46e7b9120815.png)

view of running the tests
![image](https://user-images.githubusercontent.com/64787873/119403245-06d5be00-bcac-11eb-94e8-c626593e6b06.png)




## Exercise 1:
for this part of the lab, I used the test cases given in tutorial and by manually running the tests on the application, I have noted the results in the following table.

Test Case |  Expected Results             | Actual Results                   | Verdict(Pass, Fail, Inconclusive)
----------|-------------------------------|----------------------------------|----------------------------------
1         | registration request accepted | registration request accepted    | Pass
2         | registration request accepted | registration request accepted    | Pass
3         | registration request accepted | registration request accepted    | Pass
4         | registration request accepted | registration request accepted    | Pass
5         | Err1                          | Err1 and Err3                    | Fail
6         | Err3                          | Err1 and Err3  and Err6          | Fail
7         | Err3                          | Err3                             | Pass
8         | Err1                          | Err1                             | Pass


Test 1 and the result
![image](https://user-images.githubusercontent.com/64787873/119403761-d8a4ae00-bcac-11eb-934b-bbc3b4c728a2.png)


Test 2 and the result
![image](https://user-images.githubusercontent.com/64787873/119403876-04279880-bcad-11eb-842b-63f553004e68.png)

Test 3 and the result
![image](https://user-images.githubusercontent.com/64787873/119403940-199cc280-bcad-11eb-9a64-654a9f68ea6f.png)

Test 4 and the result
![image](https://user-images.githubusercontent.com/64787873/119404043-3e913580-bcad-11eb-8206-a8976d6680ab.png)

Test 5 and the result

![image](https://user-images.githubusercontent.com/64787873/119404075-4b158e00-bcad-11eb-8c33-f54134b79e5e.png)

Test 6 and the result

![image](https://user-images.githubusercontent.com/64787873/119404103-57015000-bcad-11eb-8905-179e4df4a88e.png)

Test 7 and the result

![image](https://user-images.githubusercontent.com/64787873/119404141-65e80280-bcad-11eb-8400-ee694a068a1b.png)


Test 8 and the result
![image](https://user-images.githubusercontent.com/64787873/119404159-6c767a00-bcad-11eb-8919-567ced7b77c9.png)


Note: I used the error table given in the tutorial 

![image](https://user-images.githubusercontent.com/64787873/119403085-d0983e80-bcab-11eb-9c6a-c99c8b35d0dd.png)



## Exercise 2:
For the tests, I have used Junit 5.
command used for compiling the tests: 

        javac -encoding UTF-8 --source-path test -d dist -cp lib/junit-platform-console-standalone-1.7.1.jar test/*.java src/*.java
        
command used for running the tests:

        java -jar lib/junit-platform-console-standalone-1.7.1.jar --class-path dist --scan-class-path           

For this part, I have started with implementing all the test cases (given in tutorial) as explicit Junit tests in the DateTest.java file.

### Explicit tests: 

Compiling the tests:
    ![image](https://user-images.githubusercontent.com/64787873/119585369-8e98f680-bd98-11eb-9f08-3a3076070d27.png)
Running the tests:
![image](https://user-images.githubusercontent.com/64787873/119585241-4ed20f00-bd98-11eb-990d-cd7a059bd127.png)
![image](https://user-images.githubusercontent.com/64787873/119585299-6c06dd80-bd98-11eb-8581-6b898a342acf.png)

 ### Parameterized tests
 
 for this part of the lab, first I wrote the tests for the DateNextDateOkTest test suite.
 
 Result of running the tests
 ![image](https://user-images.githubusercontent.com/64787873/119597484-1ab61880-bdaf-11eb-90b2-12ef4c1d041b.png)

Then, I wrote the tests in the DateNextDateExceptionTest test suite.

Result of running the tests
![image](https://user-images.githubusercontent.com/64787873/119599137-67e7b980-bdb2-11eb-8885-b64ccd6782a1.png)



Overall view of compiling and running all explicit and parameterized tests:
![image](https://user-images.githubusercontent.com/64787873/119599455-083dde00-bdb3-11eb-8a5e-b49417687690.png)
![image](https://user-images.githubusercontent.com/64787873/119599608-5e128600-bdb3-11eb-99d2-5a5adadb3960.png)
![image](https://user-images.githubusercontent.com/64787873/119599588-4cc97980-bdb3-11eb-9c02-c74be4f9d661.png)


