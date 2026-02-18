# PiQA-Odia

**PiQA-Odia** is an Odia-language dataset for evaluating **physical commonsense reasoning** in a *two-answer preference* format: given a prompt describing a concrete physical scenario, a model must choose the more physically correct of two closely matched answers.

The dataset is Odisha-centric and covers everyday physical interactions across six categories:
- Coastal Landscape & Tourism (20)
- Religious Setting (10)
- Agriculture & Environment (20)
- Food (20)
- Folk Theater (15)
- Folk Song & Dance (15)

Total: **100 instances**.

---

## Files

- `piqa_odia.tsv` (recommended): main dataset in TSV format.

> Note: Some releases may include an extra index column (e.g., `sl` or `id`). The core schema below remains the same.

---

## Data Schema (TSV)

Each row is a tuple:

`<query, solution0, solution1, label, category, language>`

| Column     | Type   | Description |
|------------|--------|-------------|
| `query`    | string | Odia prompt describing a physical scenario phrased as a common task/action. |
| `solution0`| string | **Wrong** answer: plausible and fluent, but physically incorrect. |
| `solution1`| string | **Correct** answer: physically correct. |
| `label`    | int    | Correct option indicator. In this dataset, `label` is always `1` (since `solution1` is always correct). |
| `category` | string | One of: `Landscape`, `Religious`, `Agriculture`, `Food`, `Theater`, `Song`. |
| `language` | string | FLORES-200 code for Odia: `ory_Orya`. |

---

## Example Row

```tsv
query	solution0	solution1	label	category	language
...	...	...	1	Food	ory_Orya
```

## Cite Us

```bibtex
@misc{mukherjee2026piqaodia,
  title        = {PiQA-Odia: A Physical Commonsense Reasoning Dataset for Odia Language},
  author       = {Mukherjee, Kunal},
  year         = {2026},
  howpublished = {arXiv},
  note         = {}
}
```
