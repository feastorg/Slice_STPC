# TODO

## KiBot CI/Docs Pipeline

- Pipeline functional (workflow case-fix resolved startup_failure)
- DRC: FAIL — 3 clearance violations (0.1719mm actual vs 0.2000mm netclass default)
- ERC: FAIL — 14 errors (10 pin_not_connected, 1 power_pin_not_driven, 2 label_dangling, 1 pin_to_pin)
- Fab: FAIL (blocked by ERC pre-flight)
- gen-kibot-index: skipped
- deploy-pages: skipped (repo is private; Pages requires public visibility)

## Board Development

- [ ] Fix 3 DRC clearance violations
- [ ] Fix 14 ERC errors (unconnected pins, dangling labels, power pin issues)
- [ ] Make repo public to enable GitHub Pages
- [ ] Split into separate template directories (one hardware/ directory per repository)
- [ ] Add level shifter for I2C
- [ ] Add firmware for closed loop control
- [ ] As more versions of stepper cards are released, add firmware support for them
- [ ] Add current reader for thermocouple
