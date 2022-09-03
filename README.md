DAML Version of the eCOM Registry to allow Resource Issuers (Publishers) to nominate Resource Owners, and for Owners to grant Visibility (Observer) to other parties who
can in-turn request "Access" from the Owner to download the Resource

The eCOM Registry is composed of two main components, the "Private Registry" (PR) and the "Shared Registry" (SR).

The PR is deployed on-premise and is used by organisations to "Register" Resources (Documents, URLs, Messages, Events) to a Blockchain along with the Hash of the Resource (for data integrity), metadata which describes the Resource and signed by the User and Organisation that holds the Resource.

The Resource Holder (Registrar) can choose to "Publish" the Resource metadata to the "Shared Registry" Network either as a Private or Public Resource.  At the time of Publishing, the Resource Holder can set themselves as the Resource Owner or nominate another party on the Network as the Resource Owner. The Published Resource details (Hash, Metadata, Owner, etc.) are recorded on the Blockchain.

Public Resources are "visible" to all other parties on the network. Only the Resource Owner can "Share" a Private Resource with another party.  Once a party has "visibility" to a Resource, they can request permission to "Access" the Resource from the Resource Owner.  If access is granted, the party can download the resource directly from the Resource Holder.

This DAML project reproduces the following processes from the eCOM Registry

  1.  Resource Holder publishing a Private Resource and nominating another party as Owner - Creates "Publish" Contract
  2.  Resource Owner adding other parties as an "Observer" to the contract so they have access to the metadata
  3.  An Observer requesting Access to the Resource from the Owner through an access proposal - Creates "AccessProposal" Contract linked to the "Publish" Contract
  4.  The Resource Owner accepting the Access Proposal - Creates "Access" Contract
  5.  The Resource Owner Transfering the "Access" Contract to the Requester
  6.  The Requester adding the Resource Holder as an "Observer" to the "Access" Contract.  This notifies the Resource Holder that the Owner has granted the Requester access to the Resource
  
This DAML does not cover the Resource "Registration" the the Private Registry, or the downloading of the resource by the Requester from the Holder.
