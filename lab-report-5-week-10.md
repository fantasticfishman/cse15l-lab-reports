# Lab Report 5

## Finding tests

- To find these tests, I ran the the bash script we were provided with on both the provided MarkdownParse repository and as well as my own MarkdownParse repository. I then used output redirection with `bash script.sh > results.txt` when running that script to redirect those outputs to two result.txt files. I then ran `diff mdparseweek9/results.txt mymdparseweek9/results.txt` , to compare those two result files.

## Test 1

- For this test, the provided implementation(bottom) provides a blank array, and my implementation(top) states that there is an invalid input, and returns null.

  ![Image](/week10/diff.png)

- I think that the provided implementation is "correct", because this test file should not return a link. The test file contains `[link](/url "title "and" title")`, which should not be a link, as you can see.

  ![Image](/week10/expect.png)

- While my implementation recognizes that a link is not found, you could consider this "correct", but it terminates the program right there and returns null. I think that returning a blank array would be better, because it leaves open the possibility for more links.

- The bug in my implementation is that I terminate the program immediately if any of the open/closed brackets/parenthases are not found in their respective orders, which is a good temporary solution, but terminates the program if none of them are found. If there is an actual working link after the error, it will not be found.

  ![Image](/week10/bug.png)

## Test 2

- For this test, the provided implementation(bottom) provides an empty array, and my implementation(top) states that there is an invalid input, and returns null.

  ![Image](/week10/diff1.png)

- I think that the neither implementation is correct, because this test file should return a link. The test file contains `<localhost:5001/foo>`, which Visual Studio Code seems to consider as a link. Commonmark does the same. Notice how the one in angled brackets is blue while the other is not.

  ![Image](/week10/expect1.png)
  ![Image](/week10/expect2.png)

- The bug in my implementation is that I do not consider the possibility of this type of link, which is just a link contained in angled brackets, which seems to be another valid way to have a link. I am searching for parenthases/square brackets, which are not found.

  ![Image](/week10/bug.png)
