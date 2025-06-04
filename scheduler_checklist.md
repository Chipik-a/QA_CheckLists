# Checklist: Scheduler Scan Behavior with *** Setting and Battery Status

- [ ] Cosmos setting set to `true` in portal
- [ ] Device running on battery power
- [ ] Run `*** --sched` command
- [ ] Confirm scan does **not** start
- [ ] Confirm exit status `"skipped"`
- [ ] Confirm logs mention skip reason (battery + cosmos setting)
- [ ] Connect device to power
- [ ] Run `*** --sched` again
- [ ] Confirm scan starts successfully
