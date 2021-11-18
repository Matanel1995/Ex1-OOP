# Ex1-OOP
Ex1 -Offline elevator algorithm

Literature:
  *	https://www.researchgate.net/publication/339806517_Traffic-based_floor_preference_for_the_scheduling_of_elevators_in_elevator_group_control_system
  * https://www.researchgate.net/publication/272591570_Elevator_Dispatching_Using_Heuristic_Search
  * https://www.researchgate.net/publication/343580574_Floor_Selection_Proposal_for_Automated_Travel_with_Smart_Elevator
  * https://www.youtube.com/watch?v=siqiJAJWUVg&t=1978s&ab_channel=ThinkSoftware

Offline algorithm vs online algorithm:
The benefit of an offline algorithm is that we have all the information we need at the beginning of the program, unlike online algorithm 
That mean we can take advantage of that because nothing can “surprise us”

Our algorithm:
  * If we have only 1 elevator, we will allocate all calls to this elevator
  * We iterate on all calls so we can allocate everything 
  * We iterate on all elevators
  * We are starting with allocating the first call to the first elevator and update those parameters:
      * Elevator flag (elevator direction Up Down or Level)
      * Elevator calls (Array with all the floors the elevator need to stop at)
      * Elevator timeline (Array with time at each cell, which indicate at what time this elevator will arrive to the cell(floor))
  * Then we iterate on UP calls or DOWN calls (depend on the elevator flag) 
      * We check if we can pick up the new call
      * We check we arrive to the new call source floor after the request time 
      * We check the call and the elevator heading the same direction 
      * We allocate every call that can be picked up
  * After an elevator finished all her calls 
      * We initialize the flag, the timeline array, and the calls arrays so we can use that elevator again 

Matanel Ohayon - 313231532
Roey Feingold - 313239477 
