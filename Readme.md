# MultilingualModelStatistics

Attempts to reconstruct the multilingual content of large language models and the associated training resources, using normalized (ISO) language codes.

For the English models, we assume 100% English even though the statistics of ([Blevins and Zettlemoyer, 2002])(https://arxiv.org/pdf/2204.08110v2.pdf) tell that there is some "contimation" (very poor choice of word IMO) from other languages.

For each model, the three first codes are the ISO standard, then the language name in the dataset, then the number of  Kilo-tokens and the percentage in the training data. This is only indicative of what the model has seen in training, since low-resource languages are usually oversampled (and high-resource languages) upsampled. Missing values are "??"

## [ISO standards page from the Library of Congress][https://www.loc.gov/standards/iso639-2/ascii_8bits.html]
- An alpha-3 (bibliographic) code,
- an alpha-3 (terminologic) code (when given),
- an alpha-2 code (when given),
- an English name,
- and a French name of a language are all separated by pipe (|) characters.
- If one of these elements is not applicable to the entry, the field is left empty, i.e., a pipe (|) character immediately follows the preceding entry.

## Monolingual English
 
Is a generic language distribution with 100% English, to be used for all English only models (GPT-J, etc) even though they may contain a small portion of English data.

## [mBERT]()

The language list is available at source https://github.com/google-research/bert/blob/master/multilingual.md

## [GPT-3](https://arxiv.org/abs/2005.14165)

Mostly English
[Language statistics](https://raw.githubusercontent.com/openai/gpt-3/master/dataset_statistics/languages_by_word_count.csv) contains iw, jw and zh-Hant which are not valid codes.
\cite{Lin22} claims GPT3 contains traces of 118 languages, 93% of the train data is English

## [mT5](https://aclanthology.org/2021.naacl-main.41.pdf)

mT5 is pretrained on the mC4 corpus, covering 101 languages:

Afrikaans, Albanian, Amharic, Arabic, Armenian, Azerbaijani, Basque, Belarusian, Bengali, Bulgarian, Burmese, Catalan, Cebuano, Chichewa, Chinese, Corsican, Czech, Danish, Dutch, English, Esperanto, Estonian, Filipino, Finnish, French, Galician, Georgian, German, Greek, Gujarati, Haitian Creole, Hausa, Hawaiian, Hebrew, Hindi, Hmong, Hungarian, Icelandic, Igbo, Indonesian, Irish, Italian, Japanese, Javanese, Kannada, Kazakh, Khmer, Korean, Kurdish, Kyrgyz, Lao, Latin, Latvian, Lithuanian, Luxembourgish, Macedonian, Malagasy, Malay, Malayalam, Maltese, Maori, Marathi, Mongolian, Nepali, Norwegian, Pashto, Persian, Polish, Portuguese, Punjabi, Romanian, Russian, Samoan, Scottish Gaelic, Serbian, Shona, Sindhi, Sinhala, Slovak, Slovenian, Somali, Sotho, Spanish, Sundanese, Swahili, Swedish, Tajik, Tamil, Telugu, Thai, Turkish, Ukrainian, Urdu, Uzbek, Vietnamese, Welsh, West Frisian, Xhosa, Yiddish, Yoruba, Zulu.

##  [mGPT](https://arxiv.org/pdf/2204.07580)

From the paper: "We introduce a family of autoregressive GPT-like models with 1.3 billion parameters trained on 60 languages from 25 language families using Wikipedia and Colossal Clean Crawled Corpus (C4). [Also some more rare languages from common crawl]"

Languages:

Afrikaans, Azerbaijani, Belarusian, Bengali, Chuvash, German, English, Basque, Finnish, Hebrew (modern), Hungarian, Indonesian, Japanese, Kazakh, Kirghiz, Kyrgyz, Latvian, Mongolian, Malay, Dutch, Polish, Romanian, Moldavan, Yakut, Swahili, Telugu, Thai, Turkish, Tuvinian, Urdu, Vietnamese, Yoruba, Arabic, Bashkir, Bulgarian, Buriat, Danish, Greek, Modern, Spanish; Castilian, Persian, French, Hindi, Armenian, Italian, Georgian, Korean, Lithuanian, Malayalam, Marathi, Burmese, Ossetian, Ossetic, Portuguese, Russian, Swedish, Tamil, Tajik, Turkmen, Tatar, Ukrainian, Uzbek, Kalmyk, Chinese

##  [XGLM4.5](https://arxiv.org/abs/2112.10668)
(134 languages)

## [XGLM](https://arxiv.org/abs/2112.10668)
From the paper "0nly the 4.5B model is trained on the 134 languages, the other models only use 30"

## [XLM-R](https://arxiv.org/pdf/1911.02116.pdf)

Uses the Common Crawl 100  training corpus. The language statistics are in Table 6.

## [BLOOM](https://huggingface.co/bigscience/bloom)

Bloom is trained on 46 languages

## Other Resources
- [language codes from SIL](https://iso639-3.sil.org/code_tables/639/data)
- [WALS](https://wals.info/languoid)
