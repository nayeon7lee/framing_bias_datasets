# BASIL: dataset for 'In Plain Sight: Media Bias through the Lens of Factual Reporting'

- BASIL contains 300 total files split into 100 triplets, with each triplet containing 3 articles about the same event or topic. Each article in a triplet is from a different news source. Each file contains the original text of the story as well as the gold-standard annotations.  
- Each file is named as {index}_{source}.json, where {index} is 0-99 and {source} is one of {nyt, fox, hpo} corresponding to {The New York Times, Fox News, HuffPost}  
- The files have metadata (e.g. source url), article level annotations (e.g. annotated article stance) and an article body. The body is an ordered list of sentences with the raw utf-8 text, the index of the sentence, and a (possibly empty) list of annotations of spans within that sentence.  


## Key-value pair explanations


### Keys
- url: Original url of the article  
- word-count: Number of (tokenized) words in the article  
- source: News source. One of {nyt, fox, hpo}  
- title: Title of the article  
- date: Date the article was published  
- main-entities: Annotated main entities in the article  
- annotators: Annotators that annotated the article. One of {A, B, C}  
- article-level-annotations: Resolved answers to article level questions  
- author-sentiment: Annotation of author's sentiment towards main event and main entities. One of {Negative, Positive, Neutral, Strongly positive, Strongly negative, Slightly positive, Slightly negative}  
- stance: Annotation of article's stance. One of {Left, Center, Right}  
- body: Body of the article  
- sentence: Text of the sentence  
- sentence-index: Index of the sentence in the article, zero-indexed  
- annotations: List of annotations in the sentence  
- start: Index of first character in the annotation (zero-indexed)  
- end: Index of last character in the annotation (zero-indexed)  
- target: Target main entity  
- polarity: Polarity of the bias. One of {Negative, Positive}  
- aim: Aim of the bias. One of {Direct, Indirect (Ally), Indirect (General), Indirect (Opponent)}  
- indirect-target-name: Optional name of the indirect target  
- indirect-ally-opponent-sentiment: Optional sentiment towards the indirect ally or opponent of the targeted main entity. One of {Negative, Positive, Neutral}   
- bias: Type of the bias. One of {Lexical, Informational}  
- quote: Is the bias part of a quote? One of {Yes, No}  
- speaker: Optional speaker of the quote, if the bias was part of the quote. One of the main entities or one of {Other (Pro-target), Other (Anti-target), Other (Neutral)}  
- text: Text contained in the annotation  


### Some values
- Direct: Direct bias  
- Indirect (Ally): Bias aimed at an ally of the target  
- Indirect (Opponent): Bias aimed at an opponent of the target  
- Indirect (General): Bias aimed at a general entity, not an ally or opponent of the target  
- Other (Pro-target): Speaker of the quote is 'for' the target  
- Other (Anti-target): Speaker of the quote is 'against' the target  
- Other (Neutral): Speaker of the quote is neither 'for' nor 'against' the target  

## BibTeX
```
@inproceedings{mediabias2019,
    title = "In Plain Sight: Media Bias Through the Lens of Factual Reporting",
    author = "Fan, Lisa  and
      White, Marshall  and
      Sharma, Eva  and
      Su, Ruisi  and
      Choubey, Prafulla Kumar  and
      Huang, Ruihong  and
      Wang, Lu",
    booktitle = "Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing",
    year = "2019",
    publisher = "Association for Computational Linguistics"
}
```

