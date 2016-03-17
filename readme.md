Q: NFC necklaces store a CSV string to NDEF formatted data compressed from the maternal and health card; in the case the format changes, how would you update the mobile app to be backwards compatible with previously administered necklaces ?


My Interpretation of the problem statement:

-> The NFC device (Near Field Communnication device)  holds the data as a CSV string.

-> A CSV string implies that the  NDEF (NFC Data Exchange Format) is in the form of 'PLAIN_TEXT'.

-> Let us assume that the NDEF format  changes in future from 'PLAIN_TEXT' to some other format like 'URI' or 'SMART_POSTER'. 
	(considering that the new format is also NDEF)
	(for convinence let us assume that new NDEF format is 'URI')

-> The task is to update the mobile app such that it is compatible with both formats 'PLAIN_TEXT' as well as 'URI'.


Proposed Solution:

We can update the mobile app to handle multiple NDEF records simultaneously.

1. Lets add 'intent-filter' for both 'PLAIN-TEXT' as well as 'URI' in AndroidMenifest.xml

2. Modify the code in MainActivity.java accordingly.
