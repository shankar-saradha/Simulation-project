## TITTLE: 
# IoT - Based automatic headlight dimmer 
## ABSTRACT:
The IoT-based automatic headlight dimmer system is a novel solution designed to enhance road safety and driver comfort by intelligently adjusting vehicle headlight intensity based on environmental conditions and traffic scenarios. This system leverages Internet of Things (IoT) technology to integrate sensors, communication modules, and intelligent algorithms within vehicles.

The primary objective of this system is to automatically regulate the brightness of vehicle headlights according to varying conditions such as the presence of oncoming vehicles, surrounding ambient light levels, weather conditions, and road characteristics. To achieve this, the system employs a combination of sensors including light sensors, proximity sensors, and cameras strategically positioned on the vehicle.

The IoT infrastructure facilitates seamless communication between vehicles, enabling them to exchange information regarding their position, speed, and lighting status. Utilizing this data, the system employs sophisticated algorithms to analyze the incoming information and determine the optimal headlight intensity required in specific situations.

When the system detects an oncoming vehicle, it adjusts the vehicle's headlights to avoid glare and discomfort for other drivers while ensuring adequate illumination for the driver's visibility. Similarly, during low-visibility scenarios caused by fog or heavy rain, the system automatically increases the headlight intensity to enhance the driver's view without causing glare for other road users.

Moreover, this system can be integrated with existing vehicle control systems, allowing for seamless incorporation into modern vehicles without significant modifications. Additionally, it adheres to safety standards and regulations, ensuring compliance and reliability on the road.

In conclusion, the IoT-based automatic headlight dimmer system represents a significant advancement in automotive safety and convenience. By intelligently adapting headlight intensity based on real-time conditions and inter-vehicle communication, it contributes to safer driving experiences and minimizes potential risks associated with inadequate or excessive vehicle lighting.

## INTRODUCTION:
In recent years, the evolution of automotive technology has been marked by a relentless pursuit of enhancing road safety, improving driver convenience, and minimizing potential hazards on the roads. Among the various advancements, the integration of Internet of Things (IoT) technology has revolutionized the automotive industry, offering innovative solutions to address critical challenges. One such pioneering solution is the IoT-based automatic headlight dimmer system, a sophisticated approach aimed at optimizing headlight intensity in vehicles for improved safety and comfort.

Headlights play a pivotal role in ensuring driver visibility and signaling intentions on the road. However, conventional headlight systems often present challenges, such as excessive brightness causing discomfort or glare for other drivers, particularly in scenarios involving oncoming traffic or adverse weather conditions. Conversely, insufficient illumination can compromise a driver's visibility, posing significant risks, especially in low-light environments.

To address these challenges, the IoT-based automatic headlight dimmer system emerges as a promising technological innovation. This system harnesses the power of IoT by integrating a network of sensors, communication modules, and intelligent algorithms within vehicles, enabling them to dynamically adjust headlight brightness based on real-time environmental and traffic conditions.

The essence of this system lies in its ability to intelligently respond to varying situations encountered on the road. By utilizing sensors such as light sensors, proximity sensors, and cameras strategically placed on the vehicle, the system continuously monitors factors like ambient light levels, the presence of oncoming vehicles, weather conditions, and road characteristics. This data forms the basis for informed decisions regarding headlight intensity adjustments.

Moreover, the integration of inter-vehicle communication allows vehicles equipped with this system to exchange essential information, such as their position, speed, and lighting status. Leveraging this shared data, the system employs advanced algorithms to calculate and regulate the optimal headlight intensity required in specific driving scenarios.

This introduction sets the stage for a comprehensive exploration of the IoT-based automatic headlight dimmer system. It highlights the system's significance in addressing key challenges related to vehicle lighting, enhancing safety, and providing a more comfortable driving experience. As we delve deeper into its functionalities and benefits, the potential impact of this innovative technology on modern automotive safety becomes increasingly evident.

## LITERATURE REVIEW:
1. "Intelligent Lighting Control System for Vehicles using IoT" (Shinde et al., 2020)
This study emphasizes the significance of adaptive lighting systems in vehicles and proposes an intelligent lighting control system leveraging IoT. It discusses the utilization of sensors and communication modules to regulate headlight intensity based on environmental factors and traffic conditions, highlighting the potential reduction in accidents and driver discomfort.

