# UAT Test Cases

> Designed for a synthetic portfolio case study. These tests have not been executed against a production banking system.

## UAT-01 — Ownership and reassignment

**Related requirement:** FR3

**Precondition:** A failed trade case exists.

**Steps**
1. Assign the case to Analyst A.
2. Open the case and verify the current owner.
3. Reassign the case to Analyst B.
4. Verify the current owner again.
5. Review ownership history.

**Expected result:** Analyst B is the current owner and Analyst A remains in ownership history.

## UAT-02 — Illustrative high-value prioritisation

**Related requirement:** FR5

For this test only, assume `Trade_Value_GBP > £1,000,000` means High Priority.

**Test data**
- Trade A: £10,000
- Trade B: £5,000,000
- Trade C: £50,000

**Expected result:** Trade B is High Priority. Trades A and C are not High under this illustrative rule.

> The threshold is an invented test assumption and is not a real financial institution's policy.

## UAT-03 — Central visibility

**Related requirement:** FR4

**Steps**
1. Create several outstanding cases with different owners and statuses.
2. Open the central management view.
3. Confirm each outstanding case is visible.
4. Confirm status, current owner and priority are shown.

**Expected result:** Management can see the required information for all outstanding cases in one view.
