# GLAB 930.2 — Chronological Transcript

## Task 1: Practical Applications

### USER PROMPT

What are some practical applications of LLMs in enhancing customer support?

### AI RESPONSE

LLMs can enhance customer support in several practical ways:

| Application | Example | Benefit |
|---|---|---|
| **Answer common questions** | Explain return policies, shipping options, or account setup using an approved knowledge base. | Faster answers and fewer repetitive inquiries. |
| **Guide troubleshooting** | Walk a customer through diagnosing a connection problem, adapting to each response. | More personalized assistance. |
| **Assist support agents** | Suggest relevant help articles and draft responses for an agent to review. | Reduces research and writing time. |
| **Summarize conversations** | Convert a long chat into the issue, attempted solutions, and next steps. | Smoother handoffs between agents. |
| **Classify and route tickets** | Identify billing, technical, or cancellation requests and suggest the appropriate queue. | Helps requests reach the right team. |
| **Provide multilingual support** | Translate customer inquiries and draft replies in their preferred language. | Improves accessibility across languages. |
| **Adapt tone and clarity** | Rewrite a technical explanation in plain language or draft an empathetic reply to a frustrated customer. | Clearer, more considerate communication. |
| **Find recurring issues** | Analyze support tickets to identify repeated complaints or gaps in documentation. | Helps teams improve products and self-service resources. |

**A practical starting point:** use an LLM to draft answers from approved support documentation, with human review. Connect it to authorized systems when account-specific information or actions are needed, and provide a clear path to a human when it cannot resolve the issue.

## Task 2: Identifying Limitations

### USER PROMPT

What limitations do LLMs face when handling customer support inquiries? Please provide specific examples.

### AI RESPONSE

LLMs can help with routine customer support, but they may struggle with ambiguity, accuracy, emotional nuance, and situations requiring human judgment.

| Limitation | Specific example | Potential consequence |
|---|---|---|
| **Misunderstanding context** | A customer says, “I already reset it twice,” but the LLM recommends another reset without clarifying what was reset. | Repetitive advice frustrates the customer and delays resolution. |
| **Providing irrelevant information** | A customer reports a duplicate charge, but the LLM explains how to update a payment method. | The response sounds helpful but does not address the issue. |
| **Generating incorrect information** | Without access to the company’s policy, the LLM confidently states that all purchases qualify for a refund within 60 days. | Customers may rely on an invented policy. |
| **Missing nuanced emotions** | A customer says, “Wonderful—another delivery that never arrived,” and the LLM interprets the sarcasm as satisfaction. | An overly cheerful reply can worsen frustration. |
| **Limited human empathy and judgment** | A bereaved customer needs help closing a relative’s account, but the LLM gives a generic checklist without acknowledging the loss or recognizing the need for sensitive assistance. | The interaction can feel impersonal or insensitive. |
| **Insufficient domain-specific knowledge** | A customer asks whether an unusual equipment fault is safe to ignore, and the LLM offers generic troubleshooting without verified product guidance. | The advice may be unsuitable or unsafe. |
| **Lack of access to current account data** | A customer asks where an order is, but the LLM has no connection to the order-management system. | It cannot verify the shipment’s actual status. |
| **Limited authority to take action** | The LLM says, “Your subscription has been canceled,” although no authorized cancellation tool was used. | The customer believes an action occurred when it did not. |
| **Difficulty maintaining conversation details** | During a long exchange, the LLM overlooks that the customer already supplied the order number and asks for it again. | Customers must repeat themselves, reducing trust. |

**For example, a complex billing dispute** might involve a duplicate charge, an expired promotion, and an earlier refund promise. An LLM could summarize the evidence and draft a response, but a human agent may need to verify records, interpret policy exceptions, and authorize a resolution.

To manage these limitations, support systems should use verified documentation, authorized account tools, clarifying questions, and clear escalation to human agents. Empathetic wording is useful, but it does not guarantee that the model understands the customer’s emotions or circumstances.

## Task 3: Crafting Effective Prompts

### USER PROMPT

How can I formulate prompts to improve the quality of responses I get from an LLM in a customer support scenario?

### AI RESPONSE

To improve customer support responses, give the LLM **clear context, a specific goal, verified information, and response constraints**. These instructions help address the relevance, accuracy, and emotional-awareness limitations discussed earlier.