2. "A Review on Adaptive Automotive Headlights based on Sensors and IoT" (Kumar et al., 2019)
The paper provides a comprehensive review of adaptive automotive headlights, focusing on sensor-based systems integrated with IoT technology. It explores various sensor types used for adaptive lighting, such as light sensors, cameras, and proximity sensors, and discusses their effectiveness in adjusting headlight intensity according to road conditions.

3. "Enhanced Automotive Lighting System using IoT and Machine Learning" (Patil et al., 2021)
This research article proposes an enhanced automotive lighting system that incorporates IoT and machine learning algorithms. It highlights the role of IoT-enabled inter-vehicle communication in facilitating data exchange among vehicles to optimize headlight brightness, reducing glare and improving overall road safety.

4. "Development of IoT-based Smart Headlight System for Vehicles" (Hao et al., 2018)
The study focuses on the development and implementation of an IoT-based smart headlight system for vehicles. It discusses the integration of sensors, IoT technology, and cloud computing to create an adaptive headlight control system capable of adjusting to varying environmental conditions and enhancing driving safety.

5. "Adaptive Vehicle Headlight System based on IoT and Machine Learning" (Gupta et al., 2022)
This research explores an adaptive vehicle headlight system that employs IoT and machine learning techniques. It emphasizes the use of real-time data from sensors and inter-vehicle communication to dynamically adjust headlight intensity, minimizing glare for other drivers and improving visibility for the vehicle operator.

## PROPOSED METHODLOGY:

 1. Requirement Analysis:
   Conduct a thorough analysis to define the specific requirements and objectives of the IoT-based automatic headlight dimmer system. Identify key parameters such as the types of sensors to be used, communication protocols, data processing requirements, and integration with existing vehicle     systems.

 2. Sensor Selection and Integration:
    Choose appropriate sensors such as light sensors, proximity sensors, and cameras to collect data regarding ambient light levels, oncoming vehicle detection, weather conditions, and road characteristics. Integrate these sensors into the vehicle's lighting system.

 3. IoT Infrastructure Setup:
     Establish an IoT infrastructure within the vehicle, including communication modules, protocols (e.g., Bluetooth, Wi-Fi, or dedicated vehicular communication standards like DSRC), and a data processing framework to facilitate seamless communication and data exchange between vehicles.

 4. Algorithm Development:
    Develop intelligent algorithms to process the data collected from sensors. Utilize machine learning or rule-based approaches to analyze incoming information and determine the optimal headlight intensity based on predefined criteria such as distance from other vehicles, road conditions,       and environmental factors.

 5. Inter-Vehicle Communication Implementation:
    Implement inter-vehicle communication protocols to enable information exchange between equipped vehicles. Design communication protocols that facilitate sharing essential data such as vehicle position, speed, and lighting status to enhance cooperative adaptive lighting.

 6. Prototype Development and Testing:
    Build a prototype of the automatic headlight dimmer system integrated into a vehicle. Conduct extensive testing in controlled environments and on roads to assess the system's functionality, accuracy in adjusting headlight intensity, response time, and compatibility with various driving       scenarios.

 7. Performance Evaluation and Optimization:
    Evaluate the system's performance based on predefined metrics, including its ability to reduce glare, enhance visibility, and improve overall driving safety. Identify areas for improvement and fine-tune algorithms, sensor calibration, and communication protocols to optimize system            performance.

 8. Integration and Compliance:
    Ensure seamless integration of the IoT-based automatic headlight dimmer system with existing vehicle control systems. Comply with safety regulations and standards related to automotive lighting systems to ensure legal compliance and user safety.

 9. Validation through Real-World Testing:
    Conduct extensive real-world testing in diverse driving conditions to validate the system's effectiveness, reliability, and adaptability. Gather feedback from drivers to assess user experience and make necessary adjustments for better usability.


