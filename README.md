# Procrustes Alignment for Text Embeddings

This project provides a Python implementation of the Procrustes alignment method to align text embeddings from different languages or sources into a common vector space. This alignment facilitates tasks such as cross-lingual word embedding mapping and transfer learning.

## Features

- **Manual Loading of `.vec` Files:** Load word embeddings from `.vec` files without relying on external libraries.
- **Procrustes Analysis Implementation:** Align two sets of embeddings by removing differences in translation, scaling, and rotation using NumPy.
- **Orthogonality Constraint:** Ensure the transformation matrix is orthogonal to preserve vector space properties during alignment.

## Requirements

- Python 3.x
- NumPy
- Gensim
- Scikit-learn
- Scipy

## Usage

1. **Load Embeddings:**

   Use the provided function to read word embeddings from `.vec` files:

   ```python
   embeddings_index = load_vec('path_to_your_file.vec')
   ```

2. **Align Embeddings:**

   Align two sets of embeddings (`source_embeddings` and `target_embeddings`) using Procrustes analysis:

   ```python
   aligned_source_embeddings = procrustes_align(source_embeddings, target_embeddings)
   ```

3. **Apply Transformation:**

   Transform new embeddings using the computed alignment:

   ```python
   transformed_embeddings = apply_transformation(new_embeddings, transformation_matrix)
   ```


## License

This project is licensed under the MIT License.
