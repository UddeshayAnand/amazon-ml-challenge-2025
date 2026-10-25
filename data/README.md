# Challenge data

Local inputs are `train.csv` and `test.csv` in this directory. Both supplied files contain 75,000 rows. Redistribution terms have not been established; obtain authorized copies. Ignoring these CSVs does not untrack a file previously committed elsewhere.

| Column | Training | Test | Requirement |
|---|---|---|---|
| `sample_id` | Required | Required | Nonempty, unique within each file |
| `catalog_content` | Required | Required | Nonempty description text |
| `image_link` | Present | Present | Unused by maintained text models |
| `price` | Required | Absent | Finite, strictly positive numeric target |

Loaders use UTF-8 by default; change `ENCODING` only when your source requires it. IDs are read as strings to preserve leading zeros. Training never modifies source files.

The supplied **Amazon 25 Problem Statement.pdf** requires predictions for every test ID, positive prices, SMAPE evaluation, and a final model of at most 8 billion parameters under MIT/Apache 2.0 terms. It prohibits external price lookup. It does not establish redistribution permission. Check the eligibility of any chosen pretrained model.

The supplied training CSV has 107 duplicate descriptions beyond first occurrences after case and whitespace normalization. Grouped splitting keeps those descriptions together; near-duplicates remain possible.
