---

#### 5. File: `docs/sdr-monitoring.md`
```markdown
# P25 Digital Radio Monitoring Node

## Hardware
- **Receiver:** RTL-SDR Blog V4 (Direct-soldered USB harness)
- **Host:** HP EliteDesk 800 G3 Mini

## Software Setup
- **Software:** SDRTrunk
- **Target Network:** NC VIPER (P25 Phase 1 / Phase 2 Digital Trunking)
- **Driver:** WinUSB installed via Zadig on Interface 0.

## Functional Specs
- Locks onto local NC VIPER control channels.
- Decodes and logs P25 talkgroups in real time.
- Synthesizes digital audio via the JMBE library codec.
