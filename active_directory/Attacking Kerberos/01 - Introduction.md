What is Kerberos?

deafult auth service for windows and is more "secure" the NTLM

Common Terms:
- Ticket Granting Ticket (TGT) - A ticket-granting ticket is an auth ticket used to request service tickets from the TGS
- Key Distribution Center (KDC) the KDC is a service for issuing a TGT and service tickets taht consist of the Auth serice and TGS
- Auth Service (AS) - Issues TGT to be used by the TGS in the domain to request access to other machines and service tickets
- Ticket Granting Service (TGS) - Takes a TGT and returns a ticket to a machine on the domain
- Service Principal Name (SPN) - SPN is an identifier given to a service instance to associate a service instanc ewith a domain service account. Windows requires that services have a domain service account which is why a service needs an SPN set.
- KDC Long Term Secret Key (KDC LT Key) - The KDC key is based on the KRBTGT service account. It is used to encrypt the TGT and sign the PAC
- Client Long Term Secret Key (Client LT Key) - The client key is based on the computer or service account. It is used to check the encryption timestamp and encrypt the session key
- Service Long Term Secret Key (Service LT Key) - The service key is based on the service account. It is used to encrypt the service portion of the service ticket and sign the PAC.
- Session Key - Issued bu the KDC when a TGT is issued. The suer will provide the session key to the KDC along with the TGT when requesting a service ticket
- Privilege Attribute Certificate (PAC) - The PAC holds all of the user's relevant information. is sent with the TGT to the KDC to be signed by the Target LT Key and the KDC LT Key in order to validate the user.