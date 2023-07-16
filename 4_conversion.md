We are given a file `Message`. It looks like a base64 string.  
Converting the base64 data to a binary file gives out an audio file.  
`base64 -d Message > message_audio`

On playing the audio file, it seems that the audio is playing in reverse.  
So, by opening the file in Audacity, and reversing the audio gives the flag text:  
`dumb_audio_flag`

That is:  
`CTF{dumb_audio_flag}`

