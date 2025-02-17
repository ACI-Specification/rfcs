# ACI Registries

## Summary

The ACI Specification Project is to maintain several registries, which are both machine and human readable, which contain important information 

## Motivation

Certain information that is outside of the technical bounds of the ACI Specification, but are related to it, needs agreement among users of the specification (device implementors, tooling authors, and system software). It is therefore necessary to maintain a list of how this information is assigned and made use of.

## Informative Explanation

Certain important information is maintained in a central list by the ACI Specification Project, to allow agreement of this information between consumers of the ACI Specification.
This may include class and vendor ids used for identifying ACI devices, and subclasses of "Well Known" classes. 

Each registration is assigned a machine-usable identifier that can easily searched or translated into an identifier in various programming languages. Such identifiers can be reassigned and deprecated, but not removed entirely from the registry.

Typically, registrations will be assigned a number value, which is similarly stable and won't ever be reused or removed from the registry once assigned.

## Normative Text

### Registries

The ACI Specification Project shall maintain a series of registries, to record important information for both machine and human users. The Registries are split into Primary Registries and Secondary Registries.

The information recorded in each registry depend on the registry, but each registration shall, regardless of registry include the following information:
* The stable machine-usable identifier for the registration,
* The human readable public name of the registration,
* The date on which the registration was issued, and
* The name and contact of the registrar that issued the registration.
    * Where the registration was issued by RFC, the name shall be "ACI Project Registrar Secretary" and the contact shall be the canonical contact address for the registrar Secretary.

Each Secondary Registry shall additionally be associated with a registration in a primary registry. Primary Registries can be created only by RFC. Whether or not the creation of a Secondary Registry requires an RFC depends on the RFC that created the associated Primary Registry. 

### Registries Format

The Registries shall be collated into a git repository by the Registrar Secretary. 

The following paths shall be made available via the git repository:
* `<name>.csv`: The Primary Registry with name `name`, in csv format,
* `deprecated/<name>.csv`: The Deprecated list for the Primary Registry with name `name`, in csv format,
* `<name>/<secondary>.csv`: The Secondary Registry `secondary` belonging to the Primary Registry `name`, in csv format,
* `deprecated/<name>/<secondary>.csv`: The Deprecated list for the Secondary Registry `secondary` belonging to the Primary Registry `name`, in csv format.

The default branch of the git repository published by the ACI Project shall contain the most up to date version of the registry at the time it is pulled.

### Registrars

The Clever-ISA Project and Lightning Creations shall be deemed the registrars of the ACI Registries. 
As appropriate, the Core Interest Groups of these two registrars shall have authority to make registrations on the behalf of the registrars, 
where such registrations are not deemed to require an RFC. Primary registries are divided between these groups, appropriately, unless explicitly assigned by RFC.

Each Registrar may set their own policies for issuing registrations, and such policies are not subject to the RFC Process. 

### Registrar Secretary

The Core Interest Groups shall together appoint a Registrar Secretary to manage the registries. 

The Registrar Secretary shall perform the following tasks:
* Apply changes to Primary and Secondary Registries as authorized by RFC or the Registrars,
* Maintain the Primary and Secondary Registries,
* Maintain and apply the Data Policy for the registries, and
* Maintain Deprecated/Reassignment lists for each Registry. 

### Deprecated/Reassignment Lists

Each Registry (Primary and Secondary) shall have an associated Deprecated/Reassignment list for renamed machine-usable identifiers. 

The Deprecated/Reassignment list shall specifiy the following:
* The previous (deprecated) identifier for the registration,
* The new identifier for the registration (if the registration was reassigned) - which shall be present in the associated registry,
* The date of the deprecation/reassignment,
* An optional reason for the deprecation/reassignment.

### Data Policy

The Registrar Secretary shall draft and adopt a policy for handling data recorded into the registry. The policy shall address:
* The right to control and protect personal data, and
* The necessity of keeping immutable records of certain parts of the registry.

The Registrar Secretary should consider Policies of similar organizations/registry processes when adopting the Data Policy.

### Copyright

Registries primarily contain a list of facts and are thus largely exempt from copyright. The Registrar Secretary shall provide the registries under the CC0 Public Domain Dedication as applied to any portion of the Registries that are not deemed purely factual.

## Security Considerations

Each Registry is released publicly and may contain some personal information. 
Both registrars and registrants should take care that such information is added to the registry. The Registrar Secretary shall take care that the nature of the information being included is disclosed to potential registrants in advance of a registration being authorized.

## Future Direction

* This leaves open the creation of the primary and secondary registries, the precise division of the primrary registries, and the "Well Known" Range. 
* The Data Policy could be made into an RFC and require an RFC to update in the future.