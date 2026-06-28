This project demonstrates how a  stable circular orbit emerges from Newton’s law of gravitation by numerically simulating the motion of a planet around a central mass


According to Newton’s law of gravitation, all masses attract each other through gravitational force. The greater the mass of an object, the stronger gravitational field it produces around it, g = GM/R²


It may seem that planets should fall in the Sun or moon should fall in the Earth due to gravitational force, but what's stopping it is the planet's sideways velocity.


How they got the velocity lies in their history. Both stars and planets form from giant clouds of gas and dust(nebula). If enough mass gathers for hydrogen fusion, star forms and from surrounding remains, planets form.


Anyways, nothing in the universe is still. All the particles of the gas clouds have some tiny random motion from thermal energy and turbulence. When these are summed up, the net angular momentum is small but not zero. Angular momentum is conserved as there is nothing to provide external Torque or even friction to take away energy. Angular momentum, vec.L = vec.r × m × vec.v (I wish I could put the vector symbols 💀), where 'r' means the distance from the axis of rotation (or center of mass).


So what happens with the velocity after stars and planets form?


Every particle in the cloud has a 'v'. From the center it has a distance 'r'. When collapses, the distance from the center to the particle or 'r' decreases. But to keep angular momentum, vec.L = vec.r × m × vec.v (or simply L = mvr) conserved, the 'v' increases.


Now since it has sideways velocity (inertia), even if the star pulls the planet bending its direction it is moving forward so the planet keeps missing the star and remains in orbit



Calculations/ Math tools/ Formulas used here – 

1. v = u + at (where due to rotation the 'direction' is constantly changing each time interval NOT the magnitude. I used t = 0.001 s, meaning it determines velocity at every 0.001 s).

2. s = s + vt (instantaneous)

3. GM, r(1.0,0.0) [Let's say that the distance is 1 AU from the Sun to the planet]. For the planet to orbit, GMm/r² = mv²/r or, GM/r = v² or, GM = 4pi² [ v = 2.pi.r/T, T = 1 year, r = 1 AU]

4. Initial velocity (whose 'magnitude' remains constant), v² = GM (From the above equation) or, v = 2pi.

5. acceleration (largest one 💀), all our vectors were like pointing from the Sun to the planet so when r is (1.0,0.0) it means planet is 1.0 unit from the Sun. There will be a minus sign before the acceleration since it is pointing towards the Sun.                                     F = GMm/r² or, ma = GMm/r² or, a = GM/r² [But this represents the number only, we need the vector. vec.r/r is the unit vector of the distance because it only represents the direction without changing the value. So, a = - GM × vec.r/ r³. Since direction of 'r' is constantly changing, we cannot simply put a minus before GM/r², but as acceleration is opposite to 'r' no matter what, we put minus before GM × vec.r/ r³. Therefore, a = - GM × vec.r/ r³, in the denominator 'r' is scalar which has been calculated in the code as "dist = np.linalg.norm(r). In my code, a = - GM*r/dist**3.


What I learned:

By doing the calculations and coding, I learnt how velocity and position matters and understood the use of GMm/R² = mv²/R more. Here in the formula we find the relationship between velocity and position by equating the gravitational force acting as centripetal force balancing with imaginary centrifugal force. If velocity or position doesn't make the equation true, the planet can't remain in a stable orbit. I realized it by putting different values for velocity and position and forgetting to recalculate the other values! That means I only knew the equation but not the true meaning!

