Coding Requirements

● Complete the assignment in Python and 1 other programming language of your choice
● Provide a link to the 2 projects in a repository on Github, Gitlab, or similar upon
completion.


Assignment
The client has provided 2 csv files with user data that they would like to import to the system:

File A:
user_id,email
oi6IhEzu9R,user_2@example.com
fQFLNRDae8,user_5@example.com
fBYRtPtAlC,user_7@example.com
fOSjdLnNP3,user_9@example.com
uxz2jFwr5I,user_1@example.com
zSbmdNiSHH,user_4@example.com
fjM66woroy,user_0@example.com
oh4mHXh8zN,user_3@example.com
gXWj37JC5d,user_8@example.com
4dBdXURAz3,user_6@example.com

File B:
user_id,first_name,last_name
oh4mHXh8zN,Julie,Mosser
zSbmdNiSHH,Taryn,Jaycox
fBYRtPtAlC,John,Smith
fjM66woroy,Yadira,Irving
fQFLNRDae8,Vella,Lynam
fOSjdLnNP3,Qiana,Walk
uxz2jFwr5I,Benito,Festa
oi6IhEzu9R,Leatrice,Oquinn
4dBdXURAz3,Jacques,Cuellar
gXWj37JC5d,Shaun,Kreiger

However some user IDs are incorrect because these users already exist in the system under
different user_id values. Generate a merged file in the format:
user_id,email,first_name,last_name
But make sure that for the incorrect records, user_id is taken from the system, rather than from
the list provided from the client.

Materials
● API documentation - https://docs.piano.io/api
● Domain for API requests - sandbox.piano.io
● AID (Application ID) - o1sRRZSLlw
● API Token - xeYjNEhmutkgkqCZyhBn6DErVntAKDx30FqFOS6D
