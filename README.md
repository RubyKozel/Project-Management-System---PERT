
Author of this program :
Ruby Kozel

    Project Management System - PERT
    ---------------------------------------------
    The following program represents a PERT management system.
    The pert itself is a graph, implemented as a dictionary.
    The graph is constructed from 3 vital parts:

        * Node       -  The actual circle which holds the information about the early and late finishes,
                        as well as the slack time (if there are any).
                        A node has a unique number which identifies it.
                        Each node can posses parallel nodes that the pert has to be reached to at
                        the same time, meaning those nodes are bounded to the main node.

        * Activity   -  The task and its duration.
                        Each task has its own unique description.

        * Transition -  Represents the transition from Node to Node via an Activity.
                        A transition is unique by its own existence.
                        There can't be a transition that travels from the same nodes with different
                        activities, therefore each transition has two nodes and one activity that
                        are unique.

    Therefore, the graph keys are nodes and its values are transitions.
    For your convenience, i added a detailed printing function to the pert so you'll understand
    the implementation of each class to the whole system.
    Below is a legend for the PERT paths in the output
    
    Have fun!
