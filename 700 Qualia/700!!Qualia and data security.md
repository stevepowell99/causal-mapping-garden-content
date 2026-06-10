---
date: 2025-11-07
---

- Data security and compliance
  - Our candid opinion is that although many clients are understandably extremely cautious about using AI, the risks are completely within the range of any other online data collection, e.g. questionnaires. A system is only as secure as its weakest link. For example if datasets are being shared by an online service like Google Drive, there is not much point having a Fort-Knox-level AI service ...
  - For Qualia:
    - The transcription and Interviewer APIs are located in the USA, at openAI's servers. Data is not used for training. Data is retained there for 30 days for US compliance purposes. 
    - Interview data is stored at a Heroku SQL database in the USA. Data is encrypted at rest and in transit. This is standard best practice. We have daily backups. While it is relatively easy to move the location of AI services it is quite difficult to move the location of database servers. 
    - Clients are sometimes concerned about the AI data being temporarly stored in the US. However, so is just about everything else that happens on the internet .... If the client requires using AI services located say in the UK or EU, we could probably do that. But it is not obvious to me what would be gained. It is in theory possible to also provide AI services which are not retained for 1-30 days for compliance purposes. However this may require justification and could conceivably attract the attention of e.g. anti-terrorism agencies. 

- **The Data Security Sceptic**
    - A client who is primarily concerned about data privacy, security compliance, and the risks associated with AI-powered interview tools.
    - Qualia's data security measures are on par with standard online data collection methods, with encryption both at rest and in transit in the SQL database.
    - Interview data is not used for AI training, addressing concerns about proprietary or sensitive information being used to improve AI models.
    - The temporary 30-day storage of data on US servers is comparable to most internet services and tools commonly used in research. There are good reasons for the data retention controls.
    - Daily backups ensure data integrity and protection against loss.

