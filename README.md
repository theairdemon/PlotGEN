# Project: PlotGEN

**Concept**

Why would we hard-code a plotline structure? My idea is to have the computer look at a text, discern important plot information from it, and construct its own story from that.

**Outline**
1. Compile texts from sources
    - Gutenberg
    - webscraper
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
4. Train unsupervised learning model on plot structures
    - Clustering in n-dimensional space
5. Generate plot structure using structures
    - Group it with closest cluster
    - Change aspect
    - Repeat until firmly within the cluster
6. Profit?