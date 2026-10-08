Project Status

Project



AI Content Repurposing Automation



Current Status



Functionally Complete and Frozen



Objective



Build an AI-powered workflow that converts one source article into a structured content package for multiple social media and content channels.



Input



The workflow accepts a source article through a webhook.



Expected input format:



{

&#x20; "article": "Source article text"

}

Automated Outputs



The workflow generates:



1 summary

1 LinkedIn post

2 Instagram captions

3 X posts

5 content ideas with titles and descriptions

Workflow

Webhook

&#x20;  ↓

AI Content Repurposing Agent

&#x20;  ↓

Structured Output Parser

&#x20;  ↓

Respond with Content Package

AI Capabilities Demonstrated

Generative AI content transformation

AI workflow automation

Structured JSON generation

Prompt engineering

Platform-specific content generation

Source-grounded content generation

Webhook-based workflow integration

Human-in-the-loop content review

Testing Status



The workflow was tested with:



A short synthetic article

The complete 425-word source article

Structured output validation

Source-grounding validation

Human-review workflow validation



All planned functional tests passed.



Human Review



The workflow does not automatically publish generated content.



Generated content should be reviewed and edited by a human before publishing.



This design reduces the risk of inaccurate, inappropriate, or poorly adapted content being published automatically.



Current Limitations

Uses an AI model through n8n Gateway credits.

Does not automatically publish to social media platforms.

Uses a webhook as the current input interface.

Knowledge grounding is limited to the supplied source article.

No long-term content history or duplicate-content detection is implemented.

Future Enhancements



Potential future improvements include:



Google Drive or document-based article input

Content approval workflow

Social media publishing integrations

Content calendar generation

Brand voice profiles

Multiple content formats

Content history and duplicate detection

Analytics-driven content optimization

RAG-based knowledge sources

Multi-agent content workflows

Portfolio Value



This project demonstrates the ability to design an AI automation workflow that transforms a single business input into multiple structured outputs while maintaining source grounding and human review.



The project focuses on practical AI automation rather than simple chatbot interaction.



Final Status



FUNCTIONALLY COMPLETE — FROZEN



The current workflow is considered complete for portfolio demonstration. Future improvements should be treated as separate iterations rather than changes to the frozen baseline.

