# RCM

RCM (short for **R**e**C**overy **M**ode) is a mode for the switch that allows nintendo to send the switch commands to do various things. People found out that on unpatched switches, you could send a payload, and then quickly copy it into the memory buffer behind the stack, overflowing the memory buffer into the stack, meaning you smash the stack and get full access to everything on the system. We use it here to launch atmosphere.



[Continue to Entering RCM :material-arrow-right:](entering_rcm.md){ .md-button .md-button--primary }
