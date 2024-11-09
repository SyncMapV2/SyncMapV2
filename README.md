# Experiment Tables for SyncMapV2

## Table 1: SyncMapV2 Ablation Study

This table shows an ablation study on various configurations of the SyncMapV2 model, highlighting the contributions of individual components. Each model variation tests a different combination of settings, including Adaptive Learning Rate, Symmetrical Activations, Space Normalization, Moving Average, and Leaking Rate. The table reports the Mean Intersection over Union (mIoU) scores on both clean data and data with Gaussian noise (S3), as well as the improvement percentages over the original SyncMap model.

|                       | **SyncMapV2 Ablation**                 |      |         |                  |      | **mIoU**        |                 | **Improvements from SyncMap**    |                   |
|-----------------------|----------------------------------------|------|---------|------------------|------|-----------------|-----------------|-----------------------------------|-------------------|
| **Model**             | Adaptive Learning Rate                | Symmetrical Activations | Space Normalization | Moving Average | Leaking Rate | Clean           | Gaussian S3      | Clean                           | Gaussian S3       |
| **Orig. SyncMap**     | -                                     | -    | -       | -                | -    | 0.251           | 0.236           | 0%                               | 0%                |
| **AdpLR**             | ✅                                    | -    | -       | -                | -    | 0.290           | 0.255           | 15.5%                            | 8.1%              |
| **SymmAct**           | -                                     | ✅    | -       | -                | -    | 0.162           | 0.143           | -35.5%                           | -39.5%            |
| **Norm**              | -                                     | -    | ✅      | -                | -    | 0.282           | 0.258           | 12.4%                            | 9.3%              |
| **MovMean**           | -                                     | -    | -       | ✅               | -    | 0.301           | 0.282           | 19.9%                            | 19.5%             |
| **LeakR**             | -                                     | -    | -       | -                | ✅    | 0.282           | 0.255           | 12.4%                            | 8.1%              |
| **SymmAct + AdpLR**   | ✅                                    | ✅    | -       | -                | -    | 0.17            | 0.20            | -33.6%                           | -17.0%            |
| **SymmAct + Norm**    | -                                     | ✅    | ✅      | -                | -    | 0.30            | 0.27            | 18.9%                            | 12.9%             |
| **SymmAct + MovMean** | -                                     | -    | ✅      | ✅               | -    | 0.14            | 0.15            | -40.2%                           | -36.8%            |
| **SymmAct + LeakR**   | -                                     | -    | -       | ✅               | ✅    | 0.28            | 0.27            | 10.5%                            | 14.5%             |
| **SyncMapV2**         | ✅                                    | ✅    | ✅      | ✅               | ✅    | **0.33**        | **0.31**        | **31.5%**                        | **31.4%**         |

---

## Table 2: Robustness Testing with Various Corruption Types

This table evaluates the robustness of the DFC, Orig. SyncMap, and SyncMapV2 models under different corruption types and severity levels. The corruption types include Gaussian Noise, Zoom Blur, Snow Weather, and Digital Contrast, each tested at severity levels 1 (S1), 3 (S3), and 5 (S5). The table reports the mIoU scores under each condition and calculates the mean performance for each corruption type, as well as an overall mean performance across all conditions. Additionally, it shows the improvement percentages of SyncMapV2 compared to DFC and the original SyncMap model.

| **Corruption Type**         | **Clean** | **Gaussian Noise**      |               |           |      | **Zoom Blur**            |           |         |      | **Snow Weather**           |           |         |      | **Digital Contrast**      |         |      | **Overall** |
|-----------------------------|-----------|--------------------------|---------------|-----------|------|---------------------------|-----------|---------|------|----------------------------|-----------|---------|------|---------------------------|---------|------|-------------|
| **Method / Severity**       | -         | S1                       | S3            | S5        | **Mean** | S1                       | S3        | S5      | **Mean** | S1                     | S3        | S5      | **Mean** | S1                     | S3      | S5  | **Mean** |
| **DFC**                     | **0.37**  | 0.26                     | 0.23          | 0.21      | 0.23 | 0.27                     | 0.26      | 0.26    | 0.26 | 0.26                     | 0.25      | 0.23    | 0.25 | 0.27                     | 0.27    | 0.25 | 0.26 |
| **Orig. SyncMap**           | 0.25      | 0.24                     | 0.24          | 0.24      | 0.24 | 0.26                     | 0.26      | 0.25    | 0.25 | 0.23                     | 0.23      | 0.24    | 0.25 | 0.26                     | 0.25    | 0.25 | 0.25 |
| **SyncMapV2**               | 0.33      | **0.32**                 | **0.31**      | **0.28**  | **0.30** | **0.32**                 | **0.30**  | **0.30**| **0.31** | **0.32**               | **0.30**  | **0.29**| **0.30** | **0.33**               | **0.33** | **0.32** | **0.31** |
| **Improvements (vs. DFC, %)** | -12%     | **26%**                  | **32%**       | **34%**   | **31%** | **16%**                 | **16%**   | **16%** | **16%** | **20%**                 | **21%**   | **26%** | **23%** | **20%**                | **22%**  | **30%** | **24%** |
| **Improvements (vs. Orig. SyncMap, %)** | **31%**   | **32%**           | **31%**       | **17%**   | **26%** | **21%**                 | **17%**   | **18%** | **20%** | **30%**                 | **31%**   | **25%** | **27%** | **30%**               | **29%**  | **29%** | **26%** |





<!--
**SyncMapV2/SyncMapV2** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
