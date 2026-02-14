# DSA_Project-HNDNE-25.2F
Temporary Extranet Network Access Management using Min Heap Data Structure

## Academic Information

**Institute:** National Institute of Business Management  
**School:** School of Computing and Engineering  
**Course:** Higher National Diploma in Network Engineering  
**Module:** Data Structures and Algorithms  
**Batch:** 25.2F  
**Group No** 3

**Team Members:**

- Name: FERNANDO M V S 
- Index_NO: COHNDNE252F-001

- Name: METHNULI J K P D D 
- Index_No: COHNDNE252F-003


## Project Overview

The proposed project simply presents how a manual based system will be transformed into an automated system in order to manage the temporary network access using the data structure of Min Heap. The supposed strategic solution ensures that the external users receive a temporary access within an expiration time frame under role based policy and will be monitored while active session is live. Hence, it will guarantee that the network infrastructure stay secured, controlled and undisturbed.

## Network Scenario

A network usually operates via intranet and extranet. The external users like visitors, auditors consultants will have the requirement in connecting to the extranet. Each user session must be within a limited time 

## Problem Context

According to the current state the organization lack in handling the external users on a time-based in an automatic manner. In manual way monitoring suspicious activities, allocating time sessions and allocation of users role-wise seems inefficient and error inclined. 

## Objectives

- Transforming access control system into automated
- Allocating users based on role
- Priority based time-session 
- Expiration time-frames
- Enhance network security
- Application of an efficient data structure for extranet management


## Solution
Selected Data Structure - Min Heap

In order to maintain efficiency in managing the network the Min Heap will be used as the tactic data structure for our temporary access system. (It provides the ability in storing temporary users, operating sessions, automatic revokes, order maintenance and seeking for certain sessions)

## Characteristics of Min Heap
	# Binary Tree
	# Parent-Child order
	# Fast access to minimum
	# Efficient 
	# Dynamic 

## Mapping

each node will be indicated as the external user session and the heap key will hold the value of expiry time.

Node →  Temporary session
Key → Expiry time
Root → session to be expired
Insert → Grant Access
Search → find specific sessions
Delete → immediate removal


## Justification

As for our system it requires user insertion, session updates, immediate withdrawal and seek of certain users. the ability of a list or queue is limited since scanning all nodes or users in finding the next expiry will be slow and inefficient. For the sake of better performance, scalability, security and efficiency Min Heap is at the peak point of suitable data structure compared to linear structures.

## Workflow/ Overview

01. User requests for temporary access 
02. Expiry time assignment based on role policy
03. Session detection into Min Heap
04. Detection of root that to be expired
05. Session annulment of root node and revoke access 
06. Monitoring for abnormal behaviours and immediate removal

## Time Complexity

Efficient operations with low time complexity

  insertion - O(logn)
  deletion - O(logn)
  root peek - O(1)

-> Insertion: when granting new access for user session
-> Deletion: Revocation of expired session
-> Root Peek: access next expiry, quick identification of the session soon to be removed

## Use Cases - Network Relevancy

The proposed solution uses Min Heap to manage temporary access in an efficient way. 
the same tactic data structure concept can be applied within;
	- Network Access Control Systems
	- VPN session Management
	- Firewall timeout enforcement
	- Guest Wi-Fi 
	- Zero Trust security architectures (no default trust on users or devices)

## Conclusion

The project is a portrayal of applying the most appropriate data structure for a problem that exists within a network infrastructure when providing the access for external users via extranet. The solution is more valid since it meets the requirements like preservation of order, prioritization the session, instant revokes, spotting the exact users while conserving the security with scalable options. In addition solution connects data structure and algorithm in a way while providing a practical clarification on addressed issue within an organization in handling the management of network access system which was in manual with the usage of Min heap data structure 
	
