# Schema Gap Audit Report

Total Unique Inner Keys from `.gon` files: 7354
Total Documented Keys found in Markdown: 51711

## Undocumented Keys (2)

After filtering out nested array values (enums/flags), top-level object IDs, and false positives from comments, there are only **2 true property keys** that appear completely undocumented in the schemas:

- `initiative_adjustment` (Used in Kaiju `BonusTurnPattern` definitions)
- `requires_counter` (Used in Event `prompt` blocks)
