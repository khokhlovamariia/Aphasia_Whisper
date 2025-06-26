#  Evaluating Whisper on Broca's Aphasic Speech
This project investigates the accuracy of OpenAI's Whisper speech-to-text model on YouTube videos of patients with Broca's aphasia. It compares Whisper-generated transcriptions with manually created ones using both subjective evaluation and objective metrics.

## Project goals
- Collect openly available video/audio records of aphasic speech
- Extract transcriptions of aphasic speech from YouTube using Whisper
- Manually transcribe the same speech records for comparison
- Identify typical errors Whisper makes with aphasic speech
- Evaluate Whisper's performance using multiple comparison metrics

## Video selection
**13** openly available videos were used for analysis with the **total duration of 43 minutes**. The samples vary by speaker gender and aphasia severity (mild, moderate, severe), and include both real stroke survivors and educational simulations. Details for each sample can be found [here](data/selected_videos/selected_videos.md).

## Manual analysis of transcriptions
The goal of the manual analysis was to evaluate how Whisper handles aphasic speech and identify recurring errors.
#### Transcription Error Types

| **Error Type**          | **Description**                                |
|-------------------------|------------------------------------------------|
| **Omission**            | Word was skipped or left out                   |
| **Insertion**           | Extra word was added that wasn't spoken        |
| **Substitution**        | Incorrect word was used instead of the right one |
| **Fluency Smoothing**   | Grammar was polished unnaturally               |
| **Hallucination**       | Content was invented (not present in speech)   |
| **Repetition Skipping** | Repeated words were dropped                    |
| **Semantic Drift**      | Meaning was changed even if sentence remained fluent |


Comparison tables for each sample with error types and notes can be found here:
* [Manual comparison for Video 1](data/manual_comparison_tables/comparison_1.md)
* [Manual comparison for Video 2](data/manual_comparison_tables/comparison_2.md)
* [Manual comparison for Video 3](data/manual_comparison_tables/comparison_3.md)
* [Manual comparison for Video 4](data/manual_comparison_tables/comparison_4.md)
* [Manual comparison for Video 5](data/manual_comparison_tables/comparison_5.md)
* [Manual comparison for Video 6](data/manual_comparison_tables/comparison_6.md)
* [Manual comparison for Video 7](data/manual_comparison_tables/comparison_7.md)
* [Manual comparison for Video 8](data/manual_comparison_tables/comparison_8.md)
* [Manual comparison for Video 9](data/manual_comparison_tables/comparison_9.md)
* [Manual comparison for Video 10](data/manual_comparison_tables/comparison_10.md)
* [Manual comparison for Video 11](data/manual_comparison_tables/comparison_11.md)
* [Manual comparison for Video 12](data/manual_comparison_tables/comparison_12.md)
* [Manual comparison for Video 13](data/manual_comparison_tables/comparison_13.md)


Overall, Whisper performs well in capturing the key meaning. Even if the speech is fragmented or unclear, it tries to reconstruct it and often does it correctly. 

Most common error types are:
* Missing fillers
* Repetition skipping
* Substitutions

For the task of understanding the patients, Whisper output is very useful. It can translate the impaired speech to the fluent one and therefore be a mediator between the aphasia patient and others, simplifying communication.

However, for the clinical purposes, its tendency to smooth and clean up the speech may not give the realistic representation of speech impairment severity.

## Aphasic speech transcription with Whisper

The notebook [whisper_transcription.ipynb](notebooks/whisper_transcription.ipynb) downloads aphasic speech samples from YouTube videos listed in [video_urls.txt](data/selected_videos/video_urls.txt) and transcribes them with Whisper.

1. For each video, the best audio is extracted and saved in .wav format using **yt_dlp** (library to download audio/videos). Audio files are saved in [data/audio folder](data/audio).
2. The **medium-size Whisper model** is used to transcribe each audio file.
3. Each transcription is saved as a .txt file in [data/whisper_transcriptions folder](data/whisper_transcriptions).