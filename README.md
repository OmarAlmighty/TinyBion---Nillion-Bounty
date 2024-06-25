## Show and tell project type
Builder Bounty Submission
## Github Repo Link
https://github.com/OmarAlmighty/NillionTinybioBounty

## Video Walkthough Link
https://www.youtube.com/watch?v=taAqr0GXoUg

## Project Description
This project introduces a private facial recognition system for biometric authentication using Multi-Party Computation (MPC). We leverages the power of the Nada library for our MPC solution to safeguard user data while ensuring robust verification through facial recognition and movement detection. 

Our demo authenticates a picture with a live photo of the user, so the authentication mechansim is secure against spoofing. In our demo, we capture 50 frames to be compared with the registeration photo. During the authentication phase, a user has to be moving his/her face to make sure that the user is actually there and it is not a photo of the user captured from other sources (e.g., social media).

## What problems does your project solve? How does it preserve privacy for users?
Biometric data is a common technique being used to authenticate users. However, the entire biometric feature graphs are typically stored on a single device or server. Furthermore, this technology is often used by finacial instution, increasing the incentive for attacker to get this data. Therefore data is highly sensitive if leaked, it may open the doors to identity theft, finacial fraud and irreversible compromise as facial features cannot be easily changed. 

By using MPC, a user can divide their biometric data among multiple servers in a way that disallows any single compromised server from learning information about the underlying user data. Further servers are able to perform certain computation on the user data, allowing them to compare deifferent facial recognition descriptors via Euclidean distance. The encrypted result of this computation can only be achieved if all parties work together. 

## How does the project use Nillion? Describe and link to any Nada programs
Our project uses the tinybio API to compute euclidean distance between two facial descriptor vectors. We developed a dual-purpose system for this approach. The first test is to detect a user facial features across multiple video frames, and the second test is to test movement between frames to prevent attackers from useing static photos (e.g. for LinkedIn). We also compute the intersection of these results across the different video frames. Thus, the verifier entity can view all three scores to determine the person is indeed the human who it was looking for.

## Is there anything else you want to share?
We are looking forward to have bounties that focus on implementing novel MPC features and optimizing performance of specific functions.