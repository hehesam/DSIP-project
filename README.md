# Low-Pass and High-Pass Filters in Image Processing

**Author:** Hesam Mohebi  
**Project Goal:**  
This notebook explores various Low-Pass Filters (LPF) and High-Pass Filters (HPF) in the context of image processing. It demonstrates how these filters affect images in both spatial and frequency domains, and provides practical implementations and comparisons.

---

## 📌 Purpose

To understand and analyze the effects of different filtering techniques on images. This includes:
- Removing noise and smoothing images (LPF)
- Enhancing edges and fine details (HPF)
- Comparing filters in spatial and frequency domains

---

## 🧠 Key Concepts

### Low-Pass Filters (LPF)
- Allow low frequencies, suppress high ones
- Cause image smoothing or blurring
- Useful for denoising and reducing image detail

#### Implemented LPFs:
- **Ideal LPF**: Sharp cutoff, introduces ringing artifacts
- **Butterworth LPF**: Smooth transition, less ringing
- **Gaussian LPF**: Smooth, natural blur
- **Mean (Box) Filter**: Simple average of neighboring pixels
- **Median Filter**: Effective for removing salt-and-pepper noise

### High-Pass Filters (HPF)
- Allow high frequencies, suppress low ones
- Enhance image details and edges

#### Implemented HPFs:
- **Ideal HPF**: Sharp edges, high ringing
- **Butterworth HPF**: Gradual frequency suppression
- **Gaussian HPF**: Smooth edge enhancement
- **Laplacian Filter**: Highlights fine details
- **Sobel Filter**: Detects vertical and horizontal edges

---

## 🔍 Methodology

### Frequency Domain Filtering
1. Compute the image’s 2D FFT
2. Apply filter mask in frequency domain
3. Perform inverse FFT to get the filtered image

### Spatial Domain Filtering
1. Convolve image with filter kernel (mean, median, Sobel, Laplacian)

---

## 📊 Visual Comparisons

- Different filters are applied to sample images like `brain.jpg` and `broken_text.jpg`
- Performance is compared across various cutoff frequencies
- Results are visualized side-by-side for easy analysis

---

## 🛠️ Libraries Used

- `NumPy`
- `Matplotlib`
- `SciPy`
- `scikit-image`

---

## ✅ Applications

- Image pre-processing
- Edge detection and feature extraction
- Noise reduction and blurring

---

## 📂 Structure

- `comparison()`: Main function to apply and visualize LPFs
- Individual blocks for each HPF type
- Plots and time performance for each filter

---

