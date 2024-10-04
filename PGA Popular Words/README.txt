Rules for the dataset:
Text type: Complex real world text.
Language: English - I know it, the course is in it, easy to read by other people.
Goal: Most popular words.
Threshold values: should get word count for the text and choose the top 1% if the text is above 500 words. If less, top 5%. 
Resaoning for word threshold: The goal is to find meaningful data, therefore it would be good to consider a final output of 
a sufficient number of items with regards to the dataset. A percentage value makes the project scalable
Text chosen: Wikipedia article on data science (thematical)

Technique for accessing data: using vanilla python input-output stream. No need to over-complicate for the task.
Technique for exploring data: copy the data onto a variable and close the stream. More lightweight solution.
Technique for counting words: use a similar technique for word counting from the videos.

Additional step 1: Exclude punctuation marks.
Additional step 2: ignore connecting and junk words such as (but not limited to) articles - "an", "a", "the", conjunctions - "and", "or", etc. and prepositions -  "about", "of", "with", etc.
Additional steps reasoning: Exclude as much junk data not needed for this analysis.

Step 1 technique: Edit the text variable as string with regular expressions to exclude anything except alphabetical characters and
whitespaces.
Step 2 technique: split the text variable into a string list with each value ending at a coma, this is a task that can be done more elegantly without regex, therefore a .csv file with all unwanted words in English will be read, copied onto a variable and the text variable will be
compared to the connectors variable, removing anything included in that.