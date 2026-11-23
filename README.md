
# Applied Hyperspectral Imaging and Spectral Analysis

## Project Overview

This repository presents practical applications of hyperspectral
imaging, spectral analysis, material identification and machine
learning.

The experiments were conducted during the Advanced Spectral
Imaging course at the University of Eastern Finland as part
of the Erasmus Mundus MSc in Computational Colour and Spectral
Imaging (COSI).

## Imaging Systems

- Specim visible-range scanner
- Specim infrared scanner
- Specim IQ hyperspectral camera
- Tunable spectral imaging system

## Applications

1. Green material segmentation
2. Plastic leaf and stem segmentation
3. Medical powder analysis
4. Plastic identification and spectral unmixing
5. Plant species segmentation
6. Flower condition classification

---

## 1. Green Material Segmentation

### Objective

Investigate the ability of hyperspectral imaging to discriminate
materials that exhibit similar visual colours but different
spectral reflectance properties.

### Methodology

Hyperspectral cubes were radiometrically corrected using white
and dark reference measurements. A representative reference
spectrum was extracted from a selected material patch.

Spectral Angle Mapper (SAM) was applied to identify pixels with
spectral signatures similar to the reference spectrum.

PCA, band selection and K-means clustering were also evaluated.

### 1.1 Visible and near infrared-Range Scanner

<table>
<tr>
<th>RGB and Reference Selection</th>
<th>Reflectance Spectrum</th>
<th>Segmentation Result</th>
</tr>
<tr>
<td><img src="result/green%20material%20segmentation/rgbGreenMaterial..png" width=""></td>
<td><img src="result/green%20material%20segmentation/spectrumGreenMaterial..png" width=""></td>
<td><img src="result/green%20material%20segmentation/resultGreenMaterial.png" width=""></td>
</tr>
</table>

### Result Analysis

Although several objects appear green in the RGB image,
their spectral reflectance characteristics differ.

The selected reference spectrum exhibits distinct reflectance
features across the visible and near-infrared wavelengths.

SAM isolates the selected material based on spectral similarity
rather than conventional RGB colour information.

### Potential Industrial Applications

- Material identification
- Industrial machine vision
- Automated sorting
- Product inspection
- Quality control

---

## 2. Plastic Leaf and Stem Segmentation

### Objective

Investigate the spectral differences between plastic leaf and
stem components using infrared hyperspectral imaging and
spectral segmentation techniques.

### Imaging System and Methodology

- Specim infrared hyperspectral scanner.
- White and dark reference correction.
- Reference material selection and spectral extraction.
- Spectral Angle Mapper (SAM).
- Principal Component Analysis (PCA).
- K-means clustering.

### Experimental Results

<table>
  <tr>
    <th>Reference Material Selection</th>
    <th>Spectral Reflectance</th>
    <th>Segmentation Result</th>
  </tr>
  <tr>
    <td>
      <img src="result/leaf%20segmentation/RGBleafmaterial.png" width="300">
    </td>
    <td>
      <img src="result/leaf%20segmentation/spectrumleafmaterial.png" width="300">
    </td>
    <td>
      <img src="result/leaf%20segmentation/resultleafmaterial.png" width="300">
    </td>
  </tr>
  <tr>
    <td colspan="3" align="center">
      <b>Figure 1:</b> Plastic stem segmentation using Spectral Angle Mapper (SAM).
    </td>
  </tr>
  <tr>
    <td>
      <img src="result/leaf%20segmentation/RGBleafmaterial2.png" width="300">
    </td>
    <td>
      <img src="result/leaf%20segmentation/spectrumleafmaterial2.png" width="300">
    </td>
    <td>
      <img src="result/leaf%20segmentation/resultleafmaterial2.png" width="300">
    </td>
  </tr>
  <tr>
    <td colspan="3" align="center">
      <b>Figure 2:</b> Plastic leaf segmentation using K-means clustering.
    </td>
  </tr>
</table>

### Spectral Analysis and Results

The extracted infrared reflectance spectra reveal distinct
spectral characteristics between the plastic leaf and stem
materials across approximately 900–2500 nm.

The stem reference spectrum exhibits pronounced reflectance
minima around 1200, 1400 and 1730 nm, while the leaf reference
spectrum exhibits a different reflectance profile, including
a substantial decrease beyond approximately 2200 nm.

These spectral differences provide useful information for
distinguishing the two material components.

Spectral Angle Mapper (SAM) selectively highlights the stem
components based on spectral similarity to the reference
signature, whereas K-means clustering identifies predominantly
leaf regions through unsupervised spectral grouping.

The results demonstrate the potential of infrared hyperspectral
imaging to discriminate material components beyond conventional
RGB-based identification.

### Potential Industrial Applications

- Plastic material identification and sorting.
- Automated component inspection.
- Industrial quality control.
- Recycling and waste management.
- Spectral machine vision.

## 3. Medical Powder Analysis

### Objective

Investigate SWIR spectral characteristics of different
medical powder samples and identify wavelength combinations
that improve their visual discrimination.

### Methodology

White and dark corrected infrared hyperspectral data were
analysed to identify spectrally informative wavelength regions.

Three SWIR regions were investigated:

| Spectral region | Wavelength |
|---|---|
| Region 1 | 1450–1850 nm |
| Region 2 | 2000–2200 nm |
| Region 3 | Above 2200 nm |

