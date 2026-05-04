# 🧪 Lab Data Naming Convention

To automate our Notion data entry, we use a standard, simple file-naming rule. The AI relies on **underscores (`_`)** to separate the different pieces of information. Spaces are fine *inside* a section, but you must use underscores to move to the next section.

## The Formula
`[Technique]_[SampleID]_[Specifications]_[Comments].[ext]`

### 1. Technique Codes (Position 1)
*   `SEM` = Scanning Electron Microscopy
*   `RMN` = Raman Spectroscopy
*   `PL`  = Photoluminescence
*   `OM`  = Optical Micrograph
*   `AFM` = Atomic Force Microscopy
*   `ELP` = Ellipsometry
*   `XPS` = X-ray Photoelectron Spectroscopy

### 2. Sample ID (Position 2)
Your unique identifier for the sample (e.g., `WS2-S1`, `Gr-S2`).

### 3. Specifications (Position 3)
Include the measurement settings here. Separate them with spaces. 
*Don't worry about being perfect with units—the AI is smart enough to know that "532" in a Raman file means a 532nm laser.*
*   **For Raman/PL:** Laser wavelength, magnification, grating, exposure time, power, accumulations.
*   **For SEM:** Acceleration voltage, detector type, magnification, working distance.
*   **For OM:** Magnification, lighting mode (e.g., Darkfield).

### 4. Comments (Position 4)
Any extra notes, locations, or findings (e.g., `spot1`, `center of flake`, `dirty sample`).

---

## 📝 Examples

**Raman Spectroscopy Example:**
> `RMN_WS2-S1_532nm 100x 1200 1s 10% 3acc_center of flake.wdf`
*   *Technique:* RMN
*   *Sample:* WS2-S1
*   *Specs:* 532nm laser, 100x lens, 1200 grating, 1s exposure, 10% power, 3 accumulations
*   *Comments:* center of flake

**SEM Example:**
> `SEM_Gr-S2_5kV Inlens 10000x 6.5mm_high contrast.tif`
*   *Technique:* SEM
*   *Sample:* Gr-S2
*   *Specs:* 5kV voltage, Inlens detector, 10000x mag, 6.5mm working distance
*   *Comments:* high contrast
