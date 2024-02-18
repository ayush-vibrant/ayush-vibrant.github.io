# Worldcoin: My understanding of Sama's latest initiative

WorldCoin's vision is "to become the world's largest human identity and financial network, giving ownership to everyone".

## So, how Does Worldcoin Work? 🚀

1. **Install the App & Create a Wallet**:
   To participate in the Worldcoin ecosystem, users need to install the Worldcoin app and create their digital wallet.

2. **Iris Scan & Public Key**:
   During registration, users provide an iris scan and a public key through the app.

3. **Secured Hash Upload**:
   Worldcoin employs advanced cryptographic techniques, where an Orb signs a message approving a specialized hash of the user's iris scan. This hash is uploaded to a database - currently centralized but planned to transition to a decentralized on-chain system, ensuring data integrity.

4. **Privacy-Preserving**:
   The system does not store full iris scans, only hashes. These hashes are used to check for uniqueness, ensuring privacy while creating a secure World ID for each user.

5. **Zero-Knowledge Proofs**:
   World ID holders can prove their uniqueness without disclosing their actual identity. They achieve this through Zero-Knowledge Succinct Non-Interactive Argument of Knowledge (ZK-SNARK), demonstrating that they hold the private key corresponding to the public key in the database.


## Addressing the Loopholes of Worldcoin

1. **Privacy**:
   The registry of iris scans may reveal information. Although currently the system only stores hashes, there may still be risk of information inference.
   At the very least, if someone else scans your iris, they can check it against the database to determine whether or not you have a World ID. Potentially, iris scans might reveal more information.

2. **Accessibility**:
   The success of the project relies on having an extensive network of Orbs, allowing anyone worldwide to access the system seamlessly. Otherwise, it just won't work.

3. **Centralisation**:
   Just using blockchain does not guarantee true decentralisation in case of worldcoin. The Orb is a hardware device, and we have no way to verify that it was constructed correctly and does not have backdoors. Hence, even if the software layer is perfect and fully decentralised, the Worldcoin still has the ability to insert a backdoor into the system.

4. **Security**:
   User's phones could be hacked. Users could be coerced into scanning their irises while showing a public key that belongs to someone else. And there is the possibility of 3D-printing "fake people" (Biometric Spoofing) that can pass the iris scan and get World IDs.


I love what Worldcoin stands for and their mission is truly inspiring. But we need to be aware of possible challenges.
It's a long road ahead. And I'd love to see how it turns out to be.