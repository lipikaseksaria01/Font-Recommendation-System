## **Overview**

The Font Recommendation System is a Python tool that leverages a Siamese neural network with pre-trained Word2Vec embeddings to recommend fonts based on similarity. The system aims to assist designers in selecting font combinations that exhibit balanced contrast and share common themes.

## **Features**

*   Utilizes pre-trained Word2Vec embeddings for font representations.
*   Siamese neural network architecture for font similarity assessment.
*   Recommends fonts based on contrast and theme similarity.

## **Prerequisites**

*   Python 3.x
*   TensorFlow 2.x
*   NumPy
*   Gensim (for loading Word2Vec embeddings)
*   Data source: https://speedysense.com/2500-fonts-bundle-download-free/

## **Example**

```plaintext
# Example Usage
base_font = "font_42.ttf"
recommended_fonts = recommend_fonts(siamese_model, font_to_index, base_font)
print(f"Recommended fonts for {base_font}: {recommended_fonts}")

# Output
Recommended fonts for Ac.ttf:
1. /content/drive/My Drive/fonts/Fonts/FreeUniversal-Regular.ttf
2. /content/drive/My Drive/fonts/Fonts/Colors Of Autumn.ttf
3. /content/drive/My Drive/fonts/Fonts/CursiveSans.ttf
4. /content/drive/My Drive/fonts/Fonts/ARDELANEY.ttf
5. /content/drive/My Drive/fonts/Fonts/Denise_Handwriting.ttf
```

## **Usage**

1.  **Data Generation:**
    *   Create font pairs and labels using the **create\_font\_pairs\_and\_labels** function.
    *   Ensure the existence of a dataset with font pairs, contrast labels, and theme labels.
2.  **Siamese Network Setup:**
    *   Adjust the **num\_fonts**, **embedding\_size**, and **embedding\_matrix** based on your Word2Vec model.
    *   Create and compile the Siamese neural network using the provided code.
3.  **Training:**
    *   Train the Siamese model on your font dataset using the **fit** method.
4.  **Recommendation:**
    *   Use the **recommend\_fonts** function to recommend fonts based on a given base font.
