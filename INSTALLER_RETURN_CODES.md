# CHI AI Assistant — Installer Return Codes

**Product:** CHI AI Assistant v1.0  
**Installer technology:** Inno Setup  
**Platform:** Windows

## Overview

This document describes the standard exit codes returned by the Inno Setup installer used to distribute CHI AI Assistant.

A return code of `0` indicates successful completion. A non-zero return code indicates that setup did not complete normally, or that setup was stopped or terminated.

## Standard Inno Setup Exit Codes

| Exit code | Meaning | Recommended action |
|---|---|---|
| `0` | Setup completed successfully. | No action required. |
| `1` | Setup failed to initialize. | Check the installer file and Windows environment, then retry. |
| `2` | The user cancelled before the installation began. | Run the installer again if installation is desired. |
| `3` | A fatal error occurred while preparing for the next installation phase. | Retry and check available system resources if the error persists. |
| `4` | A fatal error occurred during installation. | Check the displayed error message and installation logs. |
| `5` | The user cancelled during installation or selected Abort in an Abort-Retry-Ignore dialog. | Restart installation if desired and resolve any underlying error. |
| `6` | Setup was forcefully terminated by the debugger in the Inno Setup IDE. | If this occurred during development, run the compiled installer normally. |
| `7` | The Preparing to Install stage determined that setup cannot proceed. | Read the displayed error message and resolve the reported issue. |
| `8` | Setup cannot proceed, and a system restart is needed to correct the problem. | Restart Windows and try again. |

## Additional and Custom Exit Codes

The codes listed above are the standard Inno Setup setup exit codes. CHI AI Assistant does not claim to use any additional custom installer exit codes unless they are explicitly configured and verified in its Inno Setup script.

Future versions of Inno Setup may introduce additional codes. Unexpected non-zero codes should be recorded and investigated rather than assumed to have a known meaning.

## Troubleshooting

1. Record the exit code displayed by the calling application or deployment system.
2. Read any error message shown by the installer.
3. Retry the installation after addressing the reported problem.
4. If the problem persists, record the installer version, Windows version, and steps that caused the failure.

## Official Reference

Inno Setup — Setup Exit Codes:  
https://jrsoftware.org/ishelp/topic_setupexitcodes.htm

## Project Links

CHI AI Assistant website:  
https://sites.google.com/view/chi-ai-assistant

CHI AI Assistant releases:  
https://github.com/riteshphoto01-ship-it/CHI-AI-Assistant/releases
