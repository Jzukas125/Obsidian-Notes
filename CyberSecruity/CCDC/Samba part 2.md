
1. Verify TLS peer certificates and names to enable privacy and data security for communication between hosts. Ensure that all checks are performed (verify the host's digital certificate , hostname, IP address etc)
2. If you have extra time, write out a description explaining what each option does

   # What To Do
   
   Use tls verify peer and set ca_and_name_if_available example would be 
   tls verify peer = ca_and_name_if_available
   But the recommend option is to do the as_strict_as_possible check to ensure that all checks are done. Must be in the global or it will not work