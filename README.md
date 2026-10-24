# PRPForge Pro (v1.0.0)

**IEC 62439-3 PRP / HSR Substation Network Redundancy Studio & Duplicate Discard Sizer**

---

## Executive Summary

**PRPForge Pro** is an industrial-grade, client-side engineering workbench and command-line utility for designing, synthesizing, simulating, and validating **IEC 62439-3 Parallel Redundancy Protocol (PRP \- Clause 4\)** and **High-Availability Seamless Redundancy (HSR \- Clause 5\)** networks.

Targeting substation network engineers, protection & control specialists, FPGA/embedded firmware developers, and industrial IT/OT architects, PRPForge Pro automates:

- **PRP RCT & HSR Tag Synthesis**: Encodes byte-exact 6-byte Redundancy Control Trailers (RCT Suffix `0x88FB`, sequence counters, LAN ID `0xA`/`0xB`, LSDU size) and 6-byte HSR tags (EtherType `0x892F`).  
- **Duplicate Discard & Failover Simulation**: Simulates dual-attached node (DANP) reception pipelines, sliding window sequence buffers, and proves **0.0 ms bumpless failover** during physical cable severance.  
- **Topology & Skew Sizer**: Calculates transmission latency, propagation skew between LAN A and LAN B (\<200 µs), and RedBox proxy forwarding capacity across dual-star, single ring, and coupled topologies.  
- **10-Point Redundancy Auditor**: Verifies conformance against IEC 62439-3 standards, IEEE 1588 transparent clock support, and supervision frame intervals.  
- **Wireshark Scapy Exporter**: Generates ready-to-run Python Scapy scripts to construct and inject PRP/HSR frames.

---

## Getting Started

### Web Interface

Simply open `source-code/index.html` in any web browser. 100% client-side operation with zero installation, zero server dependencies, and zero telemetry.

### Command-Line Interface

cd build

./prpforge-cli.py \--seq 101 \--size 128 \--lan A

./prpforge-cli.py \--burst 16 \--fail lan\_a\_cut \--json

---

## File Structure

product\_222/

├── README.md

├── test\_prpforge.py

├── source-code/

│   ├── index.html

│   ├── prpforge.css

│   ├── app.js

│   ├── prp-engine.js

│   ├── prp-sizer.js

│   └── prp-auditor.js

├── build/

│   ├── prpforge-cli.py

│   └── prpforge-pro-v1.0.0.zip

├── documentation/

│   ├── ARCHITECTURE.md

│   ├── USER\_GUIDE.md

│   ├── MONETIZATION\_AND\_MARKETING\_PLAYBOOK.md

│   └── PROGRESS\_REPORT.md

└── screenshots/

    └── prpforge-studio-preview.svg

---

## License & Commercial Rights

Distributed under the Commercial Engineering License. See `documentation/MONETIZATION_AND_MARKETING_PLAYBOOK.md` for commercial distribution terms and enterprise utility licensing.