# TODO

## Pass 1 — CI Pipeline

- [x] Pipeline added (workflow case-fix resolved startup_failure)
- [x] DRC: FAIL — 3 clearance violations (0.172mm actual vs 0.200mm netclass default)
- [x] ERC: FAIL — 14 errors (10 pin_not_connected, 1 power_pin_not_driven, 2 label_dangling, 1 pin_to_pin)
- [ ] Fab: SKIPPED (blocked by ERC pre-flight)
- [ ] gen-kibot-index: SKIPPED
- [ ] deploy-pages: SKIPPED

## Pass 2 — Pre-Fab Review

- [ ] Fix 3x DRC clearance violations
- [ ] Fix 10x pin_not_connected ERC errors
- [ ] Fix 1x power_pin_not_driven ERC error
- [ ] Fix 2x label_dangling ERC errors
- [ ] Fix 1x pin_to_pin ERC error
- [ ] Verify BOM completeness and sourcing
- [ ] Confirm board outline and mounting holes
- [ ] Footprint verification against datasheets
- [ ] Design review sign-off

## Board Development

- [ ] Add level shifter for I2C
- [ ] Add firmware for closed loop control
- [ ] As more versions of stepper cards are released, add firmware support for them
- [ ] Add current reader for thermocouple
