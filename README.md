# Final 1
Josh Pelton
Dennis Scheglov


Given a formula to compute Pi as the perimeter of an n-sided polygon, the goal of this project was to minimize error by reworking the formula. Extreme precision loss occurs because of how floating point numbers work. Precision gets denser the closer one gets to zero, and also runs into errors when the numerator contains subtraction. The formula, sqrt((1-(sqrt(1-sin(a)^2)))/2), starts with sqrt(1-b), where b = sqrt(1-sin(a)^2). As we take very small angles (as is the case with the angle between sides of an almost circle), sin(a)^2 goes to zero, so b is very close to 1. Both 1 and b have precisions acceptable for values near 1, but nowhere near acceptable for values closer to zero. So when we take 1-b and get a small number close to zero, that unacceptable precision moves down the line to zero. For small indices (for larger angles) this effect isn't noticeable, but it begins to emerge as the angles approach zero. This is the reason for the drastic deviation in precision.
