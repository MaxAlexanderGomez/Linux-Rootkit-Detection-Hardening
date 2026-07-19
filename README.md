# Linux-Rootkit-Detection-Hardening
Project evaluating Linux rootkit detection tools and system-hardening techniques in an isolated Ubuntu virtual machine
# Linux Rootkit Detection and System Hardening

## Overview

This senior capstone project evaluates Linux rootkit-detection and
system-hardening techniques in an isolated Ubuntu virtual machine.

The project tested open-source security tools and used an LD_PRELOAD
demonstration to simulate user-space behavior associated with rootkits.

## Objectives

- Build an isolated Ubuntu testing environment using VirtualBox
- Evaluate chkrootkit, rkhunter, and Lynis
- Demonstrate user-space library hooking with LD_PRELOAD
- Compare tool results before and after the simulation
- Apply system-hardening measures using UFW and Linux security practices

## Tools and Technologies

- Ubuntu Linux
- VirtualBox
- chkrootkit
- rkhunter
- Lynis
- UFW
- Bash
- C
- LD_PRELOAD

## Project Methodology

1. Created a clean Ubuntu virtual machine.
2. Installed and ran the security assessment tools.
3. Recorded baseline results.
4. Tested an educational LD_PRELOAD demonstration.
5. Re-ran the assessment tools and documented the results.
6. Applied system-hardening measures and reviewed the final security posture.

## Key Findings

The tools produced different warnings and levels of visibility.
The project demonstrated that automated rootkit scanners should be combined
with system auditing, configuration hardening, and manual investigation.

## Ethical Use

This project was completed for educational and defensive cybersecurity
purposes in an isolated virtual environment. It is not intended for use
against systems without authorization.

## Author

Max Gomez  
B.A. Computer Technology, California State University, Dominguez Hills



linux-rootkit-detection-hardening/
├── README.md
├── src/
│   └── preload_demo.c
├── scripts/
│   └── hardening_commands.sh
├── screenshots/
│   ├── chkrootkit-results.png
│   ├── rkhunter-results.png
│   └── lynis-results.png
├── report/
│   └── senior-project-report.pdf
└── presentation/
    └── senior-project-slides.pdf
