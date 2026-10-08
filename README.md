AI Content Repurposing Automation



An AI-powered content repurposing workflow built with n8n that transforms one source article into a structured multi-platform content package.



The workflow demonstrates practical Generative AI, workflow automation, prompt engineering, structured output generation, and human-in-the-loop content review.



Project Overview



Creating content for multiple platforms from a single article can be repetitive and time-consuming.



This project automates that transformation:



Source Article

&#x20;    ↓

Webhook

&#x20;    ↓

AI Content Repurposing Agent

&#x20;    ↓

Structured Output

&#x20;    ↓

Content Package

&#x20;    ↓

Human Review

&#x20;    ↓

Ready for Publishing



The system takes one article and generates platform-specific content while keeping the generated material grounded in the supplied source.



What It Generates



For every source article, the workflow produces:



1 Summary

1 LinkedIn Post

2 Instagram Captions

3 X Posts

5 Content Ideas with titles and descriptions



The result is returned as structured JSON.



Architecture

┌─────────────────────────┐

│      Source Article     │

└────────────┬────────────┘

&#x20;            │

&#x20;            ▼

┌─────────────────────────┐

│    Webhook Trigger      │

│      POST Request        │

└────────────┬────────────┘

&#x20;            │

&#x20;            ▼

┌─────────────────────────┐

│ AI Content Repurposing  │

│         Agent            │

│                          │

│ • Source grounding      │

│ • Platform adaptation   │

│ • Content generation    │

└────────────┬────────────┘

&#x20;            │

&#x20;            ▼

┌─────────────────────────┐

│   Structured Output     │

│       Parser            │

└────────────┬────────────┘

&#x20;            │

&#x20;            ▼

┌─────────────────────────┐

│  Content Package JSON   │

└────────────┬────────────┘

&#x20;            │

&#x20;            ▼

┌─────────────────────────┐

│      Human Review       │

└─────────────────────────┘

Input



The workflow accepts a source article through a webhook.



Example:



{

&#x20; "article": "How Small Businesses Can Use AI Automation to Save Time..."

}



Webhook endpoint:



POST /webhook-test/ai-content-repurposing



The production webhook can be enabled when required.



Output Structure



The workflow returns:



{

&#x20; "summary": "A concise summary of the article.",

&#x20; "linkedin\_post": "Professional LinkedIn content.",

&#x20; "instagram\_captions": \[

&#x20;   "Educational Instagram caption.",

&#x20;   "Conversational Instagram caption."

&#x20; ],

&#x20; "x\_posts": \[

&#x20;   "First X post.",

&#x20;   "Second X post.",

&#x20;   "Third X post."

&#x20; ],

&#x20; "content\_ideas": \[

&#x20;   {

&#x20;     "title": "Content idea 1",

&#x20;     "description": "Description of the idea."

&#x20;   },

&#x20;   {

&#x20;     "title": "Content idea 2",

&#x20;     "description": "Description of the idea."

&#x20;   }

&#x20; ]

}



The actual workflow generates five content ideas.



AI Prompt Strategy



The AI agent is instructed to:



Use only information from the supplied source article.

Preserve the original meaning.

Avoid invented statistics, facts, quotes, or claims.

Adapt content to the style of each platform.

Keep LinkedIn content professional.

Keep Instagram content engaging and readable.

Keep X posts concise.

Avoid excessive hashtags.

Return only the required structured JSON.



This approach provides a basic source-grounding control for the content-generation workflow.



Human-in-the-Loop



The workflow intentionally does not automatically publish generated content.



The generated package should be reviewed by a human before publishing.



This allows the reviewer to:



Check factual accuracy

Adjust brand tone

Edit wording

Add campaign-specific information

Approve or reject individual posts

Choose which content should be published



This design demonstrates responsible AI-assisted content automation rather than uncontrolled automatic publishing.



Technology Stack

n8n — Workflow automation

AI Agent — Content generation and transformation

GPT-5 mini — Language model

Structured Output Parser — JSON output validation

Webhook — Workflow API interface

JSON — Structured content exchange

Testing



The workflow was tested with:



Test 1 — Short Synthetic Article



A short test article was submitted through the webhook.



Result:



PASS



The workflow generated the expected structured content package.



Test 2 — Full Source Article



A 425-word synthetic portfolio article was submitted.



Result:



PASS



The workflow generated:



Summary

LinkedIn post

2 Instagram captions

3 X posts

5 content ideas

Source Grounding



Generated content was reviewed against the source article to verify that the workflow remained substantially grounded in the supplied information.



Result:



PASS



Structured Output



The response was validated against the expected JSON structure.



Result:



PASS



See:



docs/testing.md

docs/architecture.md

docs/project-status.md

Project Structure

AI-Content-Repurposing-Automation/

│

├── input/

│   └── source-article.txt

│

├── output/

│

├── prompts/

│   └── content-repurposing-prompt.txt

│

├── screenshots/

│

├── docs/

│   ├── architecture.md

│   ├── testing.md

│   └── project-status.md

│

├── test-data/

│

└── README.md

Portfolio Skills Demonstrated



This project demonstrates practical experience with:



AI workflow automation

Generative AI

AI agents

Prompt engineering

Structured outputs

JSON schema-based generation

Webhook integrations

Source-grounded generation

Multi-platform content transformation

Human-in-the-loop AI workflows

Workflow testing and validation

n8n automation design

Current Limitations



This is a portfolio demonstration rather than a production publishing platform.



Current limitations include:



No automatic social media publishing

No persistent content database

No duplicate-content detection

No brand-specific memory

No analytics feedback loop

Source grounding is limited to the supplied article

AI model usage depends on available n8n/Gateway credits

Future Improvements



Possible future versions could include:



Google Drive article ingestion

Google Docs integration

Content approval workflow

Social media publishing integrations

Brand voice profiles

Content calendar generation

Content history database

Duplicate-content detection

Analytics-based content optimization

RAG-based brand knowledge

Multi-agent content generation

Automated campaign planning

Business Use Cases



The same architecture can be adapted for:



Digital marketing agencies

Freelancers

Coaches and consultants

Small businesses

SaaS companies

Personal brands

Content marketing teams



For example, a business could provide one weekly article and automatically generate a complete set of social-media content for human approval.



Project Status



Functionally Complete and Frozen



The workflow has been tested successfully and is ready for portfolio demonstration.



Future enhancements should be treated as separate iterations rather than modifications to the current frozen baseline.



Author



Obulisivananthan VR



AI Automation \& GenAI App Builder

Digital Marketing Specialist | AI Workflow Automation | Generative AI

