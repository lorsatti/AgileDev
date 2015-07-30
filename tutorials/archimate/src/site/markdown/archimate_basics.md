# ArchiMate basics


## Core elements

### Business Layer

|Symbol|Name|Explanation|
|----|------|-----------|
|![Business Actor](images/business_actor.png)|Business Actor|A business actor performs the behavior assigned to (one or more) business roles. A business actor is an organizational entity and may include entities outside the actual enterprise; e.g., customers and partners. Examples of business actors are humans, departments, and business units. A business actor may be assigned to one or more business roles. The name of a business actor should preferably be a noun.|
|![Business Role](images/business_role.png)|Business Role|A business role is defined as the responsibility for performing specific behavior, to which an actor can be assigned. Business processes or business functions are assigned to a single business role with certain responsibilities or skills. A business actor that is assigned to a business role ultimately performs the corresponding behavior. A business role may be assigned to one or more business processes or business functions, while a business actor may be assigned to a business role. A business interface or an application interface may be used by a business role, while a business interface may be part of a business role (through a composition relationship, which is not shown explicitly in the interface notation). The name of a business role should preferably be a noun.|
|![Business Collaboration](images/business_collaboration.png)|Business Collaboration|An aggregate of two or more business roles that work together to perform collective behavior. Business interactions are used to describe the internal behavior that takes place within business collaboration. The name of a business collaboration should be a noun. It is also common to leave a collaboration unnamed.|
|![Business Interface](images/business_interface.png)|Business Interface|A point of access where a business service is made available to the environment. You can think of it as a channel; e.g., phone, mail, meeting, etc. A business interface exposes the functionality of a business service to other business roles, or expects functionality from other business services. The name of a business interface should be a noun.|
|![Business Process](images/business_process.png)|Business Process|A behavior element that groups behavior based on an ordering of activities. It is intended to produce a defined set of products or business services. A business process describes the internal behavior performed by a business role that is required to produce a set of products and services. The name of a business process should preferably be a verb in the simple present tense; e.g., “handle claim”.|
|![Business Function](images/business_function.png)|Business Function|A behavior element that groups behavior based on a chosen set of criteria (typically required business resources and/or competences). A business function typically groups behavior based on required business resources, skills, competences, knowledge, etc. The name of a business function should preferably be a verb ending with “-ing”; e.g., “claims processing”, or a noun ending in “- ion” or “-ment”; e.g., “administration”.|
|![Business Interaction](images/business_interaction.png)|Business Interaction|A behavior element that describes the behavior of a business collaboration. A business interaction is similar to a business process/function, but while a process/function may be performed by a single role, an interaction is performed by a collaboration of multiple roles. The roles in the collaboration share the responsibility for performing the interaction. he name of a business interaction should preferably be a verb in the simple present tense.|
|![Business Event](images/business_event.png)|Business Event|Something that happens (internally or externally) and influences behavior. Business processes and other business behavior may be triggered or interrupted by a business event. Also, business processes may raise events that trigger other business processes, functions, or interactions. The name of a business event should be a verb in the perfect tense; for example, "claim received".|
|![Business Service](images/business_service.png)|Business Service|A service that fulfills a business need for a customer (internal or external to the organization). A business service exposes the functionality of business roles or collaborations to their environment. The name of a business service should be a verb ending with "-ing"; for example "transaction processing".|
|![Business Object](images/business_object.png)|Business Object|Business objects represent the important “informational” or “conceptual” elements in which the business thinks about a domain. Business objects are passive in the sense that they do not trigger or perform processes. The name of a business object should preferably be a noun.|
|![Representation](images/representation.png)|Representation|A perceptible form of the information carried by a business object. If relevant, representations can be classified in various ways; for example, in terms of medium (electronic, paper, audio, etc.) or format (HTML, ASCII, PDF, RTF, etc.). A single business object can have a number of different representations. Also, a single representation can realize one or more specific business objects. The name of a representation is preferably a noun.|
|![Meaning](images/meaning.png)|Meaning|The knowledge or expertise present in a business object or its representation, given a particular context. A meaning is the information-related counterpart of a value: it represents the intention of a business object or representation. It is a description that expresses the intent of a representation; i.e., how it informs the external user. The name of a meaning should preferably be a noun or noun phrase.|
|![Value](images/value.png)|Value|The relative worth, utility, or importance of a business service or product. Value may apply to what a party gets by selling or making available some product or service, or it may apply to what a party gets by buying or obtaining access to it. Although the name of a value can be expressed in many different ways (including amounts, objects), where the “functional” value of a service is concerned it is recommended to try and express it as an action or state that can be performed or reached as a result of the corresponding service being available.|
|![Product](images/product.png)|Product|A coherent collection of services, accompanied by a contract/set of agreements, which is offered as a whole to (internal or external) customers. The name of a product is usually the name which is used in the communication with customers, or possibly a more generic noun.|
|![Contract](images/contract.png)|Contract|A formal or informal specification of an agreement that specifies the rights and obligations associated with a product. The contract concept may be used to model a contract in the legal sense, but also a more informal agreement associated with a product. It may also be or include a Service Level Agreement (SLA), describing an agreement about the functionality and quality of the services that are part of a product. A contract is a specialization of a business object. The name of a contract is preferably a noun.|

