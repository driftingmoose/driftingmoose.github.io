---
title: Best Practices
layout: home
nav_order: 2
---

# Best Practices

## Table of Contents

- [Add Project Information to the Prompt](#add-project-information-to-the-prompt)
- [User Files as References](#use-files-as-references)
- [Add Documentation to Your Requests](#add-documentation-to-your-requests)
- [Generate Only What You Need](#generate-only-what-you-need)
- [One File – One Generation](#one-file--one-generation)
- [Ask for Feedback on Code Quality and Project Structure](#ask-for-feedback-on-code-quality-and-project-structure)
- [Use Code Buddy for Planning Modules and Projects](#use-code-buddy-for-planning-modules-and-projects)
- [Focuse on 'Why' When Debugging](#focus-on-why-when-debugging)

## Add Project Information to the Instructions

Think of the prompt not just as a set of instructions but as an opportunity to inform the AI about your project and yourself. Providing details like genre, platform, graphics style, and project scope will make code generation more consistent and tailored to your needs. The same applies to your experience level, explanation details, code complexity preferences, and approaches. Use the instrucitons settings actively as a static context source for your project or task.

## Use Files as References

Describing functionality in words can take too much time. If you have an example code from your project that follows a similar structure, style, or logic, attach it to your request and ask the AI to replicate or follow the relevant part. This saves a lot of time in explaining code nuances.

## Add Documentation to Your Requests

When working with third-party assets, extensions, or new APIs, Code Buddy might misuse external functions that are not part of the project context. AI models have a knowledge delay, lack real-time validation, and the current version of Code Buddy doesn’t search for missing information online. If you notice that generated code misuses external dependencies or Unity classes, simply paste the relevant part of the documentation into your request and ask the AI to use that information for generation. This resolves issues in 99% of cases.

## Generate Only What You Need

Even with fast models, once the file exceeds 100 lines, waiting for regeneration and tracking changes becomes difficult. If you need to add a single method or fix a few lines, request exactly that. The process will be faster, smoother, and easier to manage.

## One File – One Generation

This is my personal rule, proven effective. AI models, despite what their creators claim, quickly start losing track of task details, forgetting nuances, and making or repeating mistakes. Additionally, Code Buddy gathers project context only at the start of a new chat and then relies solely on messages for updates. Shorter conversations provide much more usable results for any task, whether generating from scratch or modifying code.

## Ask for Feedback on Code Quality and Project Structure

Large models have a solid foundation in project architecture and code quality. If your project is growing and implementing changes is becoming harder, ask Code Buddy to review your class structure or attach a file and request potential refactoring suggestions. It often provides valuable advice and a plan for making improvements.

## Use Code Buddy for Planning Modules and Projects

When starting new functionality or projects, ask Code Buddy to create a plan with class lists, interactions, and prompts. This allows you to iterate on the structure that best fits your needs without spending time on generation and coding. The result is a well-prepared list of classes with instructions for generation.

## Focus on "Why" When Debugging

AI models know a lot but understand very little. If you face a complex issue, ask Code Buddy to describe possible causes instead of simply fixing the code. This helps you better understand what’s happening in the project and speeds up troubleshooting.

Often, if an AI’s first attempt doesn’t fix an issue, it starts adding workarounds and overcomplicating the code. Understanding the problem yourself protects you from such situations.

This, of course, doesn’t apply to simple typos and AI hallucinations—Code Buddy handles those effortlessly.
