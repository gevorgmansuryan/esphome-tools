# ESPHome LD2410 Component with Automatic Calibration

This ESPHome package extends the LD2410 component with an **automatic calibration tool**.  
It collects the maximum move/still values per gate during a calibration run and applies them as thresholds with a configurable margin.

---

## Usage

```yaml
packages:
  ld2410:
    url: https://github.com/gevorgmansuryan/esphome-tools
    files:
      - path: packages/ld2410.yaml
        vars:
          tx_pin: GPIO21
          rx_pin: GPIO20
          default_threshold: 1
          collection_seconds: 30
```