| Prompting technique | What to include | Why it helps |
|---|---|---|
| **Define the role** | “Act as a customer support assistant for an online retailer.” | Establishes the support setting. |
| **Provide context** | The customer’s message, relevant order facts, and troubleshooting already attempted. | Reduces assumptions and repetitive advice. |
| **Specify the outcome** | “Explain return eligibility and the next step.” | Keeps the response focused on the customer’s need. |
| **Supply verified information** | The applicable policy or approved help article. | Gives the model evidence to use. |
| **Set boundaries** | “Do not invent policies or claim an action was completed.” | Reduces unsupported statements. |
| **Specify tone and format** | “Use empathetic, plain language; stay under 120 words.” | Makes the response easier for the customer to understand. |
| **Handle missing information** | “Ask a clarifying question if eligibility cannot be determined.” | Encourages clarification instead of guessing. |

For example, consider this **hypothetical return inquiry**.

**Ineffective prompt:**

> Help a customer return something.

This leaves out the customer’s concern, purchase details, policy, and desired next step. The response may be generic or based on assumptions.

**Effective prompt:**

> Act as a customer support assistant for an online retailer.  
> Customer message: “These headphones don’t work. I received them 10 days ago and want my money back.”  
> Approved policy: Defective products may be returned within 30 days of delivery. An order number is required to begin a return request.  
> Draft a reply that acknowledges the inconvenience, explains eligibility under the supplied policy, and asks for the order number. Use friendly, professional language and stay under 100 words. Do not claim that a return or refund has already been processed.

**Example response to the effective prompt:**

> I’m sorry the headphones aren’t working. Based on our policy, defective products received 10 days ago are eligible for a return within the 30-day window. Please provide your order number so we can begin your return request.

Another useful comparison involves troubleshooting:

| Ineffective prompt | Effective prompt |
|---|---|
| “Fix the customer’s Wi-Fi.” | “The customer’s laptop cannot connect to Wi-Fi, but their phone connects successfully. They already restarted the laptop and router. Ask which operating system they use before suggesting the next troubleshooting step. Do not repeat the completed steps.” |

**Refine prompts using observed results.** If the reply repeats advice, explicitly list completed steps. If it misses the customer’s main concern, name that concern and prioritize it. If it invents details, restrict the answer to supplied sources and require it to acknowledge missing information.

Clear prompts improve guidance, but they do not guarantee correctness. Review responses for **accuracy, relevance, tone, and an actionable next step** before using them with customers.

### Task 3 — Vague Return-Prompt Experiment

#### USER PROMPT

Help a customer return something.

#### AI RESPONSE

I can help with your return. What item would you like to return, which store did you purchase it from, when did you receive it, and why would you like to return it?

### Task 3 — Improved Return-Prompt Experiment

#### USER PROMPT

For this hypothetical exercise, act as a customer support assistant for an online retailer.

Customer message: “These headphones don’t work. I received them 10 days ago and want my money back.”

Supplied policy: Defective products may be returned within 30 days of delivery. An order number is required to begin a return request.

Draft a customer-facing reply that acknowledges the inconvenience, explains return eligibility under the supplied policy, and asks for the order number. Use friendly, professional language and stay under 100 words. Do not invent additional policies or claim that a return or refund has already been processed.

#### AI RESPONSE

I’m sorry your headphones aren’t working—that’s frustrating. Since you received them 10 days ago, they’re eligible for a return under our policy allowing defective products to be returned within 30 days of delivery. Could you please provide your order number so we can begin your return request?

## Task 4: Ethical Considerations in AI

### USER PROMPT

What ethical considerations should be taken into account when implementing LLMs in customer support roles?

### AI RESPONSE

Implementing LLMs in customer support requires protecting customer information, treating people fairly, and keeping humans accountable for the service provided.

