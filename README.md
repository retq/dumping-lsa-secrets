# LSA Secrets

### What is stored in LSA Secrets ?

Originally, the secrets contained cached domain records. Later, Windows developers expanded the application area for the storage. At this moment, they can store PC 
users' text passwords, service account passwords (for example, those that must be run by a certain user to perform certain tasks), Internet Explorer passwords, RAS 
connection passwords, SQL and CISCO passwords, SYSTEM account passwords, private user data like EFS encryption keys, and a lot more. For example, the NL$KM secret 
contains the cached domain password encryption key.

### What are LSA Secrets ?

LSA secrets is a special protected storage for important data used by the Local Security Authority (LSA) in Windows. LSA is designed for managing a system's local security policy, auditing, authenticating, logging users on to the system, storing private data. Users' and system's sensitive data is stored in secrets. Access to all secret data is available to system only. However, as shown below, some programs, in particular Windows Password Recovery, allow to override this restriction.

### Where are they stored ?

LSA secrets are stored in an encrypted form in the Windows registry, in the HKEY_LOCAL_MACHINE/Security/Policy/Secrets key. The parent key, HKEY_LOCAL_MACHINE/Security/Policy, contains the additional data, necessary for accessing and decrypting the secrets. Here are the descriptions of some values of this key

![image](https://user-images.githubusercontent.com/73394656/169624963-59350ceb-3b5b-4721-8d97-e62378dfb920.png)
