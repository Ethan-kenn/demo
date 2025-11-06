
# write sample 


![System Design Cheatsheet](https://via.placeholder.com/800x200.png?text=System+Design+Cheatsheet)

# System Design Cheatsheet  
**Picking the right architecture = Picking the right battles + Managing trade-offs**

## Basic Steps  
- Clarify and agree on the scope of the system  
- User cases (description of sequences of events that, taken together, lead to a system doing something useful)  
  - Who is going to use it?  
  - How are they going to use it?  
- Constraints:  
  - Mainly identify traffic and data-handling constraints at scale.  
  - Scale of the system such as requests per second, request types, data written per second, data read per second.  
  - Special system requirements such as multi-threading, read- or write-oriented.  
- High level architecture design (Abstract design)  
  - Sketch the important components and connections between them, but don’t go into detail.  
  - Application service layer (serves the requests)  
    - List different services required.  
  - Data Storage layer:
 
    
    - e.g., usually a scalable system includes webserver (load balancer), service (service partition), database (master/slave cluster) and caching systems.  
- Component Design:  
  - Component + specific APIs required for each of them.  
  - Object oriented design for functionalities.  
  - Map features to modules: “One scenario → one module.”
  -  <img width="332" height="328" alt="EEEE" src="https://github.com/user-attachments/assets/8d3eafa8-b5a9-431d-877a-78916e82e855" />

  - Consider relationships among modules:  
    - Certain functions must have unique instance (Singletons)  
    - Core object can be made up of many other objects (composition)  
    - One object is another object (inheritance)
   
      ![capte](https://github.com/user-attachments/assets/16ff091a-7986-4363-9ffe-093f49083532)

  - Database schema design.  
- Understanding Bottlenecks:  
  - Perhaps your system needs a load balancer and many machines behind it to handle user requests; or maybe the data is so huge that you need to distribute your DB. What are the downsides?  
  - Is the database too slow and does it need some in-memory caching?  
- Scaling your abstract design:  
  - Vertical scaling — you scale by adding more power (CPU, RAM) to your existing machine.  

