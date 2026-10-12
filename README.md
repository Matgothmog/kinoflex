# Synchronised Multi-camera Video Capture with a Distributed Fleet of 10 Raspberry Pi Cameras: Architecture, Synchronisation, and Evaluation Methodology

Report by Matteo Pecher, written during an internship at Inria Grenoble (Morpheo team) as part of the M1 MoSIG programme at Univ. Grenoble Alpes / Grenoble INP — Ensimag. Supervisor: Julien Pansiot (Inria Grenoble). Submitted 5 June 2026.

## About

KinoFlex is a low-cost synchronised capture rig built from Raspberry Pi 5 boards, each fitted with a Sony IMX296 global-shutter camera. A Raspberry Pi Pico microcontroller broadcasts a shared external-trigger pulse at 60 fps. The planned rig has 80 nodes; this report covers stage 1, a 10-node fleet.

The report makes two contributions:

- **The system.** A hardware-triggered acquisition pipeline with on-node delta+zstd compression, an MQTT-based orchestration plane, a PySide6 supervisor GUI, parallel SCP export, and an Ansible-based deployment layer.
- **The evaluation methodology.** A three-tier test suite (unit, deployment, chaos) and a synchronisation-comparison protocol that benchmarks free-run, NTP, libcamera master/slave and the hardware trigger against an LED probe panel used as ground truth.

## Report

[Pecher.pdf](Pecher.pdf) (15 pages, English)
