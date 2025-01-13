---
title: "Using Artificial Intelligence"
description: "Guides lead a user through a specific task they want to accomplish, often with a sequence of steps."
summary: ""
date: 2023-09-07T16:04:48+02:00
lastmod: 2023-09-07T16:04:48+02:00
draft: false
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---
Harnessing the power of artificial intelligence requires a balance of innovation, responsibility, and vigilance. AI tools offer transformative potential to enhance productivity, improve decision-making, and deliver impactful results. However, their use must account for the serious threats to security, privacy, and ethical integrity they can pose if not managed properly. This policy emphasizes the importance of responsible AI integration, ensuring adherence to ethical standards, safeguarding sensitive information, and fostering advancements aligned with established goals and values.

This AI Usage Policy provides clear, actionable guidance to ensure the responsible, secure, and effective use of AI tools. By following this policy, individuals can confidently leverage AI while minimizing threats to data security, privacy.

## What is Artificial Intelligence (AI)?

Artificial intelligence (AI) refers to any computer system that can perform tasks typically requiring human intelligence. These tasks may include:

- **Visual perception**: Identifying objects, faces, or patterns in images or videos.
- **Text generation**: Creating written content, summarizing documents, or answering questions.
- **Speech recognition**: Understanding and processing spoken language.
- **Language translation**: Converting text or speech from one language to another.

AI can range from simple rule-based systems to advanced models that learn and adapt over time. Examples include predictive analytics tools, chatbots, and generative systems that create text, images, or code.

### On-Device AI
On-device AI processes data locally on a device without requiring a connection to external servers. This can provide benefits such as enhanced privacy, faster processing, and reduced dependency on internet connectivity. Examples include AI features on smartphones for image enhancement, voice commands, or offline translation.

## Guidelines for Using AI Tools

{{< callout context="note" title="Ongoing compliance with policies" icon="outline/alert-triangle" >}}
 AI is still subject to established policies and procedures for patch management, vendor management, vulnerability management, and dependency tracking.
{{< /callout >}}

### Verification
- Review all AI-generated information to ensure accuracy and appropriateness. Cross-check with trusted sources to confirm validity and reliability.

### Intellectual Property (IP) Risks
- Verify that AI-generated content does not infringe on third-party **intellectual property rights** by checking for originality using plagiarism detection tools or trusted intellectual property databases.
- Contact the legal team at `legal@company.com` for guidance on intellectual property or compliance issues.

{{< callout context="caution" title="Ensure intellectual property compliance" icon="outline/alert-triangle" >}}
AI-generated content must not violate intellectual property rights. Plagiarism detection tools or trusted intellectual property databases can be used to verify originality. Consult legal experts if there is any doubt.  
Failure to verify compliance could result in serious legal or financial liabilities.
{{< /callout >}}

