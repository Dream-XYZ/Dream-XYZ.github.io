# DreamStory

Story visualization aims to create visually compelling images or videos corresponding to textual narratives. Despite recent advances in diffusion models yielding promising results, existing methods still struggle to create a coherent sequence of subject-consistent frames based solely on a story. To this end, we propose an automatic open-domain story visualization framework by leveraging the LLMs and a novel multi-subject consistent diffusion model (**DreamStory**).

The DreamStory consists of (1) an LLM acting as a story director and (2) an innovative **M**ulti-**S**ubject consistent **D**iffusion model (**MSD**) for generating consistent multi-subjects across the images. First, DreamStory employs the LLM to generate descriptive prompts for subjects and scenes aligned with the story, annotating each scene’s subjects for subsequent subject-consistent generation. Second, DreamStory utilizes these detailed subject descriptions to create portraits of the subjects, with these portraits and their corresponding textual information serving as multimodal guidance. Finally, the MSD uses this multimodal guidance to generate story scenes with consistent multi-subjects.

Specifically, the MSD includes Masked Mutual Self-Attention (MMSA) and Masked Mutual Cross-Attention (MMCA) modules. MMSA module ensures detailed appearance consistency with reference images, while MMCA captures key attributes of subjects from their reference text to ensure semantic consistency. Both modules employ masking mechanisms to restrict each scene’s subjects to referencing the multimodal information of the corresponding subject, effectively preventing blending between multiple subjects.

To validate our approach and promote progress in story visualization, we established a benchmark, **DS-500**, which can assess the overall performance of the story visualization framework, subject-identification accuracy, and the consistency of the generation model. Extensive experiments validate the effectiveness of DreamStory in both subjective and objective evaluations.
