mailman-ldap
============

Perl script to extract ldap groups and add them in mailman

The script make use of groupOfUniqueNames group and it verify that the attribute mail for the groups exists.
If it exist it searches for the users looking for the attribute uniqueMember, then for each member it searched the attribute mail.

The original script has been taken from http://www.warden.pl/2010/02/01/synchronizing-mailman-lists-with-ldap/

Differences from the original are:

1. saving in variables mailman path bin and list
2. changed attribute mailGroup to groupOfUniqueNames and added search for mail attribute on group
3. changed condition on user search for disabled account with OpenDJ
4. now the email of the group is not anymore added to the group itself

