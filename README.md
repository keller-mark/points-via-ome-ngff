# points via OME-NGFF

Experiment in evaluating storage of points (2D, 2.5D, or 3D point clouds) via OME-NGFF:
- Definition of the storage approach
- Prototype implementation
- TODO: Utilities to convert SpatialData Points elements to this format
- TODO: Benchmarking of common operations (existing Parquet-based format vs. this OME-NGFF-based format)


## Storage approach

- 2D case: 2D multi-channel image, with channels `["x", "y", "c"]`
- 2.5D case: 2D multi-channel image, with channels `["x", "y", "z", "c"]`
- 3D case: 3D multi-channel image, with channels `["x", "y", "z", "c"]`

(where "c" corresponds to the feature_index values, i.e., the gene indices in `sdata.tables['table'].var.index`)

For more details see https://github.com/scverse/spatialdata/issues/789
