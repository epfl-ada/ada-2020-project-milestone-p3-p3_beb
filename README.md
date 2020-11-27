# Title: Analysis of Sexual Discrimination in Police Stops across the US
# Abstract
In the paper, Pierson et al. investigate whether there is racial discrimination in police stops across the US. As our creative extension, we propose to examine the dataset from a different angle, sexual discrimination in police stops in some specific states in the US. We think this topic is interesting because we can apply some of the techniques that were applied in the original paper. We will start by analyzing who carries more contrabands, men or women. Then we investigate the contrabands by their types, such as drugs and weapons. Furthermore, we will use the "Veil of the Darkness" test from the paper and observe stop rates around dusk time for each of the sexes. Lastly, we will inspect if the officers with less experience are more sexist or avoid such discrimination due to lack of experience.

# Research Questions
- RQ1: Which sex carries more contrabands?
- RQ2: Is there any sexual bias against drivers? Do officers stop and search men more than women for no reason?
- RQ3: Are officers with less experience more sexist?

# Proposed dataset
As in the research paper, we will use data from the Stanford Open Policing Project. This project consists of several datasets of police stops across the US. Based on some criteria, such as the availability of relevant information for our analysis, we will focus on some specific locations (Long Beach, CA; Statewide, FL; Chicago, IL). The most constraining factor here is the availability of officers’ years of experience.

Even in the aforementioned states, not all of the data points have the officer’s years of experience, so we will likely have to do imputation or drop some data points. Most of the missing data is from Florida, where we have 100% coverage for officer_id, which might help a bit for imputation. An in-depth look at the data is required to know what the best approach is.

We looked for a dataset which contains dusk information for states across the USA. However, we could not find such a dataset. Therefore, we will use the Astral Python library to calculate the information.

# Methods
Our team will share the research questions, and everyone will work on one research question.

Data Collection: Our team members will select the USA states from the Stanford Open Policing Project that contain the required fields to answer their research question.

Answering the Research Questions:
- RQ1: We will answer the first research question by investigating potential bias in searching drivers for contraband. By using the threshold test, we will highlight a potential correlation between successful search rate and gender.
- RQ2: To answer this question, we will use the "Veil of Darkness." We will examine if there is a bias against drivers of different sexes by analyzing stop rates before and after sunset. After sunset, the lack of sunlight makes it difficult to identify one's sex. The Astral library gives us the dusk time of a location for a given day. Using this information, we will analyze the distribution of stops for each sex.
- RQ3: We will repeat the analysis from RQ2, but this time we will put the traffic stops into different buckets depending on the officer’s total years of experience. We could probably get meaningful results with about 3 buckets: 0-2 years of experience, 2-10, 10+. We will then compare the results between these buckets and see if experience affects gender biases. We might have to alter the buckets a bit depending on the data (new officers might be accompanied by a supervising experienced officer).

# Proposed timeline
- Week 1: Our team will download datasets and start processing the data, such as merging the datasets, managing missing values, summarizing the dataset. 
- Week 2: Our team will start analyses by implementing the proposed methods.
- Week 3: Our team will continue analyses and work on the report, data story, and video recording.

# Organization within the team
- Aaron: Aaron will investigate how officer experience influences gender bias.
- Alpha: By analyzing the datasets, Alpha will focus on the ratio between search and success rate among genders by using the threshold test.
- Melike: She will answer RQ2 using the "Veil of Darkness" test. In Week 1, she will download and clean datasets that have the fields related to the test. Besides, she will use the Astral library to calculate dusk time information of states. In Week 2, she will start implementing the "Veil of Darkness" test and visualize her findings. In Week 3, she will finalize the test and visualization. In Week 3, she will also work on the report, data story, and video.

In Week 3, team members will examine each other's work and discuss their findings.

# Questions for TAs (optional)
