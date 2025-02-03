# Project Overview

This repository contains a solution to the Dragonfruit Software Engineering Challenge, which involves processing large-scale images of microorganisms for cancer detection. The solution includes efficient data structures, image simulation, cancer classification, and performance optimization.

# Data Representation
To efficiently store and process high-resolution images (100,000x100,000 pixels), we used:

- Microscope Image Representation: Run-Length Encoding (RLE) to store black pixels as start-end index pairs in each row, minimizing storage needs.
- Dye Sensor Representation: A sparse representation using coordinate lists since the dye regions are minimal and scattered.

# Generating Simulated Data
We generate realistic test images before handling actual data:

- Microscope Image Simulation: Uses cellular expansion to create arbitrary-shaped blobs that mimic microorganisms.
- Dye Sensor Simulation: Generates dye leakage and internal flows using random sparse pixel distributions.

# Cancer Detection Algorithm
A parasite is classified as cancerous if the dye-occupied area inside its body exceeds 10% of its total area.

- Identify the parasite's region from the microscope image.
- Count the dye pixels within this region.
- Compute the ratio and classify accordingly.

# Performance Enhancements
To improve execution speed:

- Used NumPy arrays for vectorized operations.
- Optimized flood-fill algorithms for region segmentation.
- Implemented parallel processing to handle multiple images simultaneously.

# Compression Techniques
Bitmask-based storage for microscope images.

- Quad-tree compression for sparse dye data.
- Wavelet transforms to reduce resolution without significant data loss.

# Tools Used

- Python, NumPy, Matplotlib for data processing and visualization.
- GitHub, Stack Overflow, Copilot for collaborative problem-solving.
- LLMs (ChatGPT, Copilot) to explore optimized solutions.

# Running the Code

- Clone the repository.
- Run DragonFruitAI.ipynb in Jupyter Notebook.
- View results and analyze execution performance.
