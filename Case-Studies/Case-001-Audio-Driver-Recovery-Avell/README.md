# Case Study 001

## Executive Summary

This case study documents the investigation and resolution of an audio issue affecting an Avell LIV 62 notebook running Windows 11 Pro 25H2.

After resuming from sleep mode, the operating system lost audio functionality, requiring a full system restart to restore sound.

The investigation identified that Windows was using a generic Microsoft High Definition Audio driver instead of the OEM Realtek driver provided by the manufacturer.

The issue was resolved by installing the official Realtek driver package from Avell, validating the solution through multiple functional tests, including an overnight sleep cycle.

## Environment

| Component | Details |
|----------|---------|
| Device | Avell LIV 62 RTX |
| Operating System | Windows 11 Pro 25H2 |
| Processor | Intel Core i7-10750H |
| Graphics | NVIDIA GeForce RTX 2060 (6 GB) |
| Integrated Graphics | Intel UHD Graphics |
| Audio Hardware | Realtek Audio (OEM) |
| Audio Driver (Before Resolution) | Microsoft High Definition Audio Driver |
| Audio Driver (After Resolution) | Official Realtek Driver provided by Avell |
| Additional Software | THX Spatial Audio |

## Problem Description

The notebook intermittently lost all audio functionality after resuming from sleep mode.

The audio device remained visible in Windows, and the system displayed the normal audio icon without any warning messages or error indicators. However, no sound was produced through the speakers or headphones.

The issue could only be temporarily resolved by restarting the operating system, indicating that the problem occurred during the transition from sleep mode rather than during system startup.

## Symptoms

---

## Initial Investigation

---

## Root Cause Analysis

---

## Corrective Actions

---

## Validation

---

## Lessons Learned

---

## Technical Skills Demonstrated

---

## Commands Used

---

## References
