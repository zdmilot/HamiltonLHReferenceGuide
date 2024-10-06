# Microplate Robots

Robots! Isn’t that why we’re all here? Robots are what make the world of lab automation go ‘round. This is a starter guide to the types of plate-handling robots you may find in an automated lab.

What is or isn’t a robot is surprisingly hard to agree on, but in this context we'll call robots the devices that physically manipulate samples on their way to or from a lab instrument. This binary between “robots” and “lab instruments” is fairly artificial; most automated lab instruments could qualify as robots in a technical sense, but it helps to separate the devices that do lab work from the devices that shuttle plates around a lab or workcell.

#### Articulated Robots

<figure><img src="../.gitbook/assets/image.png" alt="" width="375"><figcaption></figcaption></figure>

Articulated robot arms are the standard in industrial automation, but they are much less common in the lab. They are most popularly constructed with 6 axes, excluding the end effector.

A full range of motion and rotation makes articulated robots extremely flexible in their applications. With enough careful programming, they can perform movements that are nearly identical to a human arm. However, this flexibility makes them tricky to program for a novice.

Articulated robots operate within a coordinate system that most find unintuitive, and their flexibility is generally unecessary for a traditional workcell. But for specialty applications, they cannot be beat.



#### SCARA

![](https://theautomatedlab.com/assets/images/content/scara-diagram.png)

Selective Compliance Articulated Robot Arm (SCARA) is the standard for microplate manipulation. SCARA robots have selective compliance, meaning there are some ways they cannot move. This is a problem if you need your robot to reach a full range of motion and rotation, but it is a benefit if your robot needs to carry a pitcher of water without spilling it.

![Roll, pitch, and yaw are the terms for rotation about the x, y , and z axis. Microplate 'pick and place' operations, the movement of a payload from location A to location B, require that pitch and roll be held constant throughout the entire operation.  If not, the plate's contents may be spilled.](https://theautomatedlab.com/assets/images/content/rotation-diagram.png)

Microplates and sample tubes need to be kept level at all times to prevent spillage, with few exceptions. SCARA robots ensure this through an inability to change the pitch or roll of its payload. SCARA robots generally have four or five axes, excluding the end effector. Colloquially, these are called the column, shoulder, elbow, and wrist. Sometimes the column is able to rotate about the base, significantly widening the arm’s work envelope.

SCARA robots in the life sciences are almost all designed to be collaborative through low-force movements and collision detection. Lab-specialized SCARA robots tend to be expensive, but are ultimately more approachable for someone new to robotics and meet all of the criteria needed for a standard integrated workcell robot.



#### Cartesian Robots

![](https://theautomatedlab.com/assets/images/content/cartesian-diagram.png)

Cartesian robots move along three orthogonal axes: x, y, and z. They are generally suspended in a frame with the end effector operating below, much like a claw machine in an arcade.

Cartesian robots rely on three linear actuators for their movement, with potential for additional rotation or fine movement at the end effector. This makes them simple to teach and cheap to assemble compared to other robots.

They have a rectangular work envelope, rather than the round envelope of articulated and SCARA arms. This makes them ideal for embedding inside devices that may require on-deck plate movement: liquid handlers.

|      | Articulated Robot                                                                                                                                 | SCARA                                                                              | Cartesian Robot                                                                                                 |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Pros | <ul><li>can be programmed to do just about anything</li><li>a more common industrial robot, therefore more cost and feature flexibility</li></ul> | <ul><li>more likely to be collaborative</li><li>always keeps plate level</li></ul> | <ul><li>cheapest build</li><li>easiest to teach</li><li>keeps plate level through hardware constraint</li></ul> |
| Cons | <ul><li>less common in the lab, therefore vendors may be less familiar with desired application</li><li>potential safety hazard</li></ul>         | <ul><li>expensive</li><li>unable to perform pitch or roll movements</li></ul>      | <ul><li>use cases are limited</li><li>requires support frame around work envelope</li></ul>                     |

#### Collaborative Robots (Cobots)

Collaboration is defined by the inability of a robot to maim a human who wanders into its path. I personally prefer a higher standard for collaboration, but this is an important distinction to make among robots.

Industrial robots have historically targeted functions that are quite dangerous for humans: heavy lifting, welding, manipulation of large metal objects. Robots with the capacity to lift cars and puncture steel are inherently dangerous, as humans are notoriously easier to puncture than steel.

Collaborative robots are designed for use in proximity to humans, and therefore are designed as much for human safety as they are for their functional purpose. They are made collaborative through some combination of restricted speed and force, sensors to detect the presence of obstacles, and elimination of sharp edges and heavy moving parts.

Most robots in the lab are collaborative given that payloads are often quite light and there is simply no need to use machines that risk human safety. This comes with the added benefit that the robots are far less likely to destroy nearby lab equipment in the event of a robot crash.

Humans will attempt to circumvent every measure you put between them and bodily harm, which is why your priority as an engineer is to remove the potential for bodily harm. I have watched scientists reach through crowded equipment into moving workcells only to be bonked in the head by a collaborative robot. Thanks to the collaborative design, the low-force collision triggered an immediate equipment stop that could be later resumed by the on-call engineer. Only egos were damaged that day.

#### Mobile Robots

Every year at lab automation conferences I see demos of mobile robots shuttling plates from station to station. Imagine a roomba. Now imagine a robot arm the size of a small human bolted to said roomba. There you go, that’s a mobile lab robot.

Rather than being a statically positioned arm maneuvering plates from one device to another in a workcell, a mobile robot is designed to shuttle plates from workcell to workcell. They generally have a suite of sensors that allow them to navigate a lab and identify work stations, often by barcode or other visual cue. They are generally collaborative, as they are designed to freely wander lab space shared with humans.

I assume someone, somewhere, has purchased a mobile lab robot, but I have yet to see a lab that makes use of them. While conceptually interesting, mobile robots solve for a problem that is currently far downstream of the biggest challenges an automated lab faces.



***

Source: [https://theautomatedlab.com/article.html?content=lab-robots](https://theautomatedlab.com/article.html?content=lab-robots)
