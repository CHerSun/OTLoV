NOTE: To load file that has no dedicated template - select the file specifically (not it's folder).

# "Brocade SSHOW_SYS (stripped).txt"
One of quite typical tasks is to check transmit / receive signal levels for SFPs. This could show if a cable or an SFP is misbehaving. Open the file and try a filter:
	>^port ^port\s+\d+: -> ^(TX|RX|Port)

# "MP-SEL - verbose.txt"
People often use verbose log formatting. It's not a very convenient format to work with. Here I want to reduce amount of text that I need to read by limiting alert level. Try a filter:
	>^Log.Entry -> -^$ -> alert.level.[3-9] ++ --
