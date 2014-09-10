so-data-flows
=============

Data flow diagrams for security onion

These are my attempt to get a handle on how the data travels through security onion.

I needed to be able to track down an issue where snorby and bro stopped updating and was trying to figure out what was failing.

These were generated using the Gliffy chrome plugin.

I have left the snorby data flow off as it complicates the diagram. The snorby database is written directly by the barnyard process. Any issues with the snorby database can also cause the snort agent to stop writing to sguild. 

In my opinion if you are running sguil do not run snorby, it just means you have to acknowledge alerts in two places and can cause snort alerts in sguil to stop.

Having said the above my issues were caused by too many bro workers on too many pfrings causing some form of resource contention that broke both bro and snorby.
