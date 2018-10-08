# A Flexible and Portable Approach for Communication in Distributed Computing Systems

Latex sources of my diploma thesis from december 2014

## Introduction
The domain of high performance computing is subject to constant develop-
ment.
The main focus of this development is the increase of computing
power [ref:performance_development]. More computing power enables high
performance applications to solve more complex problems or allows for an increase of
the problem size. Current state of the art computing systems reached the area of one
petaflop, that are 10 to the power of 15 floating point operations per second (petaflop/s), in the year
2008 [ref:ibm_roadrunner]. But only a small number of applications worldwide have
taken advantage of these so called petascale systems.
One application that has shown scalability on petascale systems, is PIConGPU
[ref:picongpu_scale]. It is a particle in cell physics simulation that was running
on the Titan supercomputer at the Oak Ridge National Laboratory in the United
States [ref:titan], reaching 7.1 petaflop/s peak performance by utilizing 18.000 Graphics
Processing Units (GPUs). However, applications capable of fully utilizing a petascale
system can often be expected to desire systems with even more computational power.
Therefore, current computing systems will no longer adequately cover the future needs
of complex, computation intensive scientific and industrial applications. To provide more
computing power to these applications, a rapid progress in the development of computers
and algorithms is necessary. The next milestone in the development of supercomputers
are exascale systems, capable of at least one exaflop/s, which represents a thousandfold
increase over the first petascale system.

On the one hand, not all questions about the construction of such a system are
solved. On the other hand, it is certain that exascale will increase the amount and
complexity of computers to a new level [ref:cresta], amplifying the challenge of reliability,
programmability and usability of such systems.

Considering an exascale system, it is not sufficient to simply port the applications
previously running on petascale systems. The sole, massive increase in size of the
computing system will lead to a decrease in the mean time to failure (MTTF) and
an increased importance of data locality. Furthermore, the emergence of accelerator
hardware leads to computing systems that are more heterogeneous and hierarchical, as
well as increasingly complex to program and use [ref:accel]. Therefore, applications
running on high performance computers have to be adapted to utilize the upcoming
generation of supercomputers. Current applications lack techniques that form the basis
for load balancing and fault tolerance. Thus, there is a need for a smart description
concept for high performance applications that models upcoming exascale computing
systems with respect to these techniques.

Many applications exploit the parallel power of clusters by interconnecting their parallel
entities via network. These applications can be enhanced by a smart communication
approach. This approach will enhance already existing communication libraries by a
1further layer, which is necessary for the upcoming supercomputers. This additional
layer is separated into three components: an abstract communication layer, a model
of the communication topology, and a mapping from the topology onto the abstract
communication layer. These mappings can be changed at any time during the application
execution. In connection with the exchangeable communication library, it forms a flexible
and portable communication approach for the upcoming supercomputer generation. A
prototype, that combines these three components in a single system, was implemented and
deployed in simulation applications. The message passing interface (MPI) was used within
this prototype as communication back-end underneath the communication abstraction
layer. It maps common communication processes onto equivalent MPI methods.
The following Chapter 2 first motivates the design of the system and subsequently
provides a discussion about of the system components. Selected implementation details
of the system is presented in Chapter 3. The developed prototype is evaluated and
compared in contrast to an MPI implementation in Chapter 4. Chapter 5 provides ideas
to enhance the system in future work. Finally, Chapter 6 summarizes the developed
system and Chapter 7 provides an outlook for future development.

#  Dependencies
* latex
* biber
* make

# Compile
```
cd thesis
make
```
