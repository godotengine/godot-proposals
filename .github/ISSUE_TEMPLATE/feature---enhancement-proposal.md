---
name: Feature / Enhancement proposal
about: 'Open a new proposal'
title: 'KCP protocol support'
labels: 'topic:network'
assignees: 'networking'

---

<!--
Please fill in *all* the questions below and don't remove any of them.
Proposals not following the template below will be closed immediately.
-->

**Describe the project you are working on:**
i'm working on a online multiplayer project right now


**Describe the problem or limitation you are having in your project:**
both UDP and TCP have a lot of issues, UDP needs and NAT punch thoughts, which is tricky to do, and can cause a lot of disconnects, and some routers don't even accept that, and TCP
even tho have no issues with NAT punch thoughts, it stutters heavily when it has packed loss due to the TCP sockets freezinge

**Describe the feature / enhancement and how it helps to overcome the problem or limitation:**
KCP is a new protocol that was made with real time applications in mind, a implementation of it would give godot a severe advantage over unreal and unity as it would be way easier to make online components for godot than the other two

also there is a link that explains it's features better than i can do:

https://improbable.io/blog/kcp-a-new-low-latency-secure-network-stack/
https://github.com/skywind3000/kcp/blob/master/README.en.md

**Describe how your proposal will work, with code, pseudocode, mockups, and/or diagrams:**
i imagine something similar to TCP syntaxes with

	packet.connect_to_host_kcp( Ip, PORT)

and code that would look like

	if peerstream.get_available_packet_count() > 0:
		data = (peerstream.get_packet())
		string = data.get_string_from_ascii()
		recive_data = parse_json(string)
    
	packet.put_string(to_json(json) + "\n")

**If this enhancement will not be used often, can it be worked around with a few lines of script?:**
i don't think it's possible to implement KCP in GDscript

**Is there a reason why this should be core and not an add-on in the asset library?:**
i believe this feature is just too useful, i also believe it wouldn't weight down the core bny more than a few kilobytes


