# FUTOG — data for reproduction

One row per participant / item / group, as described in `metadata.xlsx`.

| file | level | notes |
|---|---|---|
| `belief_items.xlsx` | participant x item x time | likelihood ratings |
| `subject_measures.xlsx` | participant | belief/emotion/connectedness/memory + flags |
| `group_conversation.csv` | group | transcript-derived tone + discussion amounts (no verbatim text) |

**Transcripts and questionnaire data are not shared** (participant privacy). The BDI-II, LOT-R and TIPI responses collected at screening are not included; the BDI-II was used only to apply the preregistered exclusion criterion described in the Methods, and every participant in these files scored at or below the cut-off. The conversation analyses use only the group-level aggregates in `group_conversation.csv` (affective tone from sentiment; discussion amounts from keyword matching, SI Note S7). The prevalence of encoded Cognitive Units *within the imagination task* (Results, memory section) likewise derives from the transcripts and is not reproducible from these aggregates.

## The `group` column

`group` has a different meaning in each condition:

- **Collaborative condition** — a real group of four participants who interacted (19 groups). These are the units used in every group-level analysis.
- **Individual condition** — participants did not interact, so each one carries their own participant ID in this column (75 "groups" of one). They are never treated as groups; they enter the pseudo-group null only as a pool of non-interacting individuals to be partitioned at random.

The 94 distinct values are therefore 19 real groups plus 75 individual participants. Group labels are arbitrary identifiers (`G01`–`G19` for the interacting groups, `I01`–`I75` for the individual participants) and carry no information about when a session took place.
