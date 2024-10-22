# Slave Error IDs – Pipetting Channels

| ID | Error                                            | Description                                                                     |
| -- | ------------------------------------------------ | ------------------------------------------------------------------------------- |
| 0  | No Error                                         |                                                                                 |
| 20 | No communication to EEPROM                       | IC Bus or EEPROM not working                                                    |
| 30 | Undefined command                                | unknown command                                                                 |
| 31 | Undefined parameter                              | Unknown parameter                                                               |
| 32 | Parameter out of range                           | Parameter outside of permitted range                                            |
| 35 | Voltages outside permitted range                 | Hardware not working properly                                                   |
| 36 | Stop during execution of a command               |                                                                                 |
| 37 | Movement interrupted                             | Second core gripper pipetting channel has a step loss                           |
| 40 | No parallel processes permitted                  | Two or more commands sent for the same control process                          |
| 50 | Init. Position not found                         | Hardware not working properly                                                   |
| 51 | Dispensing drive not initialized                 | Command sent prior to device init                                               |
| 52 | Dispense dive movement error                     | Step loss                                                                       |
| 53 | Maximum volume in tip reached                    |                                                                                 |
| 54 | Dispense drive position out of permitted area    |                                                                                 |
| 55 | Y drive blocked                                  | Hardware not working properly                                                   |
| 56 | Y drive not initialized                          | Command sent prior to device init                                               |
| 57 | Y drive movement error                           |                                                                                 |
| 60 | Z drive blocked                                  | Hardware not working properly                                                   |
| 61 | Z drive not initialized                          | Command sent prior to device init                                               |
| 61 | Z drive not initialized                          | Command sent prior to device init                                               |
| 62 | Z drive movement error                           |                                                                                 |
| 63 | Z drive limit stop not found                     |                                                                                 |
| 65 | Squeezer drive blocked                           | Hardware not working properly                                                   |
| 66 | Squeezer drive not initialized                   | Command sent prior to device init                                               |
| 67 | Squeezer drive movement error                    |                                                                                 |
| 68 | Squeezer drive init position adjustment error    |                                                                                 |
| 70 | No liquid level found                            | No liquid present                                                               |
| 71 | Not enough liquid present                        | Immersion depth or surface following position below minimal access range        |
| 72 | Auto calibration at pressure sensor not possible | Hardware not working properly                                                   |
| 73 | No liquid level found with dual LLD              | Difference of LLD positions on dula LLD exceed the maximum allowable difference |
| 75 | No tip picked up                                 | No tip present at position (tip pick-up).  No tip picked up (module commands)   |
| 76 | Tip already picked up                            | A fresh tip cannot be picked up because one is already present                  |
| 77 | Tip not discarded                                |                                                                                 |
| 78 | Wrong tip detected                               | The tip picked up was not of tip type specified                                 |
| 80 | Liquid not correctly aspirated                   | Error in liquid aspiration                                                      |
| 81 | Clot detected                                    |                                                                                 |
| 82 | TADM measurement out of lower limit curve        |                                                                                 |
| 83 | TADM measurement out of upper limit curve        |                                                                                 |
| 84 | Not enough memory for TADM measurement           |                                                                                 |
| 85 | No communication to digital potentiometer        |                                                                                 |
| 90 | Limit curve not resettable                       |                                                                                 |
| 91 | Limit curve not programmable                     |                                                                                 |
| 92 | Limit curve name not found                       |                                                                                 |
| 93 | Limit curve data incorrect                       | Syntax error.  Calculate data address out of limit curve address range          |
| 94 | Not enough memory for limit curve                |                                                                                 |
| 95 | Not allowed limit curve index                    |                                                                                 |
| 96 | Limit curve already stored                       |                                                                                 |

\


\
