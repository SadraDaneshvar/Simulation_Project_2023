<span style="font-family:Times New Roman; font-size:14pt;">
<h2 align="center"><b>Simulation and Performance Evaluation of a Car Insurance Assessment Center</b></h2>
</span>



<span style="font-family:Times New Roman; font-size:15pt;">
<h4><b>1. Problem Overview<b></h4>
<span>
<span style="font-family: Times New Roman; font-size: 13pt;">

The car insurance assessment center is facing challenges related to its operational efficiency and capacity management. With limited resources and a specific working schedule from 8:00 am to 6:00 pm, the center struggles to accommodate all incoming cars and provide timely services. 

One significant issue is that if a car arrives after the center's closing time, it cannot be assessed until the next working day, causing delays and potential customer dissatisfaction. Another factor complicating the center's operations is the requirement for paired cars to arrive together. If one car arrives without its partner, it must wait for the partner to arrive before the assessment process can begin. This prioritization of paired cars further adds to the complexity of managing the center's workflow.

Additionally, the assessment center has a queue for taking photos, but it has a limited capacity. When the queue is full, cars have to wait outside until space becomes available. This not only leads to longer waiting times but also poses challenges in terms of space management and organizing the incoming cars effectively.

To address these issues and improve the overall performance of the center, a comprehensive study has been conducted utilizing discrete-event simulation. This simulation aims to model the system and provide statistical measures of its performance. By simulating various scenarios, we can analyze the system's behavior and identify potential bottlenecks or areas for improvement.

<span style="font-family:Times New Roman; font-size:15pt;">
<h4><b>2. Phase1; System Modeling<b></h4>
<span>
<span style="font-family: Times New Roman; font-size: 13pt;">
  
In the first phase of the project, our main objective was to develop a comprehensive description of the system, both in terms of its static and dynamic aspects. This encompassed the identification and definition of state variables, entities, and events that play a crucial role in the assessment center's operations. Additionally, we created flow diagrams for each event to effectively illustrate the logic and the interconnectedness between them.

State variables, such as queue lengths at different sections of the center, as well as the status of photographers, documenters/fulfillers, complaint experts, and evaluation experts, have been identified to capture the dynamic nature of the system. Entities, representing the vehicles, have also been defined, including attributes such as entrance number, pairing status, and complaint status. Events that impact the state of the system, such as arrivals, departures, and shift start/end, have been categorized to simulate the center's workflow accurately.

Another crucial aspect that required consideration was ensuring that all our activities, including interarrival times, partner arrival times, service durations, and others, adhered to specific distributions and were generated accordingly. While several of these distributions were already known and provided, we had to undertake input modeling for the fulfillment service time to ensure accuracy and appropriateness. To achieve this, we began by preparing the data and subsequently selected a distribution that was both intuitive and in accordance with the nature of the phenomenon under investigation. Following this, we employed a q-q plot to visualize the distribution and conducted statistical tests such as the chi-square and Kolmogorov-Smirnov to validate our hypothesis.

</span>

<span style="font-family:Times New Roman; font-size:15pt;">
<h4><b>3. Phase2; Implementation of Simulation Model and Performance Evaluation<b></h4>
<span>
<span style="font-family: Times New Roman; font-size: 13pt;">

In the second phase of the project, we focused on coding and programming the simulation model in Python uisng "SimPy" library. This involved implementing the logic and flow of events, considering the different activities, interarrival times, service times, and delays associated with each event. Once the simulation model was fully developed, we analyzed the output and performed sensitivity analysis to assess the system's performance under various scenarios.

<span>

<span style="font-family:Times New Roman; font-size:15pt;">
<h4><b>4. Phase3; Benchmarking and Sensitivity Analysis<b></h4>
<span>
<span style="font-family: Times New Roman; font-size: 13pt;">

During the final phase of our study, we were presented with two alternative systems aimed at replacing the incumbent one. Each of these systems underwent a series of modifications to enhance the overall performance of the center. In System 1, the parking lot section was entirely removed, and a fundamental assumption was made that all customers arrive in pairs. Furthermore, operating hours were adjusted to provide service round-the-clock, following an exponential distribution with a mean of 5. On the other hand, System 2 represented a revised version of System 1. Here, the mean arrival probability for customers was altered to 3.2, and the complaint section was relocated to a different area. Additionally, four new experts were hired for the Documentation sector, with their service times following a triangular distribution with parameters 6, 8, and 10. In the Fulfillment sector, the new experts' service times followed a triangular distribution with parameters 3, 3.5, and 4. Furthermore, a new Evaluation employee was recruited, and with appropriate training, the mean service time for experts in this section was reduced to 8. To address these requirements, the implementation of the new systems closely follows the approach utilized for the previous model.

<span>

  
<br>

  
You can find the results and step-by-step explanations for this project in the .pdf file. We've also included the code for each phase, along with complete documentation and line-by-line explanations for your further review.

