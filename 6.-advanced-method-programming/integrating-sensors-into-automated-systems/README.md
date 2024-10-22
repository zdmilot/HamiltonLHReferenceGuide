# Integrating Sensors into Automated Systems

Implementing sensors is an effective way to monitor and understand the physical world within the digital realm of automation. These sensors provide crucial insights into:

* **Ambient environmental conditions**
* **Temperature at specific points or for specific liquids**
* **Physical location of objects**
* **Sample storage conditions** (e.g., CO2 levels, temperature, humidity)

This data is invaluable in automation systems, especially for processes that rely heavily on environmental stability and precision, like scientific assays.

### Sensors vs. Indicators

It's essential to differentiate between **sensors** and **indicators**:

* **Sensors**: These are devices that monitor various environmental or operational conditions, such as:
  * Temperature
  * Humidity
  * CO2 levels
  * Oxygen flow
  * Power consumption
  * Presence detection (using IR beams or reflectors)
  * Ultrasonic liquid level detection
  * Magnetic door sensors
  * Flood detection
* **Indicators**: These typically refer to biological metrics, such as:
  * **pH levels**: Gauging the acidity or basicity of a solution
  * **Bacterial contamination**: Monitoring for unwanted bacterial presence
  * **Cell viability**: Checking whether cells remain healthy and functional during processes

#### Example: Canary in a Coal Mine vs. Thermometer

A classic example of an **indicator** is a _canary in a coal mine_. The canary provides a **binary** signal: if the bird dies, it’s an immediate "no-go" for human safety due to toxic gases. This is a clear, go/no-go decision based on a specific condition.

In contrast, a **thermometer** is a **sensor** that provides a **range of values** (e.g., temperature), which can be evaluated to determine if they fall within an acceptable range. If the temperature is within a predefined range, the system can proceed ("go"). If not, adjustments are needed ("no-go").

In automation:

* **Indicators** are often more **binary** (e.g., go/no-go based on a specific condition).
* **Sensors** allow for a **range of values** that can be monitored and evaluated to ensure they fall within a specific threshold.

#### Blurring the Lines: Indicators as Sensors in Automation

In biology and automation, the distinction between sensors and indicators can become blurred. For example, **IR beam presence detection** may technically be an indicator, signaling a binary result (object present or not). However, due to how it interfaces with automation systems, it is often referred to as a sensor.

> Generally speaking, these devices are still called **sensors** since they produce signals that can be easily evaluated digitally. But the line between **physical indicators** and **digital sensors** can sometimes be vague, especially when dealing with both physical and digital data in an automated environment.

#### Working Together: Sensors and Indicators

When combined, sensors and indicators offer a more comprehensive understanding of an automated process. For example:

> If your sensor indicates that environmental conditions are ideal, yet your biological indicator shows contamination, it signals that the workflow still needs improvement, even if physical conditions seem fine.

Conversely:

> If an indicator suggests no contamination, but a sensor detects inadequate airflow in the sterile field, that inconsistency should raise concerns and may prevent the assay from passing validation.

#### Key Sensors in Automation

Here are some key sensors often used in automation systems:

| Sensor Type                       | Purpose                                                     |
| --------------------------------- | ----------------------------------------------------------- |
| Ambient temperature sensors       | Monitor environmental temperature to ensure stability       |
| Humidity sensors                  | Track moisture levels which can affect sample integrity     |
| Light/lux sensors                 | Measure light exposure, critical for light-sensitive assays |
| CO2 and oxygen sensors            | Monitor gas levels in incubation or storage environments    |
| IR beam detectors                 | Detect object presence or movement                          |
| Magnetic door open sensors        | Ensure doors remain closed for safety or sterility          |
| Ultrasonic liquid level detectors | Measure liquid levels in storage containers                 |
| Liquid presence/flood detectors   | Alert when liquids are present where they shouldn't be      |
| Power consumption monitors        | Track energy usage, helping to prevent system overloads     |

### Application in Sensitive Assays

For sensitive assays, environmental conditions such as light, temperature, and humidity can significantly influence the outcome. For instance:

> **Acids** or other sensitive reagents may behave differently under varying environmental factors. Sensors that track these conditions provide critical data that can explain variations in results.

Additionally, monitoring how the automated system is operating—such as detecting an overflowing plate washer—can prevent damage to equipment and ensure laboratory safety.

### Data Communication: Direct Connection vs. Centralized Database

There are two common ways for sensors to communicate with automated systems or end-users:

1. **Direct PC Connection**:
   * Typically uses serial or digital connections.
   * Advantages: Allows data collection even in systems without internet access.
   * Disadvantages: Data is often not logged over time, making it difficult to track historical trends or notify key personnel of deviations.
2. **Centralized Database (API-Based)**:
   * Examples: **Watt IQ**, **Elemental Machines Dashboards**
   * Advantages:
     * Interdepartmental transparency.
     * Multiple automation cells can access data from a central location.
     * Historical records of sensor data.
     * Centralized record management.
   * Disadvantages:
     * Most systems use APIs to access sensor data, which can be rate-limited.
     * Frequent API calls may lead to server overload, particularly in complex automation setups where numerous data points are being monitored at once.

#### Comparing Approaches

| Connection Type          | Advantages                                                           | Disadvantages                                |
| ------------------------ | -------------------------------------------------------------------- | -------------------------------------------- |
| **Direct PC Connection** | Allows data collection in offline systems                            | Limited data logging and historical tracking |
| **Centralized Database** | Allows for transparency, historical records, and multi-device access | Potential API rate-limiting issues           |

### Integration Strategy

The key to building a compliant, consistent, and transparent automated system is choosing the right data entry and exit strategy. Often, this means incorporating both methods of data collection.

*   **Local Sensing**: Sensors like **IR beam detectors** for presence detection are best used within a specific automated work cell. For example:

    > Verifying a door is closed or confirming the presence of an object on a deck can be achieved more effectively through local data collection.
*   **Centralized Monitoring**: Other sensors, such as **ambient temperature monitors**, benefit from centralized logging.

    > These sensors can provide interdepartmental transparency, allowing teams to proactively correct environmental deviations.

#### Examples of Integration

1. **IR Beam Detectors**:
   * Typically used locally to detect whether objects or equipment are in the right position.
   * Best for applications like ensuring a door is closed.
2. **Flood Detection Sensors**:
   * Ideal for centralized logging, especially when monitoring liquid handling systems.
   * When water is detected in an undesired location, this data is useful for cross-departmental transparency and safety.

### Conclusion

Successfully integrating sensors and indicators is essential for creating automated systems that are efficient, compliant, and transparent. Choosing the right method of data collection, whether through direct connections or centralized databases, will ensure that automation engineers provide the most reliable solutions for their operations. By blending both methods, automation engineers can monitor conditions in real-time while also ensuring that long-term trends and potential issues are easily identified and addressed.
