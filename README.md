# EternalBlue-Exploit-Prevention
# Overview

This project focuses on hardening a Windows system to mitigate the EternalBlue vulnerability (MS17-010), a critical flaw in the SMBv1 protocol that enabled widespread ransomware outbreaks such as WannaCry. The goal of this work was to reduce attack surface and prevent exploitation through defensive system configuration rather than exploit development.

The project was completed in a controlled lab environment and emphasizes practical defensive security principles used in real-world system administration and cybersecurity roles.

## Background

EternalBlue is a remote code execution vulnerability that targets legacy implementations of SMBv1. Systems that are unpatched or improperly configured are vulnerable to exploitation and lateral movement within a network.

Because SMBv1 is deprecated and inherently insecure, effective mitigation requires a layered defensive approach rather than reliance on a single control.

## Mitigation Approach

The system was hardened using multiple defensive measures, including:

Disabling legacy SMBv1 services to remove the vulnerable attack vector

Verifying system patch status related to MS17-010

Reviewing firewall configuration to limit unnecessary SMB network exposure

Applying general system hardening principles to reduce attack surface

These steps reflect defense-in-depth practices commonly used to mitigate known vulnerabilities in enterprise environments.

## Evaluation

Mitigation effectiveness was evaluated in a lab setting by observing system behavior following hardening steps. The focus of evaluation was on confirming that vulnerable services were disabled and that network exposure was appropriately restricted.

This project emphasized understanding why each mitigation step is effective rather than relying solely on automated tools.

## Tools & Technologies

Windows operating system (lab environment)

System configuration and service management

Firewall configuration concepts

Vulnerability research and documentation (MS17-010)
