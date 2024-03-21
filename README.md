# GitHub Copilot Case Study

## Overview and Origin

This case study is on GitHub Copilot

GitHub Copilot's initial technical preview launched June 29, 2021.

GitHub Copilot was developed in collaboration between GitHub and OpenAI.

GitHub engineers had ideas for code generation as AI was developing, but it wasn't until 2020 that they found a model to be good enough for code generation with the release of GPT-3. They tested and prototyped, and found an implementation integrated in an IDE promising. Work continued in the GitHub Next team and resulted in Copilot.

GitHub Copilot earns revenue through subscriptions, with plans for individuals, businesses, and enterprise. From Microsoft's 2024 second quarter earnings conference:

> We now have over 1.3 million paid GitHub Copilot subscribers, up 30% quarter-over-quarter.
>
> &mdash; _Satya Nadella_

With the lowest cost plan at $100 a year, that could be more than $130 million yearly earnings.

## Business Activities

GitHub Copilot aims to elevate the developer workflow for productivity and quality. It provides intelligent code completion and code generation from natural language.

GitHub Copilot is for Software engineers and developers at all experience levels. Statistics had over 26 million software developers worldwide in 2021.

GitHub Copilot is tuned for programming tasks where other models like ChatGPT are built for natural language tasks. GitHub also works to tightly integrate Copilot with its other services (repositories, pull requests, actions, mobile, etc.) and can closely work with Visual Studio & VS Code as these editors&mdash;like GitHub&mdash;are owned by the same company, Microsoft.

GitHub Copilot uses OpenAI's Codex model&mdash;a descendant of GPT-3. Codex is specifically trained with lines of public code to generate code from text prompts. Training with public code means Codex supports many of the most popular languages. GitHub then does communications to the underlying LLM to improve Copilot's quality.

## Landscape

GitHub Copilot is in Software Development and Artificial Intelligence fields. To try defining something more specific to compare, it's in Intelligent Code Completion.

AI-powered intelligent code completion is fairly new, so I was not able to find well formatted research over a long period of time. So far, major innovations would be the features provided by AI coding tools:

* Autocomplete list of options that prioritizes by interpreting surrounding context rather than alphabetical order
* Generating code snippets from natural language prompts
* Interpreting code to describe in natural language
* Answering queries on the content of a repository
* Initially supporting popular programming languages, but expanding support to more languages

Other notable AI code completion tools include:

* Amazon CodeWhisperer
* Visual Studio IntelliCode
* YouCode
* Tabnine
* Kite

## Results

In the Microsoft 2024 second quarter earnings call, over 50,000 organizations have business subscriptions. Accenture was highlighted for plans to roll out GitHub Copilot to 50,000 of its developers this year.

Intelligent Code Completion has success measured from a mixture of developer opinion and performance improvements. GitHub has their own rubric to evaluate this, aligning with academic and industry standards:

* **Readable**: does code follow language idioms and naming patters?
* **Reusable**: is code written so it can be reused?
* **Concise**: does code adhere to Don't Repeat Yourself?
* **Maintainable**: is code written in a way that's clear, transparent, and relevant?
* **Resilient**: does code anticipate and handle errors?

The GitHub Blog shared on October 10, 2023 some of its research results for GitHub Copilot (and a recent feature, Copilot Chat):

* 85% of developers reported more confidence in code quality when using Copilot
* Code reviews were completed 15% faster

That reads as a net benefit to developers, especially for perceived code quality.

In _Evaluating the Usability and Functionality of Intelligent Source Code Completion Assistants: A Comprehensive Review_, a survey was conducted to answer various research questions, including a question about intelligent source code completion assistants available and their functionality. GitHub Copilot was found the most advanced, followed by Tabnine, Kite, and IntelliCode.

## Recommendations

GitHub already has shared plans for feature additions for what they call Copilot X:

* A chat window to interact like ChatGPT
* Generating descriptions for pull requests
* Learn from and answer questions about documentation
* Run in the command line to generate commands

These all touch parts of a developer workflow outside the code editor, so I'd advise expanding more into complex and vital workflows.

I could see a tool made for Developer Operations to aid in responding to issues in production, like parsing and summarizing logs to highlight what's happening and describe it in natural language.

A large amount of Copilot customers are tech businesses seeing value in investing in a tool for developer productivity. They're motive in this is to rapidly release features and bug fixes so their services stay competitive. Tech companies also have high motivation to have their services stable, often measured as uptime&mdash;a percentage of how long the service has not been down or inaccessible over the year. Developer Operations is responsible for prioritizing this uptime through promoting code quality and controlling code deployment with automated testing. Sometimes though, DevOps have to handle emergencies when they happen, diagnosing and addressing errors in production as fast as possible to mitigate loss in uptime. The existing way to improve the responsiveness of DevOps is having experienced senior developers familiar with the codebase, architecture, and tools used, which isn't easy to control or improve. If Copilot could improve the DevOps workflow with faster response times, it could draw in customers that prioritize stability.

It would likely require a model trained on the formatting of log files, with examples of logs from various server side programs and code languages. The model should be made private and bespoke per company as logs are expected to hold private company information.

GitHub Copilot already relies on a model specially trained with lines of code as other models don't prioritize code. Log files are not code but also not just natural language; typically they may refer to lines of code or error types typical in a programming language within some natural language and informational data (especially timestamps). A Copilot for logs should develop a similar special-use model to be able to reach the level of quality Copilot currently provides.

## References

[GitHub Copilot landing page](https://github.com/features/copilot)

Friedman, Nat. "Introducing GitHub Copilot: your AI pair programmer." _The GitHub Blog_, 29 June 2021, https://github.blog/2021-06-29-introducing-github-copilot-ai-pair-programmer/.

Verdi, Sara. "Inside GitHub: Working with the LLMs behind GitHub Copilot." _The GitHub Blog_, 17 May 2023, https://github.blog/2023-05-17-inside-github-working-with-the-llms-behind-github-copilot/.

Rodriguez, Mario. "Research: Quantifying GitHub Copilot's impact on code quality." _The GitHub Blog_, 10 October 2023, https://github.blog/2023-10-10-research-quantifying-github-copilots-impact-on-code-quality/.

Dohmke, Thomas. "GitHub Copilot X: The AI-powered developer experience." _The GitHub Blog_, 22 March 2023, https://github.blog/2023-03-22-github-copilot-x-the-ai-powered-developer-experience/.

"Microsoft Fiscal Year 2024 Second Quarter Earnings Conference Call." _Microsoft_, 30 January 2024, https://www.microsoft.com/en-us/investor/events/fy-2024/earnings-fy-2024-q2.aspx.

Lindner, Jannik. "Must-Know Software Developers Statistics." _Gitnux_, 16 December 2023, https://gitnux.org/software-developers-statistics/.

Williams, Alexander T. "Top 5 Code Completion Services." _The New Stack_, 20 July 2023, https://thenewstack.io/top-5-code-completion-services/.

Hliš, Tilen, et al. "Evaluating the Usability and Functionality of Intelligent Source Code Completion Assistants: A Comprehensive Review." _Applied Sciences_, vol. 13, no. 24, 7 December 2023, p. 13061, https://doi.org/10.3390/app132413061.
