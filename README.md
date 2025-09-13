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
          # config
          tx_pin: TX                      # replace with your TX pin
          rx_pin: RX                      # replace with your RX pin
          default_collection_seconds: 30  # how many seconds to collect calibration data
          default_move_margin: 2          # default threshold margin to add on top of maxima
          default_still_margin: 1         # default threshold margin to add on top of maxima
          # fixed values
          g0_move: 50
          g1_move: 50
          g0_still: 0
          g1_still: 0
```
