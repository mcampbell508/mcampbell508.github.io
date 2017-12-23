---
layout: post
title:  "My experience and recommendations for internal documentation"
date:   2017-12-17 15:20:59 +0000
tags: documentation wiki developer team
---

Here are some of my recommnendations for pages that could help improve overall knowledge, for new & current team members. Maybe you won't need all of them, as situations will differ from one team to another.

These pages are intended to help team members find things for themselves before having to ask other team members for help. **However, asking for help should always be encouraged**, especially for new team members.

The following pages are primarily designed for **Developers**, but some could be appropriate for other departments in a company.

- **Environment setup**
    - This will depend on the circumstances but if a Virtual Machine is used, then a small guide might be helpful on how to appropriately set up the build environment, locally.
- **Internal systems and tools**
    - This will include information about internal tools used within a team. This could be things like:
        - Where are Git repositories stored remotely
        - Server details
        - Communication tools like Slack
        - Info about issue tracking systems used like Jira, Trello or Fogbugz
- **Git Workflow**
    - This should include information about any prefered styles of using Git ranging from:
        - Git branching strategies
        - Whether or not rebasing is used
        - Formatting Git commit messages to include as much information as possible.
        - Whether or not including issue numbers (JIRA) in commit messages, is recommended.
        - Whether the team follows community guidelines
            - [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
            - [5-useful-tips-for-a-better-commit-message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
- **Helpful tools and hidden gems**
    - This should include things if internal tools or code has been written to aid other members of the team. E.g you can use X if you need to Y, as this tool has been written to do so.
- **FAQs**
    - Self-explanatory, this should include Questions and Answers based on commonly asked questions. The questions could be incrementally built up when new members join the team.
- **Glossary of terms and abbreviations**
    - It will depend if abbreviations are used throughout the team - common terms should be documented here, with brief explanations.
- **Domain Knowledge**
    - This should relate to information relating to the domain of the business.
- **Common naming conventions**
    - If the team follows any naming conventions, such as use `camelCase` when using variables or please create databases `with_underscores`.
- **Code Style PHP**
    - This is specific to PHP, but this should probably include information about any agreed code styles such as PSR1&2.
- **Code Style JavaScript**
    - Similar to above, code style agreed for JS.

### References

I saw a while back on [Twitter](https://twitter.com/dhh/status/859417818261069824?lang=en) that [David Heinemeier Hansson \(DHH\)](https://twitter.com/dhh), publicly shared the [BaseCamp Employee Handbook](https://github.com/basecamp/handbook).
