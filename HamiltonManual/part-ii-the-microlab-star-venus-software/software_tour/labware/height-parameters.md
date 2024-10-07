# Height Parameters

Both the rack and the container have clearance heights. This is the minimal height at which the pipetting channels must pass over the labware so that their movement is not blocked by the labware. The software automatically takes the highest clearance height.&#x20;

The maximum pipetting height is the deepest position the tip or needle can be placed inside a well. It is counted from the bottom of the container upwards and determines the dead volume of the container.&#x20;

The LLD search height is the height at which the speed of the pipetting channel is reduced to look for the liquid surface.&#x20;

<figure><img src="../../../.gitbook/manual-images/assets/image (213).png" alt=""><figcaption></figcaption></figure>

**Container:**

A: Clearance height&#x20;

B: LLD search height&#x20;

C: Maximum pipetting height&#x20;

D: Container bottom thickness&#x20;



**Rectangular Rack:**

E: Total calculated clearance height&#x20;

F: Distance from rack base to container base Carrier (Template):

G: Clearance height&#x20;

H: Origin Z (also called “Base Offset”)&#x20;

I: Snap to site of base of rack or to container \


Regarding the z position, two different cases of rack placement on the deck can be distinguished in the STAR which is controlled by the switch “I” in the sketch above:&#x20;

<details>

<summary>“Container-Based” Rack - Snap to base of container </summary>

A “Container-Based” Rack is placed with the container bottom directly on the carrier (e.g. the microplates on a plate carrier):

<img src="../../../.gitbook/manual-images/assets/image (214).png" alt="" data-size="original">

The reference position Z0 is the lowest position in the well. Here, the reference height is calculated from

Z0 = Zdeck + Zcarrier + Zthick ,

Zdeck is fixed at 100mm,

Zthick (D) is defined in the container labware,

Zcarrier (H) is defined in the carrier template definition.

A "Rack-Based" Rack is placed with the frame on the instrument deck (e.g., a tube rack, where Zcarrier (H) = 0, because the tube rack is used directly as a carrier)

</details>

<details>

<summary>“Rack-Based” Rack - Snap to base of rack</summary>

A “Rack-Based” Rack is placed with the frame on the instrument deck (e.g., a tube rack, where Zcarrier (H) = 0, because the tube rack is used directly as a carrier)

![](<../../../.gitbook/manual-images/assets/image (215).png>)

The reference position Z0 is the lowest position in the well. The reference height is calculated using: Z0 = Zdeck+Zcarrier+Zbasediff+Zthickness

Zdeck is a fixed quantity

Zcarrier (H) is defined in the carrier definition

Zbasediff (F) is defined in the rectangular rack labware Zthickness (D) is defined in the container labware

</details>
