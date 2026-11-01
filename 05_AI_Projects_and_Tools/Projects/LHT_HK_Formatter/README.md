# LHT_HK_Formatter

A specialist formatter for TRUMPF LHT (Lohnherstellkosten) SAP Controlling exports. It defines a strict six-sheet Excel output for CK13N, CK53N, ZCo6, ZCo9, and structurally similar exports.

## Capabilities

- Detect source transaction and select full BOM, flat itemization, or period-comparison mode.
- Normalize German number formats and parse header metadata.
- Define exact sheet names, Excel table names, and column orders.
- Classify material, operation, and overhead rows and preserve verified BOM hierarchy.
- Validate workbook structure, totals, missing data, and numeric values.
- Support pasted text with Assembly/BOM disambiguation.

## Six-sheet output contract

1. Cover
2. Assembly (`Tbl_Assembly`)
3. BOM_Detail (`Tbl_BOM`)
4. Pivot_Assembly (plain range, not an Excel Table)
5. Operations (`Tbl_Operations`)
6. Suppliers (`Tbl_Suppliers`)

See [the full workflow specification](skills/lht-hk-formatter/SKILL.md).

## Open the ChatGPT plugin

[Open LHT_HK_Formatter in ChatGPT](https://chatgpt.com/plugins/plugins_6ade2a48501c8191a3d355c267113d34)

The plugin is private. Its GitHub documentation does not automatically synchronize with the installed ChatGPT plugin. A skill-only plugin also relies on available file-reading and workbook-generation capabilities; the assistant must disclose any validation step it cannot actually execute.

## Data confidentiality

Do not commit SAP cost exports, material costing data, or supplier details to a public repository. Publish only the reusable instructions and sanitized examples.

## Runnable reference implementation

A Python implementation is available in [`implementation/lht_hk_formatter.py`](implementation/lht_hk_formatter.py). Install `openpyxl` and `pandas`, then run `python lht_hk_formatter.py input.xlsx -o output.xlsx`. Because SAP layouts vary, review transaction detection, hierarchy mapping, cost-summary basis, and ZCo6/ZCo9 period-comparison results before using the workbook operationally.
