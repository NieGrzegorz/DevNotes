## Characteristics and Atributtes 
Characteristic - group of attributes 
Attribute - information transferred between devices 

Characteristics organize and use attributes as data values, properties, and configuration inforamtion. 

Characteristic is composed of the following attributes: 
- Value 
- Declaration - descriptor storing properties. location and type of characteristics 
- Client characteristic configuration - allows the GATT server to configure the characteristic to be notified or indicated
- User description - ASCII string describing the characteristic 

Single attribute is associated with the following properties: 
- Handle - the index of the attribute in the table 
- Type - what the attribute data represents 
- Permissions - enforces if and how a GATT client device can access the value of an attribute

