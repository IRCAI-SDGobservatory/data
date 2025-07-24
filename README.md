# SDG Data Infrastructure

This reppository describes the SDG data infrastructure feeding IRCAI's SDG Observatory and the data projects that relate to it. The data infrastructure is distributed across 6 elasticSearch indices that are

* INDICATORS: Global indicators capturing progress on SDGs, used to guide findings and explore causality relations
* MEDIA: Worldwide news on over 60+ languages worldwide used to assess the coverage of the media on AI impac
* SCIENCE: Peer-reviewed scientific articles covering knowledge used to investigate research topics and good practices
* POLICY: Legal and regulatory landscape on AI and Sustainabilit used to monitor perspectives on the use of AI 
* EDUCATION: A range of multilingual open education resources used to facilitate the education for AI and SDGs
* INNOVATION: Entrepreneurship ecosystems focusing AI & Sustainabilit used to ease collaboration, ideation and capacity building

The data is mostly public data often obtained in partnership as follows:

* Our World in Data: we are ingesting the data from the SDG Tracker initiative of the Our World in Data, preprocessing it and readressing the SDG assignment to each of the time series, complementing them with existing ingested data into the system
* Event Registry: under a research usage collaboration with Event Registry we are exploring the multilingual news data rich on metadata extracted through ML methods and technologies (e.g. wikifier.org)
* OpenAlex: we ingest the full open dataset of titles and abstracts of 120M multilingual worldwide research papers representing the published scientific knowledge
* MEDLINE: we complement the wider OpenAlex dataset with the well-estcablished metadata based on the medical taxonomy MeSH Headings  
* OECD.AI: following the OECD AI initiative, we ingest the AI Policies public dataset and explore the SDG topics that are addresssed in these documents in the different perspectives across world regions
* Videolectures.net: 
* IRCAI TOP100: we use part of the data on the listed enterpreneurship initiatives on AI and Sustainability through the TOP100 

The following are the structure files that are made available to understand the metadata of the 6 different data indices:

* IRCAI-ELKdata: 
* IRCAI-SDGObservatory-Indicators: 
* IRCAI-SDGObservatory-Target Indicators: 
* IRCAI-SDGontology: 
* IRCAI-SDGtopics-oAlex: 
* IRCAI-SDGtopics: 
* IRCAI-ObsPilots: 

	NAME	AUTHOR	CONCEPTS	SENTIMENT	SDG	SDG-topic	COUNTRY	PILOT	YEAR
INDICATORS	Indicator Name	/	/	/	SDG	/	country_code	pilot	year
MEDIA	title	authors.name	wikifier.concepts.name	sentiment.compound	SDG	SDGtopic	location.country	pilot	year
SCIENCE	display_name	authorships.author.display_name	wikifier.concepts.name	sentiment.compound	SDG	SDGtopic	authorships.institutions.country_code	pilot	publication_year
POLICY	title	/	wikifier.concepts.name	sentiment.compound	SDG	SDGtopic	country_code	pilot	year
EDUCATION	title	authors.name	wikifier.concepts.name	sentiment.compound	SDG	SDGtopic	country_code	pilot	year
INNOVATION	title	/	wikifier.concepts.name	sentiment.compound	SDG	SDGtopic	country_code	pilot	year


##SDG Terminology Aligned with Wikidata

The terminology used to assigned the 17 SDG labelsto textual documents is based on 10 topics selected as representative and curated by the *mentor* of the SDG (usually the related IRCAI chair).
The 10 Topics defined at each SDG is based on Wikidata keywords that allows a crosslingual approach with language coverage as indicated in Wikipedia.org.
The references to this work are as follows:

Phadke H. and DeMates L. (2022) Investing with the Sustainable Development Goals. TruValue Labs
Salvatori A. and Ho C. (2022) Measuring Corporate SDG Alignment. TruValue Labs




#### Country Codes

Taken from https://github.com/lukes/ISO-3166-Countries-with-Regional-Codes/tree/master
