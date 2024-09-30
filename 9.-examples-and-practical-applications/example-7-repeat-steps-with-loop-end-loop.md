---
description: >-
  Using the 1000µL channels, you will be creating a method that will repeatedly
  aspirate and dispense a fixed number of times from sample tubes to 96-Well
  plate in three separate loops.
---

# Example 7: Repeat steps with Loop-End Loop

1. Using your Basic\_Deck layout that we’ve been adding to through the course of the challenges, create a new method, and name it Repeat\_Samples\_To\_Plates.
2. In the Deck Layout editor, change the Stamp Tool from Head 96 to 1000µl Channels
3. Create a new Sequence, SamplesTubes96 which consists of all 4 Sample Tube Carriers.

<figure><img src="../.gitbook/assets/image (281).png" alt=""><figcaption></figcaption></figure>

\*Note - Use the format shown above.  One for each transfer so we can repeat the Aspirate and Dispense steps.

4. Transfer 50µL from 48 samples (our new sequence, SamplesTubes96) to the first 6 columns of first plate sequence (Nun\_96\_Fl\_Lb\_0001).&#x20;
5. Add the step Sequence: Set Current Position so the SampleTubes96 sequence starts at the first tube again.

<figure><img src="../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure>

6. Create a second Loop.  Transfer 50µL from 96 samples to 12 columns of second plate (Nun\_96\_Fl\_Lb\_0002).
7. Add the step Sequence: Set Current Position so that SampleTubes96 sequence starts at the first tube again.
8. Create a third Loop.  Transfer 50µL from the same 8 samples (SamplesTubes96) to 12 columns of thirdplate (Nun\_96\_Fl\_Lb\_0003) so there are identical samples across the row.
9. Save and launch Run Control.  Simulate the method and correct any errors.

## Optional Expert Challenge

1\.    Using “Save As”, save a copy of the method, call it Repeat\_Samples\_To\_Plates\_Extra.

2\.    Transfer 900µL from the first 8 sample tubes of the first tube carrier (SMP\_CAR\_24\_15x75\_A00\_0001) to the first 8 sample tubes of the second carrier (SMP\_CAR\_24\_15x75\_A00\_0002) using only 300µL tips.

3\.    Transfer 50µL from all samples (SamplesTubes96) to first three plates (define a new Sequence for this) so that each sample tube carrier matches to one column across all 3 plates, i.e.

Samples 1-8 (SMP\_CAR\_24\_15x75\_A00\_0001) to

Column 1 Plate 1 (Nun\_96\_Fl\_Lb\_0001),

Samples 9-16 (SMP\_CAR\_24\_15x75\_A00\_0001) to&#x20;

Column 1 Plate 2 (Nun\_96\_Fl\_Lb\_0002),

Samples 17-24 (SMP\_CAR\_24\_15x75\_A00\_0001) to&#x20;

Column1 Plate 3 (Nun\_96\_Fl\_Lb\_0003),

Samples 25-32 (SMP\_CAR\_24\_15x75\_A00\_0002) to

Column 2 Plate 1 (Nun\_96\_Fl\_Lb\_0001),

Samples 33-40 (SMP\_CAR\_24\_15x75\_A00\_0002) to

Column 2 Plate 2 (Nun\_96\_Fl\_Lb\_0002),

Samples 41-48 (SMP\_CAR\_24\_15x75\_A00\_0002) to

Column 2 Plate 3 (Nun\_96\_Fl\_Lb\_0003),

&#x20;

and so on…
