# DICE

Data for the paper **"A Fine-Grained Vietnamese Hotel Review Benchmark and Definition-Informed Cross-Aspect Encoding for Sentiment Intensity Analysis"** (under review).

This repository currently releases **ViHotelSI**, a corpus of Vietnamese hotel reviews from Hanoi annotated for ten aspects on a five-point sentiment intensity scale. The code will be added later.

## Files

| File | Reviews |
|---|---|
| `train.csv` | 12,755 |
| `val.csv` | 1,594 |
| `test.csv` | 1,595 |
| **Total** | **15,944** |

The splits are random (80/10/10), stratified by the presence of negative labels and the number of evaluated aspects. Duplicates were merged before splitting, so no review text occurs in more than one split.

## Format

Each row is one review. The column `data` holds the review text, and each of the ten aspect columns holds one label:

`room`, `service`, `location`, `price`, `food_and_beverage`, `amenities`, `cleanliness`, `transportation`, `policy`, `others`

| Label | Meaning |
|---|---|
| `0` | aspect not evaluated |
| `-2` | strongly negative |
| `-1` | mildly negative |
| `1` | mildly positive |
| `2` | strongly positive |

Example:

| data | room | service | location | cleanliness | … |
|---|---|---|---|---|---|
| phòng hơi nhỏ nhưng sạch sẽ, nhân viên rất nhiệt tình, gần phố cổ | -1 | 2 | 2 | 2 | 0 |

## Notes

- Reviews were collected from Agoda, Traveloka and Google Reviews (July–December 2025). Reviews written in other languages were translated into Vietnamese and checked manually.
- Reviewer and facility information is anonymised.
- On a re-annotated sample of 400 reviews, agreement is near-perfect for aspect detection and polarity, but only moderate for the distinction between ±1 and ±2. We recommend reporting results at the polarity level (−/+) as well as the five-class level.

## License and terms of use

The data are released **for non-commercial research purposes only** under the [LICENCE] licence. Any commercial use, including evaluating, ranking or marketing individual businesses, is not permitted. Do not attempt to identify reviewers, staff or facilities.

## Citation

The citation will be added once the paper is published.

## Contact

Tam Khoi Tran (242805006@student.tdtu.edu.vn), Ton Duc Thang University, Ho Chi Minh City, Vietnam.
