# GRACE digital twin

In the GRACE mock data challenge project, I successfully generated data for each of the five sensors within GRACE Follow-on satellites. These efforts allowed me to create digital twins for each instrument, resulting in simulated observations spanning one month.

Traditionally, digital twin creation involves utilizing force models, integrating them, and solving ordinary differential equations to determine satellite positions. This approach incorporates data from GPS observations, KBR or LRI observations, and accelerometer measurements. Essentially, a distinct model is employed for each sensor.

However, for the star camera data, which provides attitude information, I took a different path. Instead of using a model, I engaged in a reverse engineering process. Yet, to establish a digital replica of each instrument, I proposed a distinct approach inspired by Saniya Behzadpour's work on GRACE presented at EGU 2023.

The fundamental concept involves utilizing actual GRACE data to construct digital copies, rather than relying on models. This notion emerged when an accelerometer malfunction occurred in one GRACE Follow-on satellite, leading to the transplantation of an accelerometer from another satellite. As a result, the functioning accelerometer effectively served as a digital copy of its counterpart.

This idea encompasses generating transplant data solely using the available data, without integrating any models. While TU GRAZ also produces transplant data, they combine models with data. In contrast, I propose utilizing machine learning techniques to generate accelerometer data for the other satellite. By training a supervised machine learning architecture with GRACE A accelerometer data as input and GRACE B accelerometer data as output, we can achieve the desired results.

In theory, this approach can be applied to all instruments within GRACE, including star cameras and GPS. By training a model based on data from one satellite, we can obtain digital replicas of the instruments in the other satellites.

This concept holds significant interest as it addresses the missing months between GRACE and GRACE Follow-on missions. Furthermore, we can push the boundaries further, drawing inspiration from Transformers language models. By providing the entire GRACE mission to a machine learning architecture, we could generate future GRACE missions or explore different satellite constellations. These simulations could potentially yield significant improvements in calculating the gravity field, such as utilizing twin GRACE Follow-on satellites and their digital counterparts with a Bender constellation.
