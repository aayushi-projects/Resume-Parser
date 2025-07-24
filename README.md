# Automated Resume Screening & Interview Question Generator
## What Problem this project is Solving?
Let’s say you’re an interviewer and you've been assigned 10–15 candidates to interview. Before you can even talk to any of them, you first have to go through every single resume, try to understand what they’ve done, what skills they have, what kind of projects they’ve worked on — and then, based on that plus the job description (JD), you come up with questions. This might sound simple, but when the volume of candidates increases, this becomes a painful and time-consuming task.
That’s exactly what this project solves.

## What This Workflow Does
This n8n workflow helps automate the boring parts of this process:

(i) It takes in the job description.

(ii) Then, it picks up resumes from a folder stored in OneDrive.

(iii) For each resume:

It extracts the text.

Summarizes the candidate’s profile.

Compares it with the JD.

And finally, generates custom interview questions you can actually ask.

All of this is handled automatically, and the output (summary + questions) is delivered to your Gmail inbox. So you just read the mail and you’re ready for the interview.

## Overview of How It Works
Here’s how the flow runs behind the scenes:

(i) You manually trigger the workflow when you want to start.

(ii) It fetches the job description PDF from OneDrive using the file ID.

(iii) Then it connects to a folder on OneDrive that has all the candidate resumes.

(iv) It loops over each resume:

Downloads it.

Extracts text using the PDF parser.

Sends it to the AI agent.

(v) The AI agent:

Reads both the JD and the resume.

Writes a clean and short summary of the candidate.

Comes up with 5–7 interview questions specifically tailored to that candidate and the job.

(vi) All of this is then sent to your Gmail.

## Tech Stack / Tools Used
(i) n8n – the automation engine.

(ii) OneDrive – for storing resumes and JD.

(iii) OpenAI GPT-4.1 mini – for generating summaries and questions.

(iv) Gmail – to receive the final output.

(v) PDF Extractor Nodes – for text extraction.

(vi) Loop & Memory Buffer – for handling multiple candidates one-by-one.

## How to Run It
(i) Import the workflow JSON into your n8n instance.

(ii) Plug in your credentials for Gmail, OneDrive, and OpenAI.

(iii) Update the file/folder IDs for the job description and resume folder.

(iv) Click Execute.



