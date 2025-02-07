# RFC Policy

## Summary

The ACI Specification will be developed through a serious of documents, called "Requests for Comment" or "RFC"s, 
which will provide the basis for the policies of the ACI Specification Project and the normative text for the specification.

## Motivation

A Community Oriented Process for creating and evolving the ACI Specification is desirable. Using a public "Request for Comments" system allows the Core Interest Groups of the ACI Specification to meaningfully debate the specification while making it easy for community members with their own interests to comment on the development.

## Informative Explanation

<!--Provide an informative explanation of proposal. 
This is intended to be read by someone who wishes to understand the proposal but may not have advanced technical background.
This section is intended for:
* People working with ACI at a high level, probably via tooling,
* People wishing to learn about ACI without delving into low-level details,
* Aiding in understanding the Normative Text section,
* People wishing to learn the structure of the Project (for policy proposals)

This section is not normative-->

## Normative Text

### Purpose of an RFC

An RFC is required for a proposal if it makes any of the following changes:
* It modifies any of the primary specification of any part of ACI (hardware interface, standard firmware interface, host software programming),
* It establishes a project-wide policy, or charters a group within the project designed to carry out specification work in a formal manner,
* It creates a registry within the ACI Registries,
* Or otherwise if it meaningfully amends any preexisting RFC.

An RFC may also be useful, but is not necessarily required, if the change has wide impact on the project, or is important in a meaningful way.

An RFC is not required for any of the following:
* To assign a class or vendor id (other than a class id in the "Well Known" range) - contact a registrar to recieve an assignment,
* To assign a subclass to a non "Well Known" subclass - contact the owner of the class id or their subclass registrar,
* To make a change to a non-specification technical repository - file a pull request to that repository.

### Lifecycle of an RFC

The following is the Lifecycle of every RFC

0. Pre-Review (Optional): The RFC is brought for informal review and drafting, in an incomplete (or Pre-RFC) form designed for drafting and initial design,
1. Submission: The RFC is submitted to <http://github.com/ACI-Specific/rfcs> as a Pull Request. Generally, the RFC must contain the content set forth in the [content](#content) section,
2. Review and Iteration: The Pull Request is reviewed and discussed, with appropriate concerns, design questions, proposed design changes, and appropriate changes are made to address these concerns, 
3. Approval: Once the RFC is reviewed appropriately the Core Interest Groups must approve for it to be merged. Approval represents consensus to adopt the RFC.
4. Final Comment Period: After approval the RFC must undergo a 7 day final comment period. Approval may be revoked at any point by either CIG.
4. RFC Number Assignment: The RFC is assigned a number based on its PR Number and the document is renamed accordingly.

An RFC may be explicitly closed also by request of all of the Core Interest Groups - this indicates that there is consensus not to move forward at the current time. A Closed RFC may be reopened or refiled in the future.

After approval and the final comment period, any member of the Project may perform the RFC Number Assignment (if the Number was not previously assigned) and merge the RFC.

### Content

Generally, an RFC must contain at least the following:
* A One to two paragraph summary of the RFC,
* Motivation for the RFC and the underlying proposal,
* An Informative Explanation of the proposal,
* The Normative Text of the proposal.

Additionally, an RFC should specify the following, as applicable:
* Any Security Considerations that may apply to the RFC, both as to users and ,
* Any Impacts on the ACI Registries,
* A description of Prior Art that informed the proposal,
* A description of Future Changes that can be made in respect to the RFC.

### Copyright Licenses and Notices

Each RFC is provided under a unified license. Everyone who submits an RFC must permit the ACI Project to license the RFC under the unified license. 

The License for RFCs is currently (BIKESHED) and requires an RFC to change. 

The RFC License shall always be an Open Documentation License.

## Security Considerations

There are no security considerations for this RFC, as it strictly defines a policy of the Project

## Prior Art

* [Rust RFC 2](https://rust-lang.github.io/rfcs/0002-rfc-process.html)
* IETF RFC Process

## Future Direction

* This policy does not specify the method for fixing "releases" of the Specification, whether the specification is simply a snapshot of the merged RFCs as a whole at any given time, or some formal stabilization process is required,
    * Likewise, it is not yet specified how or if releases will be "versioned", and how versions will be designated or discovered,
* The Policy also Leaves Open how to modify RFCs for non-technical reasons,
* While Copyright is addressed by the Policy, Patent considerations are currently omitted. This will need to be addressed at some point in the future,
* Finally, the policy requires RFCs to be approved by the Core Interest Groups. In the future a proper team may be chartered for this purpose, and certain kinds of RFCs may be delegated to other such teams.
