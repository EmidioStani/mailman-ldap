mailman-ldap
============

Perl script to extract ldap groups and users and add them in mailman

The script searches for groupOfUniqueNames groups and it verify that the attribute mail for the groups exists.
If it exist it searches for the users belonging to the group by looking for the attribute uniqueMember, the user found is added to the list if it has a mail attribute set and it is not disabled ( looking for ds-pwp-account-disabled attribute specific to OpenDJ, in other cases you could use the attribute pwdAccountLockedTime).

The original script has been taken from http://www.warden.pl/2010/02/01/synchronizing-mailman-lists-with-ldap/

Differences from the original are:

1. saving in variables mailman path bin and list
2. changed attribute mailGroup to groupOfUniqueNames and added search for mail attribute on group
3. changed condition on user search for disabled account with OpenDJ
4. now the email of the group is not anymore added to the group itself

