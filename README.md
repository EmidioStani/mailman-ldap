mailman-ldap
============

Perl script to extract ldap groups and add them in mailman

The script make use of groupOfUniqueNames group and it verify that the attribute mail for the groups exists.
If it exist it searches for the users looking for the attribute uniqueMember, then for each member it searched the attribute mail.

The original script has been taken from http://www.warden.pl/2010/02/01/synchronizing-mailman-lists-with-ldap/

Differences from the original are:
# put in variable mailman path bin and list
# changed attribute mailGroup to groupOfUniqueNames and added search for mail attribute on group
# changed condition on user search (removing the locking condition)
# changed the fact that the email of the group is not anymore added to the group itself

