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

- Audio icon displayed normally in the Windows taskbar.
- No audio output from the internal speakers.
- No audio output from external audio devices.
- No warning messages or error notifications were displayed.
- Windows detected the audio device correctly.
- Audio functionality was temporarily restored after restarting the system.
- The issue consistently occurred after the notebook resumed from sleep mode.

## Initial Investigation

### Step 1 — Verify the Operating System Detection

**Objective**

Confirm whether Windows was correctly detecting the installed audio hardware.

**Action**

Opened Device Manager and inspected all audio devices, drivers, and hardware status.

**Result**

Windows successfully detected the audio hardware, and no warning icons or hardware errors were present.

**Decision**

Since the hardware was correctly detected, the investigation shifted to the installed audio driver.

---

### Step 2 — Identify the Installed Audio Driver

**Objective**

Determine whether Windows was using the OEM audio driver or a generic Microsoft driver.

**Action**

Collected driver information using Device Manager and Windows command-line diagnostic tools.

**Result**

The notebook was using the Microsoft High Definition Audio Driver instead of the official Realtek OEM driver provided by Avell.

**Decision**

Investigate the availability of the official manufacturer driver package.

## Root Cause Analysis

The investigation determined that the operating system was using the generic Microsoft High Definition Audio Driver instead of the OEM Realtek driver provided by Avell.

Although the generic driver provided basic audio functionality, it did not correctly manage the hardware state transition after the notebook resumed from sleep mode.

As a result, Windows continued to recognize the audio device, but the audio subsystem failed to restore normal sound output until the operating system was restarted.

Installing the official Realtek OEM driver restored proper communication between Windows and the audio hardware, permanently resolving the issue.

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
