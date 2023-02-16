# plotdigitizer-binder
Seeing if I can get Python-based [PlotDigitizer](https://github.com/dilawar/PlotDigitizer) working in sessions served via MyBInder.org

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/plotdigitizer-binder/HEAD)

-----

Initial development:

Basing on https://github.com/fomightez/gel_image_annotation because when first tried running in a vanilla Jupyter session I got error about and when I searched that it came to [this stackoverflow post](https://stackoverflow.com/q/55313610/8508004) about getting `opencv` to work and sure enough when I seached for 'opencv' in the PlotDigitizer code](https://github.com/search?q=repo%3Adilawar%2FPlotDigitizer%20opencv&type=code), I noted it had it listed as a dependency in [pyproject.toml](https://github.com/dilawar/PlotDigitizer/blob/565b89911d92ac5bcbffe4aa1ec60232369446df/pyproject.toml#L13) & [poetry.lock](https://github.com/dilawar/PlotDigitizer/blob/565b89911d92ac5bcbffe4aa1ec60232369446df/poetry.lock#L207) and [trajectory.py in it spoke of using opencv pixel assignment values](https://github.com/dilawar/PlotDigitizer/blob/565b89911d92ac5bcbffe4aa1ec60232369446df/plotdigitizer/trajectory.py#L37). I know I had opencv working in the past in https://github.com/fomightez/gel_image_annotation , which actually was also about scanning image files and converting trends in them to data accessible in Python & so it makes sense, and so started with variations on the configuration files in there as a basis. (In fact, I was able to launch a session from https://github.com/fomightez/gel_image_annotation , install `PlotDigitizer` with `pip` and get the command `!plotdigitizer --help` to work and show usage, and thus I knew it was a good path forward.)