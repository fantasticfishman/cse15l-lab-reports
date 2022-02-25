# Lab Report 4

## Repositories

- The link to my repository is here.
- The link to the repository I'm reviewing is here.

## Snippet 1

- It should produce this link: `google.com. This is the only one that appears as a link in commonmark.
  ![Image](/week8/snippet1.png)
- This is how I turned it into a test in my implementation- it is testsnippet1.
  ![Image](/week8/my1.png)
- This is the output, my tests did not pass, and these are the JUnit outputs for the test failures. The failing test is testsnippet1.
  ![Image](/week8/my2.png)
- For the implementation that I reviewed, this is the output when running the tests- The failing test is testsnippet1.
  ![Image](/week8/other2.png)

## Snippet 2

- It should produce these 3 links: a.com, a.com(()), and example.com. These all appear as blue links in commonmark.
  ![Image](/week8/snippet2.png)
- This is how I turned it into a test in my implementation- it is testsnippet2.
  ![Image](/week8/my1.png)
- This is the output, my tests did not pass, and these are the JUnit outputs for the test failures. The failing test is testsnippet2.
  ![Image](/week8/my2.png)
- For the implementation that I reviewed, this is the output when running the tests-The failing test is testsnippet2.
  ![Image](/week8/other2.png)

  ## Snippet 3

- It should produce this link: https://cse.ucsd.edu/. This is the only one that appears as a blue link in commonmark.
  ![Image](/week8/snippet3.png)
- This is how I turned it into a test in my implementation- it is testsnippet3.
  ![Image](/week8/my1.png)
- This is the output, my tests did not pass, and these are the JUnit outputs for the test failures. The failing test is testsnippet3.
  ![Image](/week8/my2.png)
- For the implementation that I reviewed, this is the output when running the tests- The failing test is testsnippet3.
  ![Image](/week8/other2.png)

  ## Fixes

  - For snippet 1, I think an easy solution would be to not count anything as a link if anything starting from the character before the open brackets to the open parenthases contains a sequence of enclosed backticks. This commonmark seems to recognize these as code, not links.

  - For snippet 2, I think I would have my program implement a stack, where I would put every index of every open parenthases on the stack,and pop the stack when there is a closing parenthases. If the stack is empty, I would save the first open parenthases and the last close parenthases index and take the link from there. My program worked for the other links as intended.

  - For snippet 3, I think this would take more than 10 lines of code, because my code simply returned null for the list, meaning none of the issues were dealt with, and none of the cases that should have baited a link worked either, so my program is probably way off the mark when it comes to newlines, and would require some work to get working with them.