### Application Layer

|Symbol|Name|Explanation|
|------|----|-----------|
|![Application Component](images/application_component.png)|Application Component|An application component is a modular, deployable, and replaceable part of a software system that encapsulates its behavior and data and exposes these through a set of interfaces. The name of an application component should be preferably be a noun.|
|![Application Collaboration](images/application_collaboration.png)|Application Collaboration|An application collaboration specifies which components co-operate to perform some task.|
|![Application Interface](images/application_interface.png)|Application Interface|An application interface specifies how the functionality of a component can be accessed by other components (provided interface), or which functionality the component requires from its environment (required interface). The same application service may be exposes through different interfaces.|
|![Application Function](images/application_function.png)|Application Function|An application function describes the internal behavior of an application component.|
|![Application Interaction](images/application_interaction.png)|Application Interaction|A behavioral element that describes the behavior of an application collaboration|
|![Application Service](images/application_service.png)|Application Service|An application service exposes the functionality of components to their environment. This functionality is accessed through one or more application interfaces. An application service is realized by one or more application functions that are performed by the component.|
|![Data Object](images/data_object.png)|Data Object|An data object is a passive element suitable for automated processing. Application function operates on a data object. It may be communicated via interactions and used or produced by application services. It should be a self contained piece of information which a clear meaning to the business and not just to the application level.|

### Technology Layer

|Symbol|Name|Explanation|
|------|----|-----------|
|![Node](images/node.png)|Node|A computational resource upon which artifacts may be stored or deployed for execution. A node is often a combination of a hardware device and system software, thus providing a complete execution environment.|
|![Device](images/device.png)|Device|A hardware resource upon which artifacts may be stored or deployed for execution. Devices can be interconnected by networks and artifacts can be assigned to (i.e. deployed on) devices. A node can contain one or more devices|
|![System software](images/system_software.png)|System Software|Used to model the software environment in which artifact run. This can be, for example, an operating system, a application server, a database system, etc. Usually system software is combined with a device to form a general node.|
|![Infrastructure Interface](images/infrastructure_interface.png)|Infrastructure Interface|A point of access where infrastructure services offered by  node can be accessed by other nodes and application components.|
|![Network](images/network.png)|Network|Represents the physical communication mediium between 2 or more devices. A network has properties such as bandwidth and latency.|
|![Communication Path](images/communication_path.png)|Communication Path|A communication path is used to model the logical link between 2 nodes and via which nodes can exchange data. It is realized by one or more networks, which represent the physical communication links.|
|![Infrastructure Function](images/infrastructure_function.png)|Infrastructure Function|An infrastructure function describes the internal behavior of a node. If the behavior is exposed externally. this is done through one or more infrastructure services.|
|![Infrastructure Service](images/infrastructure_service.png)|Infrastructure Service|An infrastructure service exposes the functionality on a node to ites environment. This functionality is accessed through one or more infrastructure interfaces. Typical infrastructure services may include messaging, storage, naming, and directory services.|
|![Artifact](images/artifact/png)|Artifact|A physical piece of data that is used or produced in a software development process, or by deployment of a system. It is typically used to model (software) products such as source files, executable, scripts, database tables, documents, specifications, etc. An instance of an artifact can be deployed on a node.|

### Relations.

|Symbol|Name|Explanation|
|------|----|-----------|
|![Composite Relationship](images/composite.png)|Composite|Indicates that an object is composed of one ore more other objects. In contrast to the aggregate relationship, an object can be part of only one composition.|
|![Aggregate Relationship](images/aggregate.png)|Aggregate|Indicates that a concept groups a number of other concepts. In contrast to the composition relationship, an object can be part of more than one aggregation.|
|![Assignment Relationship](images/assignment.png)|Assignment|Link active elements such as business roles and application components, with units of behavior that are performed by them, (for example an application component with an application function.|
|![Realization Relationship](images/realization.png)|Realization|Indicates how logical entities, such as services, are realized by means of more concrete entities, (e.g., a process/function realizes a service).|
|![Used By Relationship](images/used-by.png)|Used By|Models the use of services by processes, functions, or interactions and the access to interfaces by roles, components or collaborations.|
|![Access Relationship](images/access.png)|Access|Indicates that a process, function, interaction, service or event 'does something' with a business or data object; e.g., create a new object, read data from the object, write or modify the object data, or delete the object. The arrow head, if present, indicatees the direction of the flow of information.|
|![Association Relationship](images/association.png)|Association|Models a relationship between objects that is not covered by another, more specific relationship.|
|![Triggering Relationship](images/triggering.png)|Triggering|Used to model the causal relationships between behavior concepts in a process.|
|![Flow Relationship](images/flow.png)|Flow|Describes the exchange or transfer of information or values between processes, functions, interactions and events.|
|![Grouping](images/grouping.png)|Grouping|The grouping relationship is used to group an arbitrary group of model objects, which can be of the same type or of different types.|
|![Junction](images/junction.png)|Junction|A junction is used to connect dynamic (trigger or flow) relationships of the same type; e.g., to indicate splits or joins.|
|![Specialization Relationship](images/specialization.png)|Specialization|Indicates that an object is a specialization of another object. Specialization is always possible between two instances of the same concept.|
|