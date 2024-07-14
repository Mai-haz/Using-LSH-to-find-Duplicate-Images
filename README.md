# Blockchain
# Image Duplicate Finder

This Python script identifies near-duplicate images in a specified directory using image hashing and Locality Sensitive Hashing (LSH). It computes a perceptual hash for each image and then identifies pairs of images that are similar based on a specified threshold.

## Features
- Calculates image hashes using the `imagehash` library.
- Identifies near-duplicate images using Locality Sensitive Hashing (LSH).
- Configurable hash size, threshold, and number of bands for LSH.

## Requirements
- Python 3.x
- `imagehash`
- `numpy`
- `Pillow`

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/image-duplicate-finder.git
    cd image-duplicate-finder
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Place the images you want to check for duplicates in a directory.

2. Update the `main` function with the correct directory path and desired parameters:
    ```python
    Directory = r"C:path-to-your-directory"
    threshold = 0.7
    HashSize = 19
    bands = 48
    ```

3. Run the script:
    ```bash
    python image_duplicate_finder.py
    ```

## Functions
### `FindSignature(image: str, HashSize: int) -> n.ndarray`
Computes the perceptual hash of an image.

### `FindDuplicates(Directory: str, threshold: float, HashSize: int, bands: int) -> List[Tuple[str, str, float]]`
Finds and returns a list of near-duplicate images based on the specified threshold.

### `main()`
The main function that initializes the parameters and calls the `FindDuplicates` function.

## Example Output
