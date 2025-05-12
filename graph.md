graph TD
    A[Load Image<br>im.jpg<br>BGR to RGB] -->|Original Image| B1[Mild Blur<br>25x25, σ=10]
    A -->|Original Image| B2[Strong Blur<br>51x51, σ=20]
    A -->|Original Image| B3[Extreme Blur<br>101x101, σ=30]
    
    B1 -->|Blurred Mild| C1[Abs. Difference<br>Original - Mild]
    B2 -->|Blurred Strong| C2[Abs. Difference<br>Original - Strong]
    B3 -->|Blurred Extreme| C3[Abs. Difference<br>Original - Extreme]
    
    C1 -->|Diff. Mild| D1[Convert to Grayscale]
    C2 -->|Diff. Strong| D2[Convert to Grayscale]
    C3 -->|Diff. Extreme| D3[No Grayscale]
    
    A -->|Original Image| E[Display Results<br>2x3 Subplot]
    B1 -->|Blurred Mild| E
    B2 -->|Blurred Strong| E
    B3 -->|Blurred Extreme| E
    D1 -->|Gray Diff. Mild| E
    D2 -->|Gray Diff. Strong| E
    
    E --> F1[Original Image<br>RGB]
    E --> F2[Mild Blur<br>RGB]
    E --> F3[Strong Blur<br>RGB]
    E --> F4[Extreme Blur<br>RGB]
    E --> F5[Diff. Map Mild<br>Jet Colormap, vmax=100]
    E --> F6[Diff. Map Strong<br>Jet Colormap, vmax=100]
