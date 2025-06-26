# Comparison Table – Video 2

| Timestamp               | Manual transcription                | Whisper transcription                     | Correct/Error type      | Notes                                                        |
|------------------------|-------------------------------------|--------------------------------------------|-------------------------|--------------------------------------------------------------|
| [00:04.000 --> 00:08.000] | Ti… bere… (?)                       | Timbers...                                 | Substitution           | Whisper hallucinated a name based on unclear input.          |
| [00:08.000 --> 00:12.000] | Tibes (?)… okay                     | Timbers...                                 | Substitution           | Hallucinated a name again; "okay" omitted                    |
| [00:12.000 --> 00:16.000] | No                                  | No                                         | Correct                |                                                              |
| [00:16.000 --> 00:20.000] | Yeah yes                            | Yes                                        | Partially correct      | Repetition skipped.                                         |
| [00:20.000 --> 00:24.000] | Yes                                 | Yes                                        | Correct                |                                                              |
| [00:28.000 --> 00:32.000] | S... Cause... I... I per... I per… (?) | My name is George Timbers.                 | Hallucination + Substitution | Whisper inserted completely unrelated fluent sentence.       |
| [00:32.000 --> 00:36.000] | INAUDIBLE                           | Because I'm bad.                           | Hallucination          | Whisper guessed meaning.                                   |
| [00:36.000 --> 00:40.000] | INAUDIBLE                           | No.                                        | Hallucination          | No audible input; Whisper guessed.                          |
| [00:40.000 --> 00:44.000] | I bet… (?)                          | I'm bad.                                   | Substitution           | Guessed fluent phrase based on unclear utterance.           |
| [00:48.000 --> 00:52.000] | I bet (?)                           | I'm bad.                                   | Substitution           | Same                                                         |
| [00:52.000 --> 00:56.000] | Yes, Richy                          | Yes, Richmond.                             | Partially correct      | Proper name mismatch, but partially phonetically close.     |
| [01:00.000 --> 01:04.000] | One-two-three.                      | 1-2-3.                                     | Correct                |                                                              |
| [01:04.000 --> 01:08.000] | Yes.                                | Yes                                        | Correct                |                                                              |
| [01:12.000 --> 01:16.000] | I… I pet am… I… (?)                 | I'm bad.                                   | Substitution + Hallucination | Whisper transformed broken sentence into fluent wrong meaning. |
| [01:16.000 --> 01:20.000] | Shuesday Wednesday Thirday          | Tuesday, Wednesday, Friday,                | Partially correct (repair) | Corrected mispronunciations, but substituted.               |
| [01:20.000 --> 01:24.000] | Friday Saturday Sunday              | Friday, Saturday, Sunday.                  | Correct                |                                                              |
| [01:24.000 --> 01:28.000] |                                     | Monday.                                    | Insertion              | No input in manual, Whisper guessed.                        |
| [01:32.000 --> 01:36.000] | Uh… Monday                          | Monday.                                    | Partially correct      | Filler removed.                                             |
| [01:36.000 --> 01:40.000] | Monday, yes                         | Monday... yes.                             | Correct               |                                                              |
| [01:40.000 --> 01:44.000] | Yes                                 | Yes.                                       | Correct               |                                                              |
| [01:44.000 --> 01:48.000] | Um, sh, uh, yes                     | Jeter...                                   | Hallucination         | Whisper interpreted sound as a name.                        |
| [01:48.000 --> 01:52.000] | Yes                                 | Yes                                        | Correct               |                                                              |
| [01:56.000 --> 02:00.000] | Thank you                           | Thank you                                  | Correct               |                                                              |

**Conclusion:** when dealing with severe aphasia, Whisper struggles significantly. It tries to reconstruct the meaning of the phrases which are inaudible, what leads to hallucinations, for example, "My name is George Timbers", "I am bad". So, Whisper tries to make the speech more meaningful than it is,  and it is misleading.