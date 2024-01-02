
1.  **Peak Signal-to-Noise Ratio (PSNR):**
    
    -   **Purpose:** Measures the similarity between an enhanced image and the original high-quality image.
        
    -   **Formula:**
        
        ```python
           PSNR = 10 * log10((MAXI^2) / MSE)
        
        ```
        
    -   **MAXI:** Maximum possible pixel value of the image
        
    -   **MSE:** Mean Squared Error between the enhanced and original images
        
    -   **Additional Info:** Higher PSNR values indicate better image quality. Often used in video and image compression. 📈🎞️
        
2.  **Structural Similarity Index (SSIM):**
    
    -   **Purpose:** Evaluates the structural similarity between an enhanced image and the original high-quality image, considering luminance, contrast, and structure.
    -   **Formula:**
    
    ```python
    SSIM = (2 * μx * μy + C1) * (2 * σxy + C2) / ((μx^2 + μy^2 + C1) * (σx^2 + σy^2 + C2))
    
    ```
    
    -   **μx, μy:** Average of pixel values in the enhanced and original images
    -   **σx, σy:** Standard deviation of pixel values in the enhanced and original images
    -   **σxy:** Covariance of pixel values in the enhanced and original images
    -   **C1, C2:** Constants to stabilize the division
    -   **Additional Info:** SSIM values range from -1 to 1, where 1 indicates perfect similarity. 🖼️🔍
3.  **Mean Squared Error (MSE):**
    
    -   **Purpose:** Calculates the average squared difference between the pixel values of an enhanced image and the original high-quality image.
    -   **Formula:**
    
    ```python
    MSE = (1 / N) * Σ(Xi - Yi)^2
    
    ```
    
    -   **Xi:** Pixel value in the enhanced image
    -   **Yi:** Pixel value in the original image
    -   **N:** Total number of pixels in the image
    -   **Additional Info:** Commonly used but sensitive to outliers; lower MSE values indicate better image quality. 📉📷
4.  **Multi-Scale Structural Similarity Index (MSSSIM):**
    
    -   **Purpose:** Extends the SSIM metric to evaluate image quality at different scales, providing a more comprehensive assessment.
    -   **Formula:**
    
    ```python
    MSSSIM = (Σ(SSIMi^(αi))^(βi))^(1 / Σβi)
    
    ```
    
    -   **SSIMi:** SSIM value at the ith scale
    -   **αi, βi:** Weights for the ith scale
    -   **Additional Info:** Addresses the limitation of SSIM by considering multiple scales for a more nuanced evaluation. 🔄🌐
5.  **Perceptual Quality Assessment (PQA):**
    
    -   **Purpose:** Assesses the perceptual quality of an enhanced image from a human observer's perspective.
    -   **Methods:** Various PQA models exist, such as the following:
        -   **Berenji's Image Quality Assessment (BIQA):** Uses a combination of spatial and frequency domain features to predict perceptual quality.
        -   **Deep Perceptual Quality Metric (DPQM):** Employs a deep neural network to learn perceptual features and predict image quality.
    -   **Additional Info:** PQA focuses on mimicking human perception, acknowledging that visual quality is subjective. Emphasizes the importance of considering human visual preferences. 👁️‍🗨️🎨
6.  **Dice Coefficient (F1 Score):**
    
    Formula:
    
    ```python
    Dice Coefficient = (2 * |X ∩ Y|) / (|X| + |Y|)
    
    ```
    
    -   `X`: Set of pixels labeled as part of the object in the prediction
    -   `Y`: Set of pixels labeled as part of the object in the ground truth
    -   Dice Coefficient is used to evaluate the overlap between the predicted and ground truth segmentation masks. It ranges from 0 to 1, where 1 indicates perfect overlap.
7.  **Intersection over Union (IoU):**
    
    Formula:
    
    ```python
    IoU = |X ∩ Y| / |X ∪ Y|
    
    ```
    
    -   `X`: Set of pixels labeled as part of the object in the prediction
    -   `Y`: Set of pixels labeled as part of the object in the ground truth
    -   Intersection over Union measures the ratio of the intersection area to the union area of the predicted and ground truth segmentation masks. It also ranges from 0 to 1, with 1 indicating perfect overlap.
