# TEST-NEEDS.md — refugia

## CRG Grade: C — ACHIEVED 2026-04-04

## Current Test State

| Category | Count | Notes |
|----------|-------|-------|
| Test directory | Present | `tests/` directory exists |
| Test framework | Configured | Via justfile and setup.sh |

## What's Covered

- [x] Test infrastructure in place
- [x] Build system integration

## Still Missing (for CRG B+)

- [ ] Unit tests implementation
- [ ] Integration test suite
- [ ] Property-based testing
- [ ] Performance benchmarks
- [ ] End-to-end tests

## Run Tests

```bash
cd /var/mnt/eclipse/repos/refugia && just test
```
