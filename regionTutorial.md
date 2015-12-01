#Commands:

/region create <name>                           Create a region
/region parent <child> <parent>                 Set the parent of a region
/region flag <name> <flag>                      Add a flag
/region addowner <region-name> <player-name>    Add an owner to the region
/region delowner <region-name> <player-name>    Remove an owner

A child of a parent will inherit all properties of the parent and can override them.

Let's say a parent has PVP on and no owner. while a child has one owner but pvp off. A child of the first child has no 
traits but a different region. The subchild has another owner

Another child of the parent has no owners special traits

Parent.         PVP on.
|_Child         One owner - player1, pvp off
  |_Subchild    player2
|_Child2        


  ==========================================
  |                                       |
  |        ---------------                |
  |        |     I       |                |    ==========
  |        |   child     |                |    | child2 |
  |        |     I       |                |    |        |
  |        |     I       |                |    ==========
  |        ------I-sub----                |
  |              I       I                |
  |              I       I                |
  |              I       I                |
  |              I_______I                |
  |                                       |
  =========================================

  PVP would be off in both Child and subchild because sub inherits the pvp off trait from child

  PVP would be on in both Parent and child2 because child2 inherits the trait from parent

  Player1 would be able to build in child1 and sub because sub inherits the ownership from child.

  Player2 would only be able to build in the sub region because it overrides the build protection of child inside its own area
  but not in the area only marked by child.