| Ethical consideration | Example concern | Responsible practice |
|---|---|---|
| **Data privacy and security** | A customer shares an address or payment details, which could be exposed through inappropriate storage or access. | Collect only necessary data, redact sensitive information, restrict access, and clearly explain how conversations are used and retained. |
| **Bias and fairness** | The model provides less helpful responses to customers using nonstandard grammar, different dialects, or another language. | Test across diverse customer groups and languages, investigate unequal outcomes, and apply policies consistently. |
| **Transparency** | Customers believe they are speaking with a human or that the AI has verified their account when it has not. | Identify the assistant as AI and explain its capabilities, limitations, and whether information has been verified. |
| **Accuracy and honesty** | The assistant invents a refund policy or says a cancellation is complete without performing it. | Use approved sources, acknowledge uncertainty, and confirm actions only after verified system results. |
| **Human oversight and accountability** | An automated assistant incorrectly denies a return, with no way for the customer to challenge it. | Assign responsible staff, review consequential decisions, and provide an accessible human escalation and appeal process. |
| **Respect and emotional sensitivity** | A distressed customer receives a dismissive response or repetitive scripted advice. | Use respectful language, avoid assuming emotions, and escalate sensitive or complex situations to trained agents. |
| **Customer autonomy** | The assistant pressures a customer to keep a subscription or makes cancellation unnecessarily difficult. | Present options clearly, avoid manipulation, and respect the customer’s stated goal. |
| **Accessibility** | Customers with disabilities or limited technical skills cannot use the AI support channel effectively. | Offer clear language, accessible interfaces, and alternative support channels. |

In the **headphone-return example**, an ethical assistant should explain eligibility using the supplied policy, request only the information needed to begin the return, and avoid claiming that a refund has been processed. In a real deployment, account details should be collected through an appropriate secure channel.

**Human oversight must be meaningful:** staff should be able to review the evidence, correct errors, and override inappropriate outcomes. Customers should not become trapped in an automated conversation when they need human assistance.

## Task 5: Case Study Reflection

### USER PROMPT

Can you summarize a successful case study of LLM implementation in customer support and what lessons can be learned from it? , Use a real, named organization and provide source links. Include reported success metrics, challenges, solutions, and lessons I could apply to a small business’s customer support. Distinguish company-reported results from independently verified findings, and note any later developments that qualify the success claims.

### AI RESPONSE — Original Progress Message

I’ll check a documented case and later developments so the results are presented with their limits.

### AI RESPONSE — Complete Original Answer

