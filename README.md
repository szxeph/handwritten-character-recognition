# Handwritten Character Recognition

A computer vision project for classifying handwritten digits and Latin letters from the EMNIST ByClass dataset.

The notebook covers data exploration, stratified splitting, image augmentation, CNN training, evaluation with accuracy and macro F1, and error analysis for visually similar characters.

## Results

The final model was trained for eight epochs on the full EMNIST ByClass training split.

| Metric | Value |
|---|---:|
| Validation accuracy | 0.871 |
| Test accuracy | 0.8717 |
| Test macro F1 | 0.7421 |

Most errors occur between visually similar classes such as `l/1/I`, `0/O/o`, `5/S/s`, and uppercase/lowercase variants. These cases are inherently difficult to distinguish without word context.

## Stack

- Python
- PyTorch
- torchvision
- scikit-learn
- pandas
- Matplotlib and Seaborn

## Files

- `handwritten_character_recognition.ipynb` - the complete experiment
- `requirements.txt` - project dependencies

## Run

Open the notebook in Google Colab, select a GPU runtime, and run all cells in order. EMNIST is downloaded automatically through torchvision. Set `FAST_RUN = True` for a shorter smoke test.

## Next step

The trained character classifier can later become part of an OCR pipeline. Document OCR also requires reliable line and character segmentation, so this extension is treated as a separate experiment rather than an already solved task.
