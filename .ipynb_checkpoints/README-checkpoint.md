# Scraping and NLP Pipeline Lab

## Objective
The objective of this lab is to gain hands-on experience with web scraping and Natural Language Processing (NLP) techniques. The pipeline consists of:

1. **Scraping Data:** Utilize Scrapy and Beautiful Soup to scrape data from Arabic web source bbc arabic.
## Example Scraped Data
```json
{
  "article_info": {
    "author": "BBC News عربي",
    "date_modified": "2024-04-07T17:29:47.481Z",
    "date_published": "2024-04-07T14:22:07.221Z",
    "headline": "خان يونس: إسرائيل تسحب كامل قواتها من جنوبي غزة، وتستكمل 'مرحلة أخرى' استعداداً 'للحرب' على حدود لبنان",
    "url": "https://www.bbc.com/arabic/articles/c1vldp9le52o"
  },
  "article_text": [
    "إسرائيل تسحب كامل قواتها من جنوبي غزة، وتستكمل 'مرحلة أخرى' استعداداً 'للحرب' على حدود لبنان",
    "",
    "أعلن الجيش الإسرائيلي الأحد أنه استكمل 'مرحلة أخرى' في إطار استعداداته 'للحرب' عند الحدود الشمالية مع لبنان حيث يستمر القصف المتبادل مع حزب الله، بينما قال إنه سحب كامل قواته من جنوبي قطاع غزة.",
    "وفي بيان بعنوان 'الاستعداد للانتقال من الدفاع إلى الهجوم' نشره الجيش الإسرائيلي، قال إنه 'خلال الأيام الأخيرة تم استكمال مرحلة أخرى من استعدادات قيادة المنطقة الشمالية للحرب'، موضحاً أن هذه التدابير اللوجستية تسمح بـ'التجنيد "
  ]
}


2. **Data Storage:** Store the raw scraped data in MongoDB, a NoSQL database.
   
3. **NLP Pipeline:** Implement various NLP techniques:
   - **Text Cleaning:** Remove noise and irrelevant characters such as emails and english caracters.
   - **Tokenization:** Split text into tokens (words or phrases).
   - **Stop Words Removal:** Eliminate common words.
   - **Normalization:** Standardize text to a consistent format , form chosen 'utf-8'.
   
4. **Stemming and Lemmatization:** Unfortunately it seems that stemming implementation in ntlk was not up to standards as it contains multiple mistakes , and i would have prefered to do Lemmatization but unfortunately there is a big lack of python librabries for the arabic language.
   
5. **Parts of Speech (POS) Tagging:**
    ***(Rule Based)***: I decided to write a simple implementation using regex , it did not give good results due to the difficulty of implementing all the rules of the arabic language , and unlike ML based one it takes way too many rules to create a working prototype.
   
6. **Named Entity Recognition (NER):** Apply NER methods to identify and classify named entities within the text data.

## Synthesis
During this project, the following tasks were completed:
- Web scraping was performed using Beautiful Soup to gather data from BBC arabic website.
- The raw scraped data was stored in MongoDB for further processing and analysis.
- A comprehensive NLP pipeline was established, including text cleaning, tokenization, stop words removal,  and normalization.
- Stemming and lemmatization techniques were applied to analyze their effectiveness in the Arabic language context.
- Parts of Speech (POS) tagging was implemented using both rule-based and machine learning approaches to classify words into different categories.
- Named Entity Recognition (NER) methods were explored to identify and classify named entities within the text data.