**Klarna is a useful case of reported efficiency gains—with later developments showing why human support still matters.** The payments company launched an OpenAI-powered assistant in early 2024 to handle inquiries about payments, returns, refunds, and other support issues. Customers could still choose a live agent. [www.prnewswire.com](https://www.prnewswire.com/news-releases/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month-302072744.html?utm_source=chatgpt.com)

**Reported success metrics**

Klarna’s February 27, 2024 announcement reported the following results after its first month:

| Metric | Company-reported result |
|---|---|
| Volume | 2.3 million conversations, covering two-thirds of customer service chats |
| Resolution time | Under 2 minutes, compared with 11 minutes previously |
| Repeat inquiries | Reduced by 25% |
| Customer satisfaction | On par with human agents |
| Capacity | Work equivalent to 700 full-time agents |
| Availability | 24/7 across 23 markets and more than 35 languages |

These figures came from **Klarna’s own press release**, rather than an independent evaluation. “Equivalent work” is a capacity estimate, not evidence that 700 particular employees were replaced. [www.prnewswire.com](https://www.prnewswire.com/news-releases/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month-302072744.html?utm_source=chatgpt.com)

**Challenges, solutions, and later qualifications**

The initial solution offered multilingual, always-available assistance inside Klarna’s app. However, complex conversations remained a challenge. In a May 2025 interview with *Big Technology*, the CEO described hiring humans for more demanding conversations while continuing to expand AI use. He also acknowledged that his expectations about the speed of AI progress had been overly optimistic. [www.bigtechnology.com](https://www.bigtechnology.com/p/klarna-ceo-were-giving-ai-more-customer?utm_source=chatgpt.com)

In September 2025, Reuters reported that Klarna was reassessing its emphasis on AI and cost reduction following concerns about service quality. This qualifies the early success narrative: faster handling and lower costs do not necessarily establish better service across every kind of inquiry. [www.reuters.com](https://www.reuters.com/business/europes-ai-poster-child-klarna-taps-brakes-chatbots-2025-09-10/?utm_source=chatgpt.com)

Klarna nevertheless continued using AI extensively. Its **2025 annual report** stated that the assistant handled 80% of customer service chats during 2025 and delivered $39 million in cost savings in 2024. Those remain company-reported figures based on internal data. The $39 million cost-savings figure should also be distinguished from the original $40 million **projected profit improvement**. [s205.q4cdn.com](https://s205.q4cdn.com/644747736/files/doc_financials/2025/q4/Klarna-Group-plc-20-F-2025.pdf?utm_source=chatgpt.com)

**What is independently established?**

Independent journalism documents Klarna’s reassessment and executive statements. It does **not independently validate the underlying resolution-time, satisfaction, or savings calculations**. I did not find an independent audit of those support-performance metrics in the sources reviewed.

**Lessons for a small business — my recommendations**

- **Start with routine questions:** opening hours, delivery policies, basic troubleshooting, and return eligibility.
- **Use approved information:** supply current policies and product documentation; require clarification when facts are missing.
- **Keep human access easy:** escalate disputes, exceptions, repeated failures, and emotionally sensitive cases.
- **Measure quality alongside speed:** track incorrect answers, repeat contacts, customer satisfaction, and successful resolutions.
- **Pilot before expanding:** begin with AI-drafted replies reviewed by staff, then automate only the tasks that perform reliably.

For the headphone-return scenario, a sensible starting point is letting AI explain the documented return policy and request the necessary order information, while staff handle exceptions and refund authorization.

Source links: [Klarna’s original announcement](https://www.prnewswire.com/news-releases/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month-302072744.html), [May 2025 CEO interview](https://www.bigtechnology.com/p/klarna-ceo-were-giving-ai-more-customer), [Reuters’ September 2025 report](https://www.reuters.com/business/europes-ai-poster-child-klarna-taps-brakes-chatbots-2025-09-10/), and [Klarna’s 2025 annual report](https://s205.q4cdn.com/644747736/files/doc_financials/2025/q4/Klarna-Group-plc-20-F-2025.pdf).

## Task 6: Summarizing Insights and Lessons

### USER PROMPT

As we conclude, what are the key insights and lessons learned about the applications and limitations of LLMs in customer support?

### AI RESPONSE

**The main lesson is that LLMs can improve customer support when they use verified information, receive clear instructions, and operate with meaningful human oversight.**

| Area | Key insight and lesson |
|---|---|
| **Practical applications** | LLMs can answer common questions, guide troubleshooting, draft replies, summarize conversations, translate messages, and help route tickets. These applications can reduce repetitive work and support agents. |
| **Inherent limitations** | They can misunderstand context, overlook emotional nuance, repeat irrelevant advice, and generate confident but incorrect information. Fluent language does not guarantee accuracy or understanding. |
| **Effective prompting** | Provide the customer’s message, relevant facts, approved policies, desired outcome, tone, and boundaries. Tell the model to ask questions when information is missing. |
| **Verified information and actions** | An LLM needs authorized system access to verify order status or perform account actions. It should never claim that a refund or cancellation occurred without confirmation. |
| **Ethical responsibilities** | Protect personal information, test for unequal treatment, disclose AI involvement, communicate respectfully, and offer accessible human assistance. |
| **Evaluating success** | Measure accuracy, customer satisfaction, repeat contacts, and actual resolution alongside speed and cost. Distinguish company-reported claims from independent validation. |

Our **return-prompt experiment** demonstrated the value of specificity. The vague prompt produced clarifying questions; it did not invent a policy, but it could not give a tailored answer. The detailed prompt supplied enough information to acknowledge the inconvenience, explain return eligibility, and request the order number without falsely claiming a refund had been processed.

The **Klarna case** illustrated why efficiency claims need qualification. Klarna reported substantial automation gains, while later reporting documented a reassessment of cost-focused AI adoption and renewed emphasis on human support. Its continued AI use supports a lesson about balancing automation with service quality. [s205.q4cdn.com](https://s205.q4cdn.com/644747736/files/doc_financials/2025/q4/Klarna-Group-plc-20-F-2025.pdf?utm_source=chatgpt.com)

For a future small-business implementation, my recommendation is to **begin with a narrow pilot using AI-drafted replies reviewed by staff**, maintain approved documentation, and expand only after measuring reliable results.

For your personal reflection, consider: **Which inquiries could AI handle reliably, which require human judgment, and what evidence would convince you that customers are receiving better support?**