# Cohere-Job-Application-Evaluator

I developed a recruiter assessment tool using Cohere's Command-R LLM model to evaluate applicant suitability based on job descriptions and resumes. This project allowed me to become familiar with Cohere's LLM models and demonstrate my qualifications for Cohere's Machine Learning Fall 2024 internship role.

Through this project, I gained insights into Cohere's LLM offerings and how they compare with other industry models. I learned to implement Guardrails AI to ensure consistent and structured outputs from the LLM. Using Pydantic, I defined an output schema to specify the expected JSON format.

Although this was a quick project, I would like to further test the LLM against multiple resumes, both suitable and unsuitable, to evaluate the reasoning behind each decision. For a weekend project, I learned a lot about Cohere's LLMs and am excited about the opportunity to contribute to advancing the capabilities of LLMs at Cohere!

## Steps
1. ### Extract Job Posting Information  
   Summarize the job posting to include the company mission, job responsibilities, and required/preferred skills.
   ```json
   {
       "position": "Machine Learning Intern/Co-op",
       "company_mission_values": "Scale intelligence to serve humanity. Team of researchers, engineers, designers. Diverse range of perspectives. Focus on building great products.\n\nMission-driven, hard-working, fast-moving, customer-centric.",
       "job_description": [
           "Ship state-of-the-art models to production",
           "Design and implement novel research ideas",
           "Build elegant training and deployment pipelines",
           "Work closely with product teams to develop solutions",
           "Train large-scale models",
           "Explore continual and active learning strategies",
           "Learn from senior ML technical staff"
       ],
       "skills": [
           "Python",
           "Tensorflow",
           "TF-Serving",
           "JAX",
           "XLA/MLIR",
           "Distributed training strategies",
           "Autoregressive sequence models",
           "Strong communication",
           "Applied NLP passion",
           "CUDA",
           "TPUs",
           "Papers at top-tier venues"
       ]
   }

2. ### Create a Checklist
   Develop a checklist based on the job description brief to evaluate applicants and resumes.
   ```json
   {
       "company_mission_values": {"align": False, "reasoning": ""},
       "job_description": {"align": False, "reasoning": ""},
       "skills": [
           {"skill": "Python", "possess": False, "reasoning": ""},
           {"skill": "Tensorflow", "possess": False, "reasoning": ""},
           {"skill": "TF-Serving", "possess": False, "reasoning": ""},
           {"skill": "JAX", "possess": False, "reasoning": ""},
           {"skill": "XLA/MLIR", "possess": False, "reasoning": ""},
           {"skill": "Distributed training strategies", "possess": False, "reasoning": ""},
           {"skill": "Autoregressive sequence models", "possess": False, "reasoning": ""},
           {"skill": "Strong communication", "possess": False, "reasoning": ""},
           {"skill": "Applied NLP models", "possess": False, "reasoning": ""},
           {"skill": "CUDA", "possess": False, "reasoning": ""},
           {"skill": "TPUs", "possess": False, "reasoning": ""},
           {"skill": "Publishing research papers", "possess": False, "reasoning": ""}
       ]
   }
  
3. ### Extract Resume and Personal Statement Information 
   Identify technical skills and work experience from the resume and personal statement.
   ```json
   {
       "name": "Joshua Chang",
       "skills": [
           "Python", "SQL", "R", "Java", "C++", "JavaScript", "BASH", "Git", "Cohere Command-R", "TensorFlow", "CUDA", "JAX", "Pandas", "Open AI", "Langfuse", "Scikit-Learn", "PyTorch"
       ],
       "experience": [
           {
               "role": "Machine Learning Engineer",
               "company": "Keplar.io",
               "duties": [
                   "Developed Constitutional AI using LLM and Prompt Engineering methodologies",
                   "Enhanced LLM performance with Optimization by Prompting (OPRO)",
                   "Constructed benchmarking suite for quantitative and qualitative tests to assess LLM performance",
                   "Generated product designs using image generation models and ControlNet"
               ]
           },
           {
               "role": "Data Scientist",
               "company": "Quantolio Financial Technologies",
               "duties": [
                   "Led end-to-end feature development, conceptualization, and implementation of an interactive Streamlit UI",
                   "Deployed containerized application on Heroku",
                   "Communicated product features and value to clients and investors"
               ]
           },
           {
               "role": "Data Engineer & Computer Vision RA",
               "company": "University of Waterloo",
               "duties": [
                   "Used YOLOv5 for object detection and 3D Pose Estimation analysis",
                   "Aggregated and cleaned baseball data from SQL databases and AWS S3 for model training"
               ]
           },
           {
               "role": "Site Reliability Engineer",
               "company": "The Globe and Mail",
               "duties": [
                   "Created AWS Lambda function to scale Kinesis data streams",
                   "Implemented monitoring and alerting for Airflow DAGs to identify anomalies"
               ]
           }
       ]
   }

4. ### Evaluate Qualification 
   Use the checklist to assess my resume and personal statement. If qualified, prepare interview questions to further evaluate suitability for the role.

    > Applicant: Joshua Chang
    > 
    > Recommendation: Proceed to interview.
    > 
    > Reasoning: Joshua Chang's application demonstrates a strong alignment with the company's mission and values, and he
    > possesses many of the skills and experiences outlined in the job description. His passion for machine learning and 
    > its positive impact on humanity is evident and closely resonates with the company's vision.
    > 
    > While there are some skills in the checklist that Joshua does not explicitly possess, his application still stands 
    > out due to his extensive experience and strong technical skills. His research and industry experience in machine 
    > learning engineering, data science, and related fields make him a promising candidate.
    > 
    > #### Suggested Interview Questions:
    > 
    > - Joshua mentions his passion for machine learning and its positive impact on humanity. Can you elaborate on how 
    > you see your work in this field benefiting others? (Company Mission & Values)
    > 
    > - You've had diverse internship experiences. How do you think these roles have prepared you for a position focusing
    > on machine learning and NLP? (Experience & Alignment with Job Description)
    > 
    > - Your recent work involved integrating recent advancements in LLMs. Can you describe a specific challenge you 
    > faced during this process and the steps you took to overcome it? (Problem-Solving & Technical Skills)
    > 
    > - In your personal statement, you mention building a recruiter assessment tool using Cohere's Command-R LLM. What 
    > motivated you to build this project, and how do you think it could be improved further? (Initiative & 
    > Problem-Solving)
    > 
    > - As you aim to expand your knowledge of LLMs, what specific aspects or challenges of this field interest you the 
    > most, and why? (Passion & Interest)
    > 
    > - Have you ever had to present your research work or project to a non-technical audience? How did you ensure your 
    > complex ideas were communicated effectively? (Communication Skills)
    > 
    > - Since publishing research papers is one of your strengths, what has been your most notable contribution, and what
    > impact do you think it has had on the field? (Research Experience)
    > 
    > - Finally, what are your expectations from your mentors and colleagues in terms of guidance and collaboration in 
    > your next role? (Alignment with Company Culture)
    > 
    > These questions will provide further insight into Joshua's suitability for the role, allowing the interviewer to 
    > assess his fit with the team, his passion for the field, and his technical skills and experience.

