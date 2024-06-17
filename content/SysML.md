### What is it?
* General purpose modelling language for systems engineering

### How it is helpful?
* SysML is helpful in visualizing the requirements of a product. It's short for _SYStems Modeling Language_
* Crucial for **Model driven development of [[Internet of Things (IoT)|IoT]] systems**
* Basis for model-based development of mechantronic PSS (Product Service Systems)
* A mandatory requirement in the US and UK defense industry

### Skeleton of SysML
**Requirements Diagram** - Identification of the requirements and the actors involved 
#### Relationships in Requirement Diagrams
* << **refine** >> - _Refinement_ = An element describes the properties of a request in more detail
* << **satisfy** >> - _Fulfilment_ = The relationship between the requirement and a model element that fulfills the requirement (_client (satisfying)_ ---> _supplier (satisfied)_)
* << **verify** >> - _Test_ = Fulfilment of the request can be verified by the linked test case
* << **deriveReqt** >> - _Derivation_ = One request is derived from the other

**Sequence Diagram** - Messages b/w comm. partners (<-->)

**Block Def. Diagram & Internal Block Diagram** - Description of class structure and internals (the skeleton)

**Activity Diagram** - How would the *mechanical engineer* describe the behaviour of the system?

**State Diagram** - How would the *computer scientist* describe the system behaviour?