RGB previews were generated automatically by evaluating
different wavelength combinations.

A variance-based criterion was used to select a combination
that enhanced colour contrast between powder samples.

### Results

<!-- Insert visible and infrared reference images -->

<!-- Insert spectral reflectance curves of powder samples -->

<!-- Insert optimized RGB visualization -->

### Result Analysis

The powder samples exhibit different spectral reflectance
characteristics in the SWIR region.

Selecting informative wavelengths improves visual contrast
between samples that are difficult to differentiate using
conventional RGB imaging.

The experiment demonstrates the potential of spectral band
selection for material discrimination.

### Potential Industrial Applications

- Pharmaceutical material inspection
- Powder identification
- Chemical material discrimination
- Non-destructive quality assessment

---

## 4. Plastic Identification and Spectral Unmixing

### Objective

Investigate the spectral and spatial differentiation of
plastic materials using hyperspectral imaging and laboratory
transmittance measurements.

### Methodology

Representative spectral endmembers were extracted from
selected plastic samples.

Non-negative least squares (NNLS) spectral unmixing was
applied to estimate the contribution of each endmember
at individual image pixels.

Hierarchical clustering was also performed using laboratory
transmittance measurements and corresponding spectral
imaging signatures.

### Reference Spectra and Plastic Samples

<!-- Insert plastic sample image and endmember spectra -->

### Spectral Clustering

<!-- Insert plastic dendrogram -->

### Spectral Unmixing Results

<!-- Insert plastic abundance maps -->

### Result Analysis

Different plastic samples exhibit distinct spectral
characteristics that support their differentiation.

The spectral abundance maps visualize the spatial
distribution of individual reference materials.

Hierarchical clustering provides additional information
about spectral similarities and groupings among the samples.

Together, these methods demonstrate the potential of
hyperspectral imaging for plastic material identification.

### Potential Industrial Applications

- Plastic sorting
- Recycling and waste management
- Polymer identification
- Industrial quality control
- Automated material inspection

---

## 5. Plant Species Segmentation

### Objective

Differentiate two plant species using pixel-level spectral
information and supervised neural network classification.

### Methodology

Hyperspectral images were preprocessed using spectral
derivatives and normalization.

Plant regions were manually annotated using GIMP to
generate training data.

Pixel-wise spectral features and corresponding labels
were used to train a fully connected neural network.

| Parameter | Configuration |
|---|---|
| Model | Fully connected neural network |
| Hidden layers | 3 |
| Optimizer | Adam |
| Loss function | Binary cross-entropy |
| Training epochs | 20 |

### Image Annotation

<!-- Insert original and annotated plant images -->

### Segmentation Results

<!-- Insert plant species segmentation results -->

### Result Analysis

The neural network differentiated the two plant species
and background within the evaluated spectral images.

The results demonstrate how spectral signatures can be
combined with machine learning to discriminate biological
materials.

### Potential Industrial Applications

- Precision agriculture
- Plant species identification
- Crop monitoring
- Agricultural machine vision
- Vegetation classification

---

## 6. Flower Condition Classification

### Objective

Investigate the ability of hyperspectral imaging and neural
networks to distinguish old and new rose flowers.

### Methodology

Spectral images were preprocessed and manually annotated
to generate training labels.

Pixel-wise spectral features were extracted and used to
train a fully connected neural network.

| Parameter | Configuration |
|---|---|
| Model | Fully connected neural network |
| Hidden layers | 3 |
| Output layer | Softmax |
| Optimizer | Adam |
| Loss function | Binary cross-entropy |
| Training epochs | 30 |

### Vegetation Indices and Image Annotation

<!-- Insert vegetation indices and annotation images -->

### Classification Results

<!-- Insert original rose image and segmentation result -->

### Result Analysis

The trained neural network differentiated old and new
rose flowers in the evaluated spectral images.

The resulting classification maps highlight the spatial
distribution of the two flower categories.

This experiment demonstrates the potential of spectral
imaging for biological material condition assessment.

### Potential Industrial Applications

- Flower quality assessment
- Agricultural product inspection
- Biological material classification
- Plant condition monitoring

---

## Technical Competencies

### Spectral Imaging and Measurements

- Hyperspectral sample measurements
- Specim imaging systems
- Visible and infrared spectral imaging
- White and dark reference correction
- Spectral reflectance analysis
- Laboratory transmittance measurements

### Spectral Data Analysis

- Spectral Angle Mapper (SAM)
- Principal Component Analysis (PCA)
- K-means clustering
- Hierarchical clustering
- Spectral unmixing
- Non-negative least squares (NNLS)
- Spectral derivatives and normalization
- Optimal wavelength selection

### Machine Learning

- Neural networks
- Supervised classification
- Pixel-wise spectral classification
- Hyperspectral image segmentation

## Source Code

The complete Jupyter notebook contains the Python
implementations and experimental outputs.

[Complete Advanced Spectral Imaging Notebook](ASI_homework2.ipynb)

## Experimental Scope

These projects demonstrate laboratory-scale spectral imaging
applications. The listed industrial applications represent
potential use cases rather than commercially validated systems.

## Author

**Luel Abrha Gebre**

MSc in Computational Colour and Spectral Imaging
(Erasmus Mundus)

MSc in Computer Engineering
