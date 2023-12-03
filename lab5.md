# Part 1:

<img width="1213" alt="Screenshot 2023-12-03 at 3 10 24 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/ed57b407-2b33-4ede-a52f-f6ad4c21c8f1">


When I run the this specific repository to check my grader it does not do what it is supposed to do which is catch the compile error. It looks like it is calculating the grade like if there was no compile error at all. What can I do to fix this error?

This is my Code:

<img width="869" alt="Screenshot 2023-12-03 at 3 12 18 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/ceea60a2-a376-4bd7-96c1-dc499efae293">

<img width="796" alt="Screenshot 2023-12-03 at 3 13 00 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/7a3e466f-396e-4728-a2f0-98d1e5ba5417">


# Part 2

It seems there might be an issue with the compilation check in your script. Take a closer look at the section containing 'if [ $? -ne 0 ]; then.' Consider what the condition is checking and how it relates to the compilation process. 

# Part 3

Changes made to the code:

<img width="766" alt="Screenshot 2023-12-03 at 3 23 17 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/819776c2-7dc2-442d-bf07-ff0e4ffe655c">


Output of the code after change:
<img width="1217" alt="Screenshot 2023-12-03 at 3 22 45 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/3df5dfd9-a9f8-4093-b5c7-a1f15fc66275">

Response:
After rectifying the issues in my code, particularly the use of 'if [ $? -ne 0 ];', which essentially checks for a compilation error and proceeds to execute the subsequent code even in the presence of an error, I've revised the logic to promptly echo a compilation error message and exit the script.

# Part 4

1.

The repository I am using: `https://github.com/CalKong/grader-review-CalKong`

My working directory: `/Users/vincenthuynh/grader-review-CalKong`

The file I am using: grade.sh

2. 

The contents of each file before change:

#### Grade.sh:
<img width="869" alt="Screenshot 2023-12-03 at 3 12 18 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/ceea60a2-a376-4bd7-96c1-dc499efae293">

<img width="796" alt="Screenshot 2023-12-03 at 3 13 00 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/7a3e466f-396e-4728-a2f0-98d1e5ba5417">

#### GraderServer.java

<img width="815" alt="Screenshot 2023-12-03 at 3 40 33 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/b859cce4-3e5c-4246-91e0-6b78d1bb5070">

<img width="886" alt="Screenshot 2023-12-03 at 3 40 58 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/562a20c8-9e57-4062-92ab-f1fcb34afbc7">

<img width="870" alt="Screenshot 2023-12-03 at 3 41 12 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/2fcd8803-e76f-4e0c-88ab-319f45568e73">

#### TestExamples.java

<img width="791" alt="Screenshot 2023-12-03 at 3 43 45 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/7eb8ea97-462f-4a30-98ad-1f4f29c504c7">

<img width="904" alt="Screenshot 2023-12-03 at 3 44 00 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/641484b4-7b2e-4799-8eb8-944832e197dc">

### Server.java

<img width="770" alt="Screenshot 2023-12-03 at 3 44 22 PM" src="https://github.com/VincentHuynh1016/Lab-Report-5/assets/114731503/c50ccd69-03a9-42bd-b55a-448307c2a903">

3. 

- `git clone https://github.com/CalKong/grader-review-CalKong`
- `cd grader-review-CalKong`
- `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-compile-error`

4. 
I am already in the correct directory : `/Users/vincenthuynh/grader-review-CalKong`

- `cat grade.sh` (I am looking at the code to see if there are any errors)
- `vim grade.sh` (I found my error so now I want to fix it)
- Clicked the `I` key so that I can delete and type in the new code: changed 'if [ $? -ne 0 ];', to 'if [ $? -eq 0 ];'
- Typed in: `<:wq>` to save
- `bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-compile-error` (Ran the bash again to check if the error was fixed)

# Reflection:


