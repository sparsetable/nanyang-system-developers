# Simple Automation Guidelines for Student Developers

## Overview

Tired of typing the same things over and over, or making the same mouse movements, whenever you run a test, or push a feature?

As programmers, we can write code to carry out these steps, interactively or non-interactively. The environment in which we run programs is called a shell, and many shells also support some form of scripting.

### Common shells and scripting languages

- **Windows**: Command Prompt, [PowerShell](https://learn.microsoft.com/en-us/training/modules/script-with-powershell/), Windows Subsystem for Linux (WSL)
- **Mac**: [Bash](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/), Zsh, AppleScript
- **Linux**: [Bash](https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/), Zsh, Python, Perl

You can save your scripts and run/invoke them from the shell/command line, carrying out many steps with a single stroke!

## Automation

On your own computer, you can schedule your scripts to run at regular intervals.

- **Windows**: [Task Scheduler](https://learn.microsoft.com/en-us/windows/win32/taskschd/about-the-task-scheduler), [PowerShell Scheduled Jobs](https://learn.microsoft.com/en-us/powershell/module/scheduledtasks/new-scheduledtask?view=windowsserver2025-ps)
- **Mac**: [Launchd](https://support.apple.com/en-sg/guide/terminal/apdc6c1077b-5d5d-4d35-9c19-60f2397b2369/mac), [Cron](https://www.redhat.com/en/blog/linux-cron-command)
- **Linux**: [Cron](https://www.redhat.com/en/blog/linux-cron-command), systemd timers

On platforms such as [GitHub Actions](https://github.com/features/actions), or [Google Cloud Run](https://cloud.google.com/run), scripts can be configured to run on certain triggers.

For example, the NYJC Computing static site [has some GitHub Actions configured](https://github.com/nyjc-computing/nyjc-computing.github.io/tree/main/.github/workflows) to test the Markdown files, deploy (publish) them, and synchronize upstream changes to downstream branches.

## Key Principles

When creating small to medium applications, automation should help make your development process easier without adding unnecessary complexity.

### 1. Start Simple
- Automate repetitive tasks like testing and builds
- Keep automation scripts simple and easy to understand
- Focus on time-saving opportunities

### 2. Maintain Control
- Include ways to run processes manually if needed
- Keep automation optional rather than mandatory
- Document how automated processes work

### 3. Focus on Development Tasks
- Automate test runs
- Set up simple build processes
- Create basic deployment scripts
- Automate code formatting and linting

### 4. Test Before Implementing
- Try processes manually first
- Automate only what you understand well
- Start with basic scripts before adding complexity

## Best Practices

1. **Documentation**
   - Write clear comments in automation scripts
   - Document how to run processes manually
   - Keep instructions simple and direct

2. **Testing**
   - Test automated processes thoroughly
   - Have a way to verify results
   - Keep test runs simple and focused

3. **Maintenance**
   - Review automation scripts regularly
   - Update as project needs change
   - Remove unused automation

## Implementation Tips

1. Start with basic task runners
2. Use built-in IDE automation features
3. Keep scripts in a single, organized location
4. Test frequently during development

Remember: For small-to-medium-scale projects, simple and reliable automation is better than complex systems. Focus on automating tasks that directly help your development process.