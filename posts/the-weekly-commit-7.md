---
title: "The Weekly Commit #7"
date: 2021-02-04T20:41:15-05:00
draft: false
---
I spotted a wild Big O application!;exciting since I've only experienced it as an exercise. Exciting because it clicked, I didn't simply see that __maybe__ I could write something better, I could **prove** it was better, given certain conditions **and** I knew __why__. 
I'll post the rough outline here so I can ask more knowledgeable people how close(or far off) I was and why. 
#### Naive
`for i in x:
	for j, k in enumerate(y):
		if i == k:
			result.append(i)
#### __More__ Performant at Scale(Big O)
`for i in x:
	index = 0
	for j, k in enumerate(y):
		if i == k:
			index = j
			result.append(i)
			break # this was in original code, but for the sake of a 'pure' naive example i excluded it 
	del y[index] # important
`
The naive is n^2(nested for loop, easy), and the improved implementation I __think__ is `n log n`, since y becomes smaller.
An exciting moment for me even if I'm not right since I at least __thought__ in these terms, unprompted and in respect to myself coding live. Right or wrong it makes me excited to prompt learning more, instead of as a dry example in a book with toy examples.
Respect the little gains, they prompt bigger ones.
### The Doing
* did some sftping, not something I'd ever done, though it's basic which is cool because it's useful and not hard to use. Pretty much the pinnacle of any tool design for any erea
* Wrote a python script that intakes a csv, a json file, updates the json file with the data from the csv in the proper spots, and than dumps out the json again.
	* it cleans up the csv-which is a cut/paste job from a spreadsheet,**fun fact**: excel delineates off of \009 when copy and pasted into plain text), which had some troublesome new lines that through off the reading
	* did some data validation to make sure every json field needed was there
	* future work on it will make it a little more general, parts of it(most of it) is coded specifically to this first file since that was my main objective
* Actually wrote a test case for my personal project. I feel the pieces falling into place for me to pick up steam on that again. More on that.
### The Learning
After only a brief absence this is **back**, for a limited tenor. Reasons why:
* Wes Bos finally updated his Advanced React course, which I use to keep myself abreast of this sort of stuff. I've been part of it for awhile, and right as I was about to use react and brush up on it so I could do the frontend for my personal project back in November, Wes said there was a major update coming for his course, so I decided to wait, and here we are 3 months later(maybe longer, definitely not shorter since I know it was before December). 
* For my job, I've been learning and need to continue to learn basic ETL concepts. Had a KT at work today, and that's prompting me to look into the ETL concepts in-light of the Star Schema.

### The Future
* Finishing up the learning
* Actually writing some more test cases for my backend.
