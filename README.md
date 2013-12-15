openldap-faq
============

This is a small faq for repeated questions on #openldap on freenode. Some of these are not
excatly questions, but it will most likely answer your question anyway.

## Any question related to phpldapadmin?
Don't use phpldapadmin. Use Apache Directory studio if you want a gui.

## How do i get posix groups working for my linux/unix stuff
Don't use nis.schema. Use rfc2307bis. It makes posixgroups auxilliary to groupOfNames, allowing you
to use you groups for other types of access controlls as well, for example webapps.

## How do i configure my unix machines to have users/groups etc in ldap?
	- Configure /etc/nsswitch.conf
	- Configure pam
	- Configure nslcd OR sssd

## How do i configure my unix machines to use active directory?
Contact you support at microsoft. 

## How do i create a secure openldap server?
You read, and understand the admin guide hosted at openldap.org. In short you do the following:
	- Create tight acls
	- Use kerberos for authentication
	- Use TLS for transport security

## I have found a bug in openldap-2.3-VENDOR
If you use the packages provided by a vendor, it is most likely years behind. It is not unlikely
that your bug only exists in the vendors packages. Compile the latest openldap and see if the 
problem persist, and we will try to help you.

## I don't want to use anything except the one from my vendor, as I will loose support
Contact your vendor then.
