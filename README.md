# articles_of_judgement
How are function words used in legal decisions?

I am curious to see whether function words are used uniformly accross judgements.
I begin with the Federal Court of Canada.

Plan:
- Take a comprehensive dataset
- isolate for judgement text
- clean the text (eliminate numbers and punctuation)
- lower
- tokenize
- write a function to count tokens at different markers of the the text (100 token window)
- markers 10, 20, 25, 30, 40, 50, 60, 70, 75, 80, 90
