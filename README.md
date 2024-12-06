# Uncommon COBOL REDEFINES Error: Data Overwrite

This example demonstrates an uncommon error in COBOL related to the use of the REDEFINES clause.  The REDEFINES clause allows multiple data items to share the same storage area. However, if not handled carefully, it can lead to data being unintentionally overwritten.

The `bug.cob` file shows the incorrect code that demonstrates the issue. The `bugSolution.cob` file offers a corrected version.

**Problem:** The initial code attempts to move data into `WS-SUB-AREA-1` and then `WS-SUB-AREA-2`.  Due to the REDEFINES clause, this modifies `WS-AREA-1`, potentially overwriting data unintentionally depending on how the data is used elsewhere in the program.

**Solution:**  The solution showcases a more robust approach to avoid this type of data corruption.