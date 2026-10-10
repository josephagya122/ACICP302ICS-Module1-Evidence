ACICP302ICS MODULE 1 – PRACTICAL LAB EVIDENCE

Integrated ICS Network Security & Attacks: Analyze, Test & Recover

LEARNER

Joseph Agyapong

SOURCE

Repository:
ACICP302ICS-Network-Security-and-Attacks
Canonical lab source:
labs/ot-security/student-lab-source/
Verified source commit:
2a66f9bcf253eb3fe31c68ad52794cd535421da8

LAB SCOPE AND SAFETY

This submission comprises of work completed using the supplied ACICP302ICS
OT Security Simulation.

All ICS communications were local to the loopback interface:
127.0.0.1

No production ICS/OT system was targeted in this lab, which used no
bridged interfaces, port forwarding, or external network connectivity.
The archive-original simulator was not run; supplied scripts and default
lab targets were used as-is without modification to target address,
port, request count, duration, or thread counts.
The four services identified in the lab were stopped after testing.

SUBMISSION CONTENTS
FINAL_REPORT/
Complete practical-lab report in MS Word format
evidence/screenshots/
Numbered screenshot files supporting the activities, controlled
demonstrations, guard analysis, and recovery
evidence/pcap/
Baseline Modbus/TCP packet capture from the supplied simulation
docs/
Evidence index and traceability documentation

KEY VALIDATION FINDINGS

Normal plant operations were established using the supplied direct
and guarded dashboards.
Modbus/TCP communications were observed locally via Wireshark.
The direct plant path accepted unsafe false-data values, illustrating
that the direct path does not enforce the same validation as the guard.
The guarded path correctly rejected out-of-range and cumulative-drift
writes.
The supplied guard did not prevent the demonstrated repeated,
identical, in-range replay writes (see final report).
Recovery was verified after the controlled demonstrations.

EVIDENCE
Documented evidence is listed and described in detail in:
docs/EVIDENCE_INDEX.md
The full interpretation, findings, risk assessment, validation results,
recovery observations, and conclusion are contained in:
FINAL_REPORT/ACICP302ICS_Module_1_Practical_Lab_Final_Report.docx

FINAL SAFETY STATE

At completion:
The lab services were stopped.
Listeners on local ports 5020, 5021, 8080, and 8081 were stopped.
The Ubuntu VM’s network interfaces used for external access were
DOWN.
The loopback interface at 127.0.0.1 was still available.
The final working tree was clean.
Verified source commit: 2a66f9bcf253eb3fe31c68ad52794cd535421da8

SUBMISSION NOTE
This repository should remain private and only contain evidence for
assessment purposes and not be shared publicly.
