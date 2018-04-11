# Project-Management-System---PERT
A program that simulates a PERT system.
"""
Author of this program :
Reuven Kozel, 206281412

    Project Management System - Pert
    ---------------------------------------------
    The following program represents a Pert management system.
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
************************************************************************************************************************

   
|**********************************************************************************************************************|
| <-------------------------------------------------PERT PATHS-------------------------------------------------------->|
|**********************************************************************************************************************|
|                                               Legend:                                                                |
|                                               -------                                                                |
| - (Node A)                                                    = A Node in the graph                                  |
| - <TASK>                                                      = An activity in the graph                             |
| - (Node A) -> <TASK> -> (Node B)                              = Transition from Node A to Node B with TASK           |
| - [A, B]                                                      = Earliest finish / Latest Finish                      |
| - <--->                                                       = The right node(s) must be finished with the left node|
| - (Node A)[0,0] -> <TASK> -> (Node B)[6,6] <---> {(Node C) }  = Transition with parallels                            |
|**********************************************************************************************************************|    

