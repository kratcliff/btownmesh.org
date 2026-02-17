# Welcome!

We are [btownmesh.org](https://btownmesh.org), the [Meshtastic](https://meshtastic.org/) local group for the Bloomington, Indiana, USA area. We are still in the process of organizing, and we need _your_ help!

# Join Up

For more information, and to join the community, please join our [Signal group](https://signal.group/#CjQKINyyolxLEPQjN-GVE5SU00uSTAzC1ZP51qGY1k-lYI9uEhBswDrzUq1VRFwFDTD-tqrg). Additionally, you can find us on the [Indiana Mesh Discord](https://discord.gg/RAnPvDsxPJ).

To cut down on spam, we ask that you introduce yourself within 24 hours of joining. A simple "Hi, I'm [name], I work in [industry/profession], and I'm interested in mesh networking!" is sufficient. We look forward to meeting you!

# What is Meshtastic?

Meshtastic is an open source, off-grid, decentralized, mesh network built to run on affordable, low-power devices. You can join and be off to a great start with $50 or less. To learn more, [check out the official project documentation](https://meshtastic.org/docs/introduction/)!

You will need the following to get off to a good start:

- A compatible 915MHz LoRa device
- Proper antennas for your device (the stock antennas that come with the devices are often not ideal, so consider upgrading to a better antenna for improved range and performance)
- A smartphone or computer with a USB A port and a Chrome-based browser to configure the device and communicate with other users

An alternative but similar mesh networking project is [MeshCore](https://meshcore.co.uk/) which uses similar hardware but differs in concept. While the area primarily uses Meshtastic, MeshCore users are also welcome to join our community. All meshers are welcome! _The settings down below will not apply to MeshCore devices, however._

# Help Wanted

Our community is just getting started, and everyone is welcome to contribute!

This site, in particular, is in dire need of some content and design. Please feel free to [fork it and send us a pull request](https://github.com/kratcliff/btownmesh.org)! All meaningful contributions are appreciated.

# Our Settings

- **Frequency Range:** Frequency Slot 20 (33cm/915MHz ISM band in the US, specifically 906.875 MHz)
- **Modem Preset:** LongFast
- **Channel Name:** `LongFast`
- **Encryption:** Default (Use `AQ==` as the key)
- **Location Sharing:** Some users choose to share their location - you are welcome to do so, but it is not required.
- **MQTT:** Optional. Use `msh/US/IN` as the topic prefix if you choose to enable MQTT. Do not include a trailing slash.
  
On selecting device roles:

Please choose the role that best fits your use case. If you are unsure, the CLIENT_MUTE role is a good default choice, as it minimizes interference with other users while still allowing you to participate in the mesh network. Before setting up a router or repeater, please consider the impact on other users and ensure that you have a good understanding of how these roles work. Please experiment with CLIENT_BASE if you are interested in utilizing similar functionality to a router without the potential interference to others.

Refer to the [Meshtastic documentation on device roles](https://meshtastic.org/docs/configuration/radio/device/#roles) for more information.

If you'd like to experiment, consider switching the modem preset to MediumFast as it provides a similar experience to LongFast but won't interfere with users on the LongFast preset.
