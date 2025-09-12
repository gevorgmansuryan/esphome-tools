# ESPHome LD2410 Component with Automatic Calibration

This ESPHome package extends the LD2410 component with an **automatic calibration tool**.  
It collects the maximum move/still values per gate during a calibration run and applies them as thresholds with a configurable margin.

---

## Usage

```yaml
packages:
  ld2410: github://gevorgmansuryan/esphome-tools/packages/ld2410.yaml@main
    vars:
      tx_pin: GPIO21             # UART TX pin
      rx_pin: GPIO20             # UART RX pin
      default_threshold: 1       # Margin added to maxima
      collection_seconds: 30     # Duration of calibration in seconds
```