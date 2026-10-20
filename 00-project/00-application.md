---
name: Sulehan
neptun: CRX1CQ
---

# Processing Mammographic Images for Tumor Detection

## My interpretation of the brief

I understand this project as an investigation of image-processing and machine-learning methods for detecting suspicious findings in mammograms.

The analysis would consider grayscale intensity together with texture, shape, edges, suspicious regions, and surrounding tissue. Image or lesion classification, lesion localisation, and distinguishing benign from malignant findings are different tasks. I would agree on a manageable task with my supervisor according to the available annotations.

## Why I am a good fit for this project

I am interested in how artificial intelligence learns useful patterns from medical images and how differences between patients affect its predictions.

My initial question is whether similar visual features should always lead to the same interpretation for patients with different characteristics. I would like to investigate whether combining images with available information, such as age, breast density, and relevant medical history, improves performance compared with using images alone.

I am also interested in whether a model performs consistently across different patient groups. I would like to investigate this experimentally rather than assume that adding information or dividing patients into categories automatically improves accuracy.

## Relevant experience and background

Through my current Project Work, I am gaining experience in defining a software project, analysing technical problems, and maintaining documentation in GitHub.

I would like to develop these skills further while learning about medical image preprocessing, supervised learning, and experimental evaluation. This project interests me because it combines software development with the investigation of a practical research question.

## Proposed approach

I would first review existing methods and inspect a suitable, appropriately licensed and de-identified dataset. I would examine its images, annotations, class distribution, and available patient information.

Next, I would prepare a reproducible preprocessing pipeline and establish an image-only baseline using a suitable pretrained image model where practical.

If sufficient metadata is available, I would compare the baseline with a model combining image features and structured patient information, using the same patient splits and evaluation conditions. Age could be represented numerically, while categorical variables would be encoded appropriately. Sex would be considered only if it varies meaningfully and sufficient samples are available.

I would initially use a shared model and evaluate performance across sufficiently represented age and breast-density groups. I would examine uneven data distributions and underrepresented groups, recognising that overly fine grouping can leave too few samples for reliable conclusions. Separate models for individual groups would require enough training data to support a meaningful comparison.

All images belonging to the same patient would remain in the same training, validation, or test partition. Only information available at prediction time would be used as input. Pathology results and other information revealing the target would be excluded from inputs. Any learned preprocessing would be fitted on training data only.

Evaluation would include sensitivity, specificity, precision, and suitable ROC-AUC or PR-AUC measures alongside accuracy, together with an analysis of false positives and false negatives. If localisation is included, corresponding localisation metrics would be selected according to the annotations.

## Initial plan

1. Confirm the scope and expected outputs with the supervisor.
2. Review existing methods and select a suitable dataset.
3. Inspect the images, annotations, and patient information.
4. Implement preprocessing and patient-level data partitions.
5. Develop and evaluate an image-only baseline.
6. Investigate image-plus-metadata modelling if suitable data is available.
7. Analyse errors and performance across patient groups.
8. Document the results, limitations, and possible improvements.

## Additional information

The core project would focus on mammographic image analysis. Patient information would be an optional extension supported by the available dataset.

The main deliverables would be a documented academic research prototype, reproducible experiments, and a comparison of the selected approaches. Any improvement would need to be demonstrated on held-out data. The prototype would not be intended for clinical diagnosis.

The final scope would be agreed with the supervisor according to dataset access and available computing resources.

GitHub repository:
https://github.com/lehansu755-a11y/Mammogr-f-k-pek-feldolgoz-sa-daganat-detekt-l-si-c-lb-l
