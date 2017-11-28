## Overview

This package extends the existing `ggplot2::facet_grid` to provide a sample
of that grid, instead of the full grid.  This is useful when visualizing
information with many values in a facet dimension.

## TODOs

 - confirm that `facet_sample` is treating data correctly for use with various `stat_*`s.
 - enable sampling by percentage
 - automated test codes?  need to understand better what the enternals of facets are supposed to be
 - handle `margins` defaults more intelligently
 - re-direct `FacetSample` object definition documentation?  Alternative approach to make
 available for user space / extension (e.g., via data)?
 - when using another aesthetic (e.g., color, fill, shape) with a facet_dimension, the
 marginal facet `(all)` should not get another value (e.g., it should show mix of
 colors, fills, shapes, etc).  This may be an issue that must be resolved at `facet_grid` level.
 if that's the conclusion, alternatives: (1) determine ggplot2 code changes and convince
 them to adopt or (2) have facet_sample no longer extend facet_grid