### Use Demo or Public Data
- Use only demo or public data when testing AI tools, such as publicly available information like marketing materials.
- Ensure all data aligns with the [Data Classification Policy](#) for appropriate handling.

#### On-Device AI Use
Using on-device AI is acceptable because data remains local, improving privacy and reducing exposure to external threats. However:

{{< callout context="caution" title="External connectivity of on-device AI" icon="outline/alert-triangle" >}}
Even on-device AI may connect to external servers for tasks requiring significant processing power or large datasets. This could expose data to external risks. Validate external connections and ensure compliance with the rules outlined in this policy.
{{< /callout >}}

#### Ask These Questions Before Sharing Data:
- Would this information be shared outside the group?
- Would it be acceptable for this data to become public?

Do not use the data if the answer to either question is no.

### Unacceptable Uses of AI

{{< callout context="caution" title="Unacceptable risk" icon="outline/alert-triangle" >}}
The EU AI Act limits certain uses of AI, like mass surveillance, predictive policing, and job selection. It also has rules that restrict data use, which can limit some AI methods.{{< /callout >}}

Some AI-driven activities are not permissible under any circumstances, in line with guidance from the EU AI Act:

- **Manipulation of individuals**: Exploiting personal vulnerabilities to influence behavior without informed consent.  
  *Example*: Using AI to analyze someone's emotional state and deliver persuasive messages intended to sway financial or political decisions.

- **Social scoring**: Assigning ratings or judgments to individuals based on their behavior or data, leading to unequal treatment or discrimination.

- **Real-time remote biometric identification**: For instance, scanning faces in public spaces to track or identify people without their knowledge or approval.

### Right to Challenge Automated Decisions

Under GDPR, individuals have the right to contest automated decisions involving AI—such as those used in hiring or credit scoring—if they believe the outcome is unfair or harmful. In such cases, a **Data Subject Access Request (DSAR)** can be submitted to gather more information or dispute the result. Refer to the [DSAR procedure](#) for proper handling of these requests in line with privacy regulations.

### Company-Managed Accounts
Once AI usage extends beyond a trial or evaluation phase, it must be conducted through company-managed accounts. Refer to the [Access Control Policy](#) for more details on managing AI accounts securely.

{{< callout context="caution" title="User responsibility for decisions" icon="outline/alert-triangle" >}}
AI can be a powerful tool to support decision-making, but it must not replace human judgment. Each individual is fully responsible for decisions made using AI-generated content. Always validate AI suggestions against reliable sources and exercise professional discretion.
{{< /callout >}}

## Preparing Data for AI Use

### Anonymization
- Remove or replace sensitive details to prevent identification.  
  **Example**: Replace customer names with randomized IDs.

### Sanitization
- Clean data to remove unnecessary or sensitive information.  
  **Example**: Redact financial account numbers from records.

{{< callout context="caution" title="Protect sensitive information" icon="outline/alert-triangle" >}}
Proprietary information, confidential documents, or unapproved source code must not be shared with AI tools like ChatGPT. This protects sensitive intellectual property from external exposure.
{{< /callout >}}

## Why AI Needs to Be Used with Care

{{< callout context="note" title="Ethical AI usage" icon="outline/info-circle" >}}
AI usage must comply with the [Acceptable Use Policy](#) to ensure all activities adhere to ethical and legal standards.
{{< /callout >}}

AI is helpful, but not flawless. Thoughtful and responsible use is required to avoid mistakes and harmful outcomes. Key considerations include:

- **AI can provide incorrect information as facts**: Sometimes, AI confidently gives wrong answers, causing misunderstandings or poor decisions.
- **AI can reflect biases**: If training data includes biases, the tool may reinforce or amplify them.
- **AI can be misled by certain questions**: Leading or manipulative questions can confuse AI and produce unreliable or skewed results.
- **AI may create harmful content**: Poorly framed instructions or questions can lead AI to generate inappropriate or harmful responses.
- **AI training data can be influenced**: If the data used to train AI is tampered with, the tool's performance and reliability can suffer.

{{< callout context="caution" title="Approach AI responsibly" icon="outline/alert-triangle" >}}
Use AI responsibly by validating results, avoiding overly leading questions, and being aware of limitations. This ensures accuracy, fairness, and safety in AI usage.
{{< /callout >}}

## Monitoring and Accountability for AI Use

- **Browser-Based ITDR Platform**: The use of AI Software as a Service (SaaS) is monitored through a browser-based Identity Threat Detection & Response (ITDR) platform to detect suspicious or unauthorized activities.
- **SIEM Logging**: Logs from AI SaaS systems must be sent to the Security Information and Event Management (SIEM) solution whenever possible. If direct logging is not supported, alternative monitoring processes are required.
- **Logging and Monitoring Policy**: Refer to the [Logging and Monitoring Policy](#) for requirements on collecting, storing, and analyzing logs related to AI services.

## Asset Inventory for AI

Approved AI systems or applications with AI components must be included in the asset inventory to ensure visibility and proper oversight. This practice helps maintain an accurate record of all AI-related assets in use, enabling better management of risks, compliance requirements, and operational considerations.

## Your Role in Responsible AI Use

1. **Validate AI-generated content**: Always check the accuracy, reliability, and appropriateness of content generated by AI tools.
2. **Protect sensitive data**: Refrain from uploading proprietary, confidential, or sensitive data to AI systems without proper anonymization or authorization.
3. **Follow policies and guidelines**: Ensure adherence to the [Data Classification Policy](#), [Acceptable Use Policy](#), and other applicable standards.
4. **Understand limitations**: Remain aware of the limitations and potential threats associated with AI tools, including bias or inaccuracies.
5. **Secure access**: Use only company-managed accounts for AI activities beyond trials to comply with the [Access Control Policy](#).
6. **Report incidents promptly**: Report biases, inaccuracies, or harmful outcomes immediately using the [Incident Response Procedure](#).

{{< callout context="caution" title="Reporting AI incidents" icon="outline/alert-circle" >}}
If incidents such as bias, incorrect information, or harmful content are identified, report them immediately according to the [Incident Response Procedure](#). Timely reporting ensures that threats are quickly addressed.
{{< /callout >}}

## Development with AI

{{< callout context="caution" title="Protect intellectual property" icon="outline/alert-triangle" >}}
Entire solutions or large portions of company code must not be uploaded to AI systems like Co-Pilot. Doing so can result in unauthorized disclosure of intellectual property.
{{< /callout >}}

- **Peer Review**: Material created with AI assistance must undergo peer review (e.g., via pull requests) to identify potential risks or errors before integration.
- **Sensitive Data Scanning**: Tools such as AikidoSec must be used to ensure confidential information, such as API keys or secrets, is not included in the material.
- **Adherence to the SDLC Policy**: All development involving AI must follow the [Software Development Life Cycle (SDLC) Policy](#), ensuring that changes are planned, documented, and reviewed for security and compliance.

## Security by Design for AI

A security-focused approach is required when implementing AI, ensuring systems are designed with functionality, performance, and security in mind.

### Secure Configuration Practices

Every new setting or configuration in AI systems is assessed through a structured due diligence process, including:

- **Assessment of Security Risks**: Identifying potential vulnerabilities.
- **Due Diligence Evaluation**: Ensuring compliance with security policies.
- **Customization for Security**: Adjusting configurations to meet safety standards.
- **Implementation of Controls**: Applying technical measures to enforce secure settings.

### Examples of Secure Configurations

- **Data Use Restrictions**:
  - AI systems must not use data for product improvements without explicit approval.
  - Models must not use group data for training by external providers.
- **Access Limitations**:
  - Only approved users can modify settings or access sensitive features. Refer to the [Access Control Policy](#) for more details.

## Risk Analysis for AI Initiatives

When evaluating AI-related risks, consider both risks to and from AI systems. Key questions include:

- **Compliance**: Does the AI system meet GDPR, the [EU AI Act](https://artificialintelligenceact.eu/), and other relevant regulations?
- **Transparency**: Can the system’s decision-making process be explained clearly?
- **Privacy**: Does the system protect rights like data access, correction, and erasure?
- **Bias**: Are potential biases identified and mitigated?
- **Necessity**: Is AI the best solution, or could a simpler alternative suffice?
- **Data legality**: Is the data lawful and appropriate for its intended use?
- **Behavior controls**: Are safeguards in place to prevent unintended behaviors or harms?

Refer to the [Risk Management Procedure](#) for additional guidance on evaluating and mitigating AI-related risks.

{{< callout context="note" title="Threat modeling in AI risk analysis" icon="outline/info-circle" >}}
Threat modeling is critical for identifying AI threats. It helps address bias, security vulnerabilities, and adversarial behavior proactively.
{{< /callout >}}

## Feedback

The AI Feedback Group on Signal Messenger is available for raising any concerns or suggestions regarding AI tools.

### Providing Constructive Feedback

1. **Describe what was shared with AI**: Clarify the type of data or information provided and any relevant context.
2. **State expected results**: Outline the intended outcome and why it was important.
3. **Provide evidence-based observations**: Highlight areas where the AI tool excelled or fell short, using factual observations.
4. **Focus on actionable suggestions**: Recommend improvements or adjustments to enhance the AI tool’s performance.
5. **Explain the impact**: Share how the AI tool’s performance affected tasks or projects.

{{< callout context="tip" title="Constructive feedback benefits everyone" icon="outline/lightbulb" >}}
Input from users is crucial for refining AI tools and ensuring their reliability, accuracy, and usefulness.
{{< /callout >}}

## Key Takeaways

1. **Exercise Caution**: AI-generated content should always be verified for accuracy and reliability.  
2. **Prioritize Privacy**: Protect sensitive information by anonymizing or sanitizing data before using AI tools.  
3. **Maintain Compliance**: Follow the [Data Classification Policy](#), [Acceptable Use Policy](#), and the [Access Control Policy](#) at all times.  
4. **Use On-Device AI Responsibly**: Remain cautious with external connections that may expose data to third-party systems.  
5. **Report Issues Immediately**: Bias, inaccuracies, or misuse of AI tools must be reported according to the [Incident Response Procedure](#).  
6. **Stay Informed**: Keep up with patch management, vulnerability management, and dependency tracking to preserve the integrity of AI solutions.

Following these guidelines helps ensure that AI usage remains safe, ethically sound, and beneficial for all users.
