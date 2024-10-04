## Description
Analysis script related to the manuscript "Predegenerating Donor Nerve for grafting Using Focused Ultrasound Neurotomy".

## Prerequisites
- DeepLabCut or Python

## Installation
* Install [DeepLabCut][DeepLabCut] via [Anaconda][Anaconda] with 
`pip install "deeplabcut[gui]"`
	
* Download and extract the [SFI][project] script to your computer.

## Usage
- After collecting gait videos from your experiment, annotate frames using the [DeepLabCut][DeepLabCut] with `python -m deeplabcut` and generate tracked `h5` files.
- Modify the `SFI.py` script to match your project requirements including injury side, project location, and labels used during annotations. By default, the script expects all the following annotations: `[R|L][Thumb|Pinky|Index|Ring|Heel|Middle]`
- Run `python sfi.py` to generate files with Sciatic Functional Index Calculation (SFI) as `ToeSpread/IntSpread/PrintLength` for `NormalLeft/InjuredRight` or `NormalRight/InjuredLeft`, and their means.

## Changelog
See [Changelog](CHANGELOG.md)

[Anaconda]: https://docs.anaconda.com/miniconda/miniconda-install
[DeepLabCut]: https://github.com/DeepLabCut/DeepLabCut
[project]: https://github.com/leomol/SFI

[Leonardo Molina]: https://github.com/leomol
[LICENSE.md]: LICENSE.md