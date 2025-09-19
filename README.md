# CMB_simulation
### CMB simulation with an arbitrary power spectrum and ananlyzing its geometrical features


This notebook simulates Cosmic Microwave Background (CMB) maps and analyzes their statistical and graph-theoretic properties. It generates synthetic CMB data from a simplified power spectrum, identifies local extrema (hot and cold spots), and builds graphs to study correlations and clustering.


### Main Components & Methods

1. CMB Map Generation

  - generate_cmb_map(n, pixel_size, A, ell_0, alpha, fwhm, mean_temp) → creates a 2D CMB temperature map from a simplified power spectrum with Gaussian random fields.

  - Uses Fourier transforms and beam smoothing (Gaussian filter) to model telescope resolution.


2. Feature Extraction

- find_local_maxima(cmb_map) → detects local maxima (hot spots).

- convert_maxima_to_degree(maxima, pixel_size) → converts pixel coordinates into angular coordinates (degrees).


3. Graph Construction

- construct_graph(maxima, threshold_angle) → builds a graph where nodes represent maxima and edges connect nodes within a given angular distance.


4. Statistical & Graph Analysis

- Correlation measures:

calculate_graph_pearson_correlation

calculate_graph_spearman_correlation

calculate_graph_kendall_correlation

- Graph metrics:

calculate_global_clustering → computes clustering coefficient.

calculate_degree_distribution → evaluates node connectivity distribution.
