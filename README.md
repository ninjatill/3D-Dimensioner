# 3D-Dimensioner
In short, the 3D Dimensioner (3DD) project is a set of infrared LASER rangefinders used to determine the exterior dimensions of a small package. The 3DD is designed for use at a shipping station in a business such as a warehouse. 

The 3DD project is an excercise in multiple "maker"/engineering disciplines such as electrical circuit design, printed circuit board (PCB) layout, surface mount device (SMD) soldering techniques, 3D computer aided drafting (CAD) and 3D printing. 

## Background
In the small parcel shipping world (think logistics companies such as FedEx, UPS, DHL, etc.) there is this concept called "dim weight". What is dim weight you ask? There's a good writeup on [Wikipedia - Dim Weight](https://en.wikipedia.org/wiki/Dimensional_weight) if you really want to get into it. What it really means to most companies shipping small parcels, is that in order to know how much it will cost to ship a package (at the time of shipping), you must record the dimensions and weight of the package. Without the dimensions, the shipping software can only quote on actual weight. But if you ship large but light packages, you will be paying on dim weight and not actual weight. UPS and FedEx both have automatic scanning systems that will record the dimensions as packages are sorted for delivery. Their billing system will automatically bill you the higher of the actual weight or the dim weight. So if you don't provide dimensions to the shipping software, you will think you are paying a lower price at time of shipping and then incurr "adjustments" (greater prices) when invoiced. To  distributors that means that a customer might not be charged enough for shipping which causes financial loss for the distributor.

Automatically recording weight is easy and cheap. UPS and FedEx will both provide a free shipping scale (as long as a company does business with them) that connects to a PC and automatically records the package weight in their shipping software. Recording dimensions is a bit more difficult and expensive. 

It is possible to automate dimension measurements but you need a "dimensioner". There are many companies that sell dimensioners but most are fairly large and require a dedicated space and workflow such as [Freight Snap](http://www.freightsnap.com/fs-parcel-product/). There are some "table-top" options such as the [Cubiscan 110](http://cubiscan.com/dimensioning/cubiscan-110/). Most likely, these examples cost thousands of dollars.

## 3DD Functional Description
The 3DD consists of three devices; the Master Control Unit (MCU), LASER Measurement Unit (LMU) and Origin Point Bracket (OPB). The MCU communicates with all the LMUs and has an LCD screen for displaying measurements and prompting the user. The MCU can also have a Remote Control Unit (RCU) which allows placement of the main button controls away from the MCU. The LMUs use an infrared LASER rangefinder to take measurements to the package surface. The OPB provides a fixed point in space to which the LMUs must be calibrated.

The 3DD uses three stationary LMUs to take measurements in the X, Y and Z planes. The package must be cubical and placed into a known origin point. The origin point reduces the number of simultaneous measurements requried to determine the package dimensions. If you reference the Cubiscan 110 above, you'll see that it takes four simultaneous measurements; two in the X plane and one in the Y and Z planes. The measurement bed and the backstop upright create a known origin point in two planes. The double measurements in the X plane allows loose X placement on the measurement bed. However, to get an accurate Y and Z measurement, the package must be placed touching the known origin point where the measurement bed and backstop upright meet. The 3DD operates similarly but uses a known origin point in three dimensions, which reduces the number of LMUs to three.

## Pros and Cons
|Feature|3DD|Cubiscan 110|
|---|---|---|
|Size|Can be scaled up to 8 meters or more due to 4m LASER rangefinders. Rangefinders are not permanently fixed and can be repositioned.|Limited to relatively small dimensions by the ultrasonic sensors. Also limited by permanently fixed and integrated sensor positions.|
|Size|Can be installed on an existing table top or workbench.|Small enough to fit on table top or workbench. Requires a dedicated space.|
|All-in-one|Only measures dimensions. Requires separate weight measuremnt|Measures both weight and dimensions.|
|Cost|Cheaper due to DIY nature of project.|Expensive|
|Engineering|Home-brewed solutions always have "rough edges".|Polished product worked on by a team of engineers (I assume).|
|Flexibility|Can be revised to measure pallets or work for any other project that needs measurements.|Does one thing and does it well. Cannot be repurposed.|



Pros:
The 3DD is small and can be mounted to table tops.
The LASER rangefinder measures up to 4 meters with a 2mm accuracy. Meaning, you could potentially measure very large packages.

Cons:
This is a DIY venture and so has all the shortcomings of the person who puts it together.
There can be variations in how the LMUs are mounted which could cause inaccuracy.

