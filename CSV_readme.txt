Each model CSV includes its Sequence ID, sequence, NCAA count, receptor,
Model ID, original Boltz confidence scores, atom counts and geometry/interface checks.
Individual model CSVs and the combined Model_scores.csv use the same columns.
Sequence is the XML sequence listing. NCAA counts retain the reviewed residue
annotations; unresolved counts stay blank. NCAA names and SMILES are in
Sequence_summary.csv. No atom coordinates or file paths are included.

ipTM describes interface confidence. Interface pLDDT is local confidence
with interface tokens upweighted. Confidence score is Boltz's recorded
overall ranking score (0.8 x complex pLDDT + 0.2 x ipTM for these complexes).
Higher values indicate higher structural confidence, not binding affinity.
Scores belong to the original prediction and are not recalculated by
refinement. Alternatives from one prediction can share their scores.
Values are rounded to six decimal places in CSVs; ranking uses the original
full-precision values. Missing values remain blank.

Atom counts refer to atoms present in the retained complex CIF. Geometry/
interface results report the specified computational checks. Pass does not
establish a native binding pose.

Sequence rankings use the highest value of the selected metric among that
sequence's displayed models, including retained alternatives. The receptor
filter applies. Unavailable values sort last in either direction. The model
providing that value is named in the ranking column. Ranking does not select
a native structure or establish affinity or activity.

Sequence_summary.csv contains the sequence, NCAA details and availability.
Model_scores.csv has one row per model. Individual *_Scores.csv files have
one row each. All CSVs use UTF-8 and comma delimiters.
