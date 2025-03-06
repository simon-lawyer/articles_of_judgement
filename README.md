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

If you review analysis.ipynb you will see that there are really interesting changes in how function words are used throughout decisions.
Notable: gendered pronouns, while following different patterns, have different quantities. Articles (particularly indefinite articles) diminish with time.

My observation too is that the dataset is so heavily skewed to immigration decision making that perhaps it should be the priority.

2025 03 06
Research questions. 
Inspired by "When Small Words Foretell Academic Success: The Case of College Admissions Essays" I ask three questions:
1. Do function words and their presumed underlying writing styles predict later citation practices?
2. Sub question: does the entropy of a judgement predict citation patterns?
3. Do function words correlate with judgement outcomes?
4. Sub question: does entropy correlate with outcomes?
5. To what extent does function word use vary across writing samples in a coherent manner, with use of words in different categories jointly contributing information that may meaningfully be combined in a single, underlying dimension?
6. How do decisions distribute themselves along this metric, if it exists? (i.e. Is the pattern identified in Small Worlds also present in legal texts?)
7. To what extent can function word patterns predict the author of a judgement?
8. Is there an entropy fingerprint?

Hypotheses:
1. Yes.
2. There is research that shows that "simpler is better." I hypothesize that simple decisions get cited more than complex decisions. Caveat: decisions that are too simple will be ignored. So, perhaps, there is a sweetspot for simplicity.
3. No. I believe the form is similiar between judgement types.
4. No. 
5. In Small Words, they found that a signfiicant portion of function word use correlated on a single PCA component. I expect similiar results.
6. In Small words, thet found essays at each end of this emtric. I hypothesize that this will not be replicated. LEgal decisions have conform more to a form and authors (judges) are selected in a more rigorous way. Together, this means that they write in similiar ways.
7. There is scholarship that suggests that function words can predict authorship. I believe this holds in legal writing, even though the form is so similiar.

Plan: this may be several articles. For example, an authorship article, a citation practices article.

MEthod:
I will focus exclusively on immigration decision making in the Federal Court.

1. Isolate FC decisions. Isolate imm decisions. Isolate for years (2009-2024; 15 years of decisions).
2. Isolate for decisions where I can computationally identify the judge and the decision.
3. Measure function words use (replicate, to the extent possible, Small Words).
4. PCA the outcome.
5. Measure entropy. Bootstrap 500 token chunks (just alpha) for each decision.
6. Determine if there are function/entropy fingerprints.
7. Determine if there is a relationship between outcomes and function/entropy.
8. Write program to count citations (citations here are a measure of importantce).
