# Project: PlotGEN

**Concept**

Why would we hard-code a plotline structure? My idea is to have the computer look at a text, discern important plot information from it, and construct its own story from that.

**Outline**
1. Compile texts from sources
    - Gutenberg
    - webscraper
    - manually copying and pasting
2. Analyze the texts
    - Characters
        - build frequency table of characters appearances
        - account for first / second person narration
        - the most frequently mentioned character is most likely the main character
    - Setting
        - use Wordnet to find locations
        - find descriptors of locations to apply as modifiers
3. Build plot structure for each text
    - Summarize each text?
    - Distill each sentence down to basic concepts
        - Example: "Michael walked along the sandy, desolate beach" -> "Michael walked beach" -> `[Michael, ACTION, SETTING]`
    - Using positve / negative word frequency to form a "plot-line"
4. Train unsupervised learning model on plot structures
    - Clustering in n-dimensional space
5. Generate plot structure using structures
    - Group it with closest cluster
    - Change aspect
    - Repeat until firmly within the cluster
6. Profit?

**Resources**

- POS tags
    - https://www.ling.upenn.edu/courses/Fall_2003/ling001/penn_treebank_pos.html
- Article about Six Plots Analysis
    - https://www.vice.com/en_us/article/8qxkkb/computers-find-that-there-are-six-plots
- Matthew Jockers' blogpost about his analysis
    - http://www.matthewjockers.net/2015/02/25/the-rest-of-the-story/
- Datasets of Positive/Negative words
    - https://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#lexicon