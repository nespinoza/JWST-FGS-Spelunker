# Change Log

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [1.0.2] - 2023-09-01 (Current release)
### Added
- Photometry can now be optimized with a mask. `spk.optimize_photometry()` does the trick via an automatic mask generation; 
  a manual mask can also be passed instead via `spk.optimize_photometry(mask = mask)`. TODO: handle optimal masks for 
  multiple guidestars.
- Added test function in `testing`, useful for testing before releases/updates. 

### Fixed
- Fixed bug introduced when storing `data_arrays` in the `spelunker_outputs` directory.
- Fixed bug introduced by directory changes.

## [1.0.1] - 2023-08-02 
- Error message when data is not downloaded either to not having propietary access period or no data.
- Possibility to download data with exclusive access period by specifying a `token` in `spelunker.load`. This is a string.
- Time is now sorted by guidestar epochs.
- Spelunker now does not use `os.chdir`, so the directory will not change unexpectedly while using Jupyter notebooks.

## [1.0.0] - 2023-07-23
### Added

- Added better file management systems. Now `spelunker` will create directories for data processing and downloads.
- Added a scalable x axis that changes timescales based on the input time array.
- You can specify a directory for `spelunker.load` with the `dir` parameter. Specifying a directory is now optional and you can call `spelunker.load` without any parameters.
- Added a `save` parameter for `spelunker.load` to toggle saving the `fg_array`, `fg_flux`, and `fg_time` arrays as a `.npy` file.
- Added saving methods for `gauss2d_fit`, `quick_fit`, and  with the `save` parameter.
- Added try and except statements to `gauss2d_fit` to prevent code crashing if a fit fails
- Added `save` method to save Gaussian fit results and object properties to a `txt` file.

### Fixed
- Fixed initial guesses of gaussian fits in `gauss2d_fit` to handle guidestar changes in position. Gaussian fits should run faster and be more reliable.


## [0.5.5] - 2023-07-20

- Changes to setup.py. Now `pip install spelunker` should run more properly.

## [0.5.4] - 2023-07-19

- Added changes to testpypi

## [0.5.3] - 2023-07-19

### Added

- `spelunker` is added to PyPI!
