WELCOME
--------------------------------------------------------------------------------
Congratulations, you opened the README.txt file! You're well on your way to
becoming a command line ninja.

WHAT IS THIS?
--------------------------------------------------------------------------------
This is a set of challenges designed to help Linux newbies learn to use the
command line. Each challenge prompts the student to learn a new command or
concept about using the command line. Some challenges have multiple solutions,
while others are more rigid.

PHILOSOPHY
--------------------------------------------------------------------------------
The world of technology changes daily. Throughout your career as a developer,
admin, consultant, or other IT professional, you will often have to learn new
skills, concepts, tools, and technologies. For the most part, no one is going to
teach these things to you; it's up to you to learn them on your own.

The philosophy of these challenges is to guide the student through the process
of learning the command line on their own. Therefore, there is no answer key
for these challenges.

DON'T PANIC!
--------------------------------------------------------------------------------
Before we get started, here are some words of encouragement: If you're new
to Linux, don't be scared away by these challenges. Some of them are HARD. Don't
give up, don't get discouraged, and, above all, don't panic.

Don't feel like you have to solve all of these challenges in one sitting (or
even one year). Many of these challenges will become obvious after you've spent
some time using the command line on a regular basis, so don't try to force it.
Solve the challenges that you can and research the ones that you can't. Get
together with your friends and try to work them out as a team.

INSTRUCTIONS
--------------------------------------------------------------------------------

1. Unless otherwise noted, all challenges can be completed by submitting only 1
entry on the command line. That is to say, you will type something on the command
line and press the <ENTER> key exactly once. Writing a script and executing it
does not count.

2. You may use any resources at your disposal to solve the challenges including
friends or even Google. I would recommend, however, that you not simply google
everything, but spend some time reading some books or articles for beginners.
Furthermore, try and use the man pages instead of Google when you can. You get
out of this what you put into it.

When you complete a challenge, take the opportunity to learn more about the
tools you used. If you learn a new command to complete a challenge, read
through its man page. Many of the same commands are used in different ways
throughout these challenges, so a little investment early on will make later
challenges easier.

3. Most challenges have more than one solution. You get "bonus points" for
solving challenges in multiple ways.

4. Some challenges stand alone, while others rely on challenges that came before
them.

5. Challenges are labeled "B" for beginner, "I" for intermediate, and "A" for
advanced.

6. All challenges assume you are using the Bourne Again Shell (bash).

CHALLENGES
--------------------------------------------------------------------------------

OK! Let's get started.

1. (B) Extract the "challenges.tar.gz" archive; you'll need its contents to
   solve some of the challenges.
   
   ***tar -xf challenges.tar.gz***

2. (B) Change your working directory to the "challenges" directory that was created when you extracted "challenges.tar.gz".

    ***cd challenges/***

3. (B) List the contents of the "challenges" directory.

    ***ls***

4. (B) Create a new directory named "foo".

    ***mkdir foo***

5. (I) Create a new directory named "foo/bar/1/2/3"

    ***mkdir -p foo/bar/1/2/3***

6. (B) Remove the directory "foo" and all of its contents

    ***rm -R foo***

7. (B) Print the text "Hello World".

    ***echo "Hello World"***
8. (B) Create a file named "hello.txt" that contains the text "Hello World".

    ***echo "Hello World" > hello.txt***

9. (B) Create an empty file named "empty.txt"

    ***touch empty.txt***
10. (B) Remove the file "empty.txt"

    ***rm empty.txt***

11. (I) Find a second way to solve challenge 9.
    
    ***cat > empty.txt***

12. (I) Find a third way to solve challenge 9.

    ***echo -n > empty.txt***
13. (B) Copy "hello.txt" and name the copy "goodbye.txt".

    ***cp hello.txt goodbye.txt***

14. (B) Rename "goodbye.txt" to "hello_copy.txt".

    ***mv goodbye.txt hello_copy.txt***
15. (I) Prove that the contents of "hello.txt" and "hello_copy.txt" are
    identical.

    ***diff -s hello.txt hello_copy.txt***
16. (B) Concatenate the contents of "hello.txt" and "hello_copy.txt" and store
    the result in a file named "2_hellos.txt".

    ***cat hello.txt hello_copy.txt > 2_hellos.txt***
17. (B) Get the full path of your present working directory ("challenges").

    ***pwd***
18. (B) List the contents of the "challenges" directory (like challenge 3), but
    show the permissions for each file.

    ***ls -l***

19. (B) Append some text to the end of "restricted.txt". It's OK to do this in
    2 steps.

    ***chmod 600 restricted.txt***

    ***echo "end line" >> restricted.txt***
20. (B) Run the "hello_executable" program.
    
    ***./hello_executable***
21. (B) Run the "challenge_20" program. It's OK to do this in 2 steps.

    ***chmod 700 challenge_20***

    ***./challenge_20***

22. (B) Compile and run "compile_me.c". It's OK to do this in 2 steps.

    ***gcc compile_me.c***

    ***./a.out***

23. (A) Run the "redirect" program and collect all of its output in a file
    named "output.txt".

    ***./redirect > output.txt***

24. (B) Get the current date and time.

    ***date***

25. (B) Show all of the running processes on your computer.

    ***top***

26. (B) Show the number of processors/cores in your computer.

    ***nproc***

27. (B) Find out what version of the Linux kernel is currently running.

    ***uname -r***

28. (B) Find the file in the "bunch_of_files/" directory that contains the string:
    "You found the needle in the haystack!"

    ***cd bunch_of_files/***

    ***grep -r "You found the needle in the haystack!"***
29. (B) Print the first 25 lines of people.csv.

    ***head -n 25 people.csv***
30. (B) Print the last 25 lines of people.csv.

    ***tail -n 25 people.csv***
31. (I) Display just the differences between greeting1.txt and greeting2.txt

    ***diff greeting1.txt greeting2.txt***

32. (I) Print "Hello", then wait 5 seconds, then print "world!".

    ***echo "Hello" && sleep 5 && echo "world!"***

33. (I) Create a 1MB file full of zeros.

    ***dd if=/dev/zero bs=1024 count=1024 > 1_mb***

34. (I) Create a 2MB file full of random data.

    ***dd if=/dev/urandom of=random_file bs=2048 count=1000***

35. (I) Count the number of lines in README.txt.

    ***wc -l README.md***
36. (B) Display the contents of README.txt in reverse (last line first).

    ***tac README.md***

37. (I) Display all of the last names in people.csv.

    ***head people.csv***

38. (A) Count the number of unique last names in people.csv.

    ***cut -d , -f 2 people.csv | sort | uniq |wc -l***

39. (A) Did you accidentally count the CSV header in the previous challenge?

    ***tail +2 people.csv | cut -d , -f 2 | sort | uniq |wc -l***

40. (A) There's a second way to exclude the CSV header from your count. Find it.

    ***sed 1d people.csv | cut -d , -f 2 | sort -u | wc -l***

41. (A) Now that you've found two ways to correctly count the number of unique
    last names in people.csv, can you prove whether or not one is more efficient
    (faster) than the other?

    ***time tail +2 people.csv | cut -d , -f 2 | sort | uniq |wc -l***

    ***time sed 1d people.csv | cut -d , -f 2 | sort -u | wc -l***


42. (A) Count the number of people with the first name "Josiah" in people.csv.

    ***cut -d , -f 4 people.csv | sort | uniq -c |grep "Josiah"***

43. (I) Count the number of files (not directories) in the "challenges" directory .
    
    ***ls -l | grep "^_" | wc -l***

    ***ls -lR | grep "^_" | wc -l***

44. (I) Count the number of subdirectories in the "challenges" directory.

    ***ls -lR | grep "^d" | wc -l***

45. (I) Remove all files with "deleteme" in the name.

    ***find . -type f -name "\*deleteme\*" -exec rm -v {} \\;***

46. (I) In challenge 28 you found a file. Replace the string "You found the
    needle in the haystack!" with "The needle has been removed."

    ***grep -lr "You found the needle in the haystack!"***

47. (A) Transform people.csv from ',' delimited to '|' delimited and save the result in people_pipe.csv.

    ***cat people.csv | tr "," "|" > people_pipe.csv***

48. (A) Find all of the files in "bunch_of_files/" that are duplicates of "file001.rand".

49. (A) Execute this challenge in exactly 2 steps

    1) (B) Create an empty file named "supercalifragilisticexpialidocious.txt".
    2) (A) Remove "supercalifragilisticexpialidocious.txt". Your command may
           only use a maximum 5 total characters (no wildcards or globs).

50. (A) Create a set of empty files. Each file has a name in the form "L-N.txt"
    where L is a letter and N is a number. Valid letters are a,b,c, while valid
    numbers are 1,2,3. Create all permutations (total of 9 files). Make your
    command as short as possible. I can do it in 25 characters, can you do
    better?

BONUS: Create a challenge of your own and ask a friend to complete it.

Congratulations! You've completed all of the challenges. If you haven't
already, go back through and find different ways to do some of the challenges.
Compare notes with a friend!