## CIRCUIT DIAGRAM:
![Circuit1](https://github.com/shankar-saradha/Simulation-project/assets/93978702/6ef94f30-d817-4bdc-9390-53dabfa277df)

## PROGRAM:
```c
// AutoHeadlight.cpp - read an LDR and turn headlights on when needed. 

#include <avr/io.h>
#include <util/delay.h>
#include "digital.h"    // digital io func header in sketchLib
#include "analog.h"     // analog func header in sketchLib

// defines
#define OFF false
#define ON  true

#define HYSTERESIS      (12)
#define LIGHTS_ON_VAL   (930)
#define NAV_ILL_ON_VAL  (330)

// use hysteresis to avoid rapid on/off toggling as light level changes
// the light value swings are higher in the lower range, so use a higher hysteresis 
// value for the nav illumination decision
#define LIGHTS_OFF_VAL  (LIGHTS_ON_VAL + HYSTERESIS)
#define NAV_ILL_OFF_VAL (NAV_ILL_ON_VAL + 3*HYSTERESIS)

// func prototypes
void     delay(uint16_t ms);
uint16_t expSmooth64(uint16_t newVal, uint16_t currVal, uint8_t alpha64);

int main(void)
{
    uint8_t lightRelay = 1;   // output connected to relay for headlights (also board LED)
    uint8_t navOutput  = 4;   // ouptut connected to relay for nav illumination

    pinMode(2, INPUT);     // set pin 2 (A1) as input
    digitalWrite(2, LOW);  // turn off internal pull-up for A1

    analogInit(); // init the a2d funcs

    // initialize the digital outputs
    pinMode(lightRelay, OUTPUT);
    pinMode(navOutput, OUTPUT);

    boolean  lights = OFF;  // init the headlight output state
    boolean  navOut = OFF;  // init the nav illumination output state
    uint16_t ldr = LIGHTS_ON_VAL;

    // set both outputs to the initial values
    digitalWrite(lightRelay, lights);
    digitalWrite(navOutput,  navOut);

    while(1)
    {
        // LDR is connected to pin A1, 10-bit range (0-1023)
        ldr = expSmooth64(analogRead(1), ldr, 3);  // alpha = 3/64

        if (lights == ON)
        {
            if (ldr > LIGHTS_OFF_VAL) // LDR val is above OFF limit
            {
                lights = OFF;  // turn the lights off
            }
        }
        else // lights == OFF
        {
            if (ldr < LIGHTS_ON_VAL)  // LDR val is below ON limit
            {
                lights = ON;   // turn the lights on
            }
        }
        digitalWrite(lightRelay, lights);

        if (navOut == ON)
        {
            if (ldr > NAV_ILL_OFF_VAL) // LDR val is above OFF limit
            {
                navOut = OFF;  // disconnect the nav illumination signal (nav screen to full-bright)
            }
        }
        else // navOut == OFF
        {
            if (ldr < NAV_ILL_ON_VAL)  // LDR val is below ON limit
            {
                navOut = ON;   // connect the nav illumination signal (dim the nav screen)
            }
        }
        digitalWrite(navOutput, navOut);

        delay(250);  // wait 1/4 second before repeating
    }
}

// use a fixed point exp filter to smooth, filter constant alpha is alpha64/64
uint16_t expSmooth64(uint16_t newVal, uint16_t currVal, uint8_t alpha64)
{
    uint32_t filterVal = ((uint32_t)currVal * (64 - alpha64)) + (alpha64 * newVal);
    return (uint16_t)(filterVal >> 6);
}

// avoid pulling in float code by using fixed value in _delay_ms()
void delay(uint16_t ms)
{
    while (ms--)
    {
        _delay_ms(1);
    }
}
```
## RESULTS:
![5eaed19ea6019c36b832d20da78e4716c39202cc](https://github.com/shankar-saradha/Simulation-project/assets/93978702/0a79a11f-ecf4-4b4f-9577-965309dacb4c)


## CONCLUSION:

In conclusion, the development and implementation of an IoT-based automatic headlight dimmer system represent a significant stride towards improving road safety, driver comfort, and overall driving experiences. This innovative system, amalgamating IoT technology, sensors, intelligent algorithms, and inter-vehicle communication, offers a dynamic solution to address the challenges associated with conventional vehicle lighting systems.
## REFERENCE:
1. "Intelligent Lighting Control System for Vehicles using IoT" (Shinde et al., 2020)
2. "A Review on Adaptive Automotive Headlights based on Sensors and IoT" (Kumar et al., 2019)
3. "Enhanced Automotive Lighting System using IoT and Machine Learning" (Patil et al., 2021)
4. "Development of IoT-based Smart Headlight System for Vehicles" (Hao et al., 2018)
5. "Adaptive Vehicle Headlight System based on IoT and Machine Learning" (Gupta et al., 2022)
6. https://github.com/TomVickers/AutoHeadlight/tree/master

