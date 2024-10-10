# Random Access with 16 1000µl-Pipetting Channels

A 4-Channel or 8-Channel instrument has random access to all positions of the deck. This means that pipetting channel No. 1 (rear most) is able to aspirate from e.g. well H1 on a plate placed on the front most plate carrier position. Having more pipetting channels result to a smaller random access area. This is because of the number of pipetting channels that must be moved over. Random access means that (e.g. due to a hit picking) the order of pipetting channels to proceed a sequence may be random.

Deck Areas for Random Access of Different Numbers of Pipetting Channels\


<figure><img src="../.gitbook/assets/image (551).png" alt=""><figcaption></figcaption></figure>



The 16-Channel Instrument is intended to be used as a batch-like processor. This means that all 16 pipetting channels should aspirate and dispense simultaneously in order to allow maximum parallel organization and highest pipetting speed. In this case, the reduced random access space of a 16-Channel Instrument does not cause any problems.

To achieve a batch-like process, all sequences involved must consist of blocks of at least 8, or better 16 positions. Sequence positions within a block must have:

* The same x-positions
* Decreasing y-positions from pipetting channel 1 (rear-most) to 16 (front-most) To program a method using single steps:
*   Select the option “keep pattern” within the “Channel Settings” Dialog in all single steps (tip pick-up, tip eject, aspirate, dispense). Do not use the option “All sequence positions”.



<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (10) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The limitation of the random access area on an instrument deck is also valid for instruments equipped with 5ml-pipetting channels and any combination of 1000µl-pipetting channels and 5ml-pipetting channels. Other equipment such as the tube gripper or the camera channel will also reduce the area for random channel access.</p></td></tr></tbody></table>



Even if an error occurs and “Exclude Channel” is selected as an error recovery, the pattern will be kept.

To program a method using Smart Steps perform the following:

* Select “Copy Pattern”
* Do not select “Exclude Erroneous Positions”
* If sequences can be reloaded (in run time during the pipette command), deselect the option “reducible by user” to maintain the original block-wise structure of the sequences

