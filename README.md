# Emotion-VLLM
Emotion-VLLM: Emotion Knowledge Enhancement for Vision Large Language Models: A Self-Verification Approach for High-Quality Emotion Instruction Data Generation

Abstract  
Facial emotion perception in vision large language model (VLLM) is a crucial element for achieving natural human-machine interaction. Creating high-quality emotion analysis annotations for downstream emotion analysis tasks demands costly expertise and specialized domain knowledge. Likewise, the lack of high-quality emotion analysis instruction data limits the performance of VLLMs in facial emotion perception. Given the issues mentioned above, in this paper, we proposed a self-verification approach with emotion knowledge enhancement (SEFK) to generate high-quality instruction data for facial emotion analysis using VLLM in a cost-effective manner. We integrate high-quality annotations from facial expression recognition (FER), action unit (AU) detection, and valence/arousal estimation (VAE), along with the emotion analysis capabilities of VLLMs, and propose a self-verification method with Uncertainty-Aware Monte Carlos samplings (SV-UAMC) to generate reliable instructions in a low cost manner." Additionally, we released a facial emotion analysis instruction dataset and introduced a facial emotion analysis benchmark to measure the facial emotion perception abilities of VLLM. Extensive experiments have shown the effectiveness of the proposed method for high-quality facial emotion instruction data generation.

## The FEID and FEAB Dataset

### General Information

The FEID (Facial Emotion Instruction Dataset) and FEAB (Facial Emotion Analysis Benchmark) are designed for training and evaluating facial emotion analysis models across three tasks: discrete emotion classification, valence/arousal estimation, and AU detection. 

FEID includes 26,238 training samples sourced from six datasets: **CK+**, **RAF-DB**, **AffectNet**, **DISFA**, **BP4D**, and **Aff-Wild2**, with annotations for emotions, valence/arousal, and 17 AU categories. 

FEAB, sourced from the same six datasets, contains 3,035 test samples independently selected to ensure generalizability, covering diverse emotional descriptions and AU occurrences.

Download the [datasets](https://drive.google.com/drive/folders/1zaKqDFNuQLkWHFyL27CVmjXgmyyaqWG2?usp=sharing), categorized by the original databases, where *train* represents **The FEID** and *test* represents **The FEAB**.

### Generated Instruction Data

We leverage GPT-4o and design an **uncertainty-aware self-verification** method to complete missing emotion descriptions. 

By embedding prior knowledge and estimating epistemic uncertainties through adaptive Monte Carlo sampling, we generate reliable emotion descriptions, including discrete emotion categories, valence/arousal values, and AU activations. This approach enables **high-quality instruction data generation** without extra manual annotations.

Download the [instruction data annotations](https://drive.google.com/drive/folders/1-Wmw_zjUv9JLAlYykg-DeWyGfYSv4LaO?usp=sharing), categorized by the original databases.

