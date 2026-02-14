## TEMPORARY EXTRANET NETWORK ACCESS MANAGEMENT USING MIN HEAP

The software-based automatic extranet access control system operate for main three scenarios:
 
## ALGORITHM : Access Allocation

Step 01 : Gathering user information through a digital form.
Step 02 : Assign User ID and Expiry time Automatically
Step 03 : Create the Heap node with user information.(UID, Role, Access Scope, Expiry time)
Step 04 : Insert the user into the Heap
Step 05 : Enable User Access

Pseudocode 

	FUNCTION AllocateAccess(UserForm):
    		UID = GenerateUserID()
    		ExpiryTime = AssignExpiry(UserForm.Role)
    		Node = CreateHeapNode(UID, UserForm.Role, UserForm.AccessScope, ExpiryTime)
   		HeapInsert(Node)
    		EnableAccess(UID)
	END FUNCTION

-------------------------------------------------------------------------------------------------------


## ALGORITHM : Expiry Enforcement & Extension

Step 01 : Checks the Root of the heat for next user to be expired.
Step 02 : Check if ;
          current time >= Expiry Time
	  If yes;
Step 03 : Sends an Extension request notification to the user.
Step 04 : If user needs to extend the Time;
	  Update Expiry time in the node.
	  Rebalance the heap if needed
Step 05 : If user don’t need extension;
	  Remove the user (Root) from heap
	  Revoke Access. 
          Update the Heap 


Pseudocode 

	FUNCTION CheckExpiryAndExtension():
    		RootNode = HeapRoot()
    
    		IF CurrentTime >= RootNode.ExpiryTime THEN
        		NotifyUserForExtension(RootNode.UID)
        
        		IF UserWantsExtension(RootNode.UID) THEN
            			RootNode.ExpiryTime = GetNewExpiryTime()
            			Heapify(RootNode)
        		ELSE
            			HeapRemoveRoot()
           			RevokeAccess(RootNode.UID)
        		END IF
    			END IF
		END FUNCTION


-------------------------------------------------------------------------------------------------------



## ALGORITHM : Unusual Behavior Detection

Step 01 : Receives detected user’s UID.
Step 02 : Find the node of  that UID within the heap.
Step 03 : Remove the User from the heap.
Step 04 : Update the Heap accordingly.
Step 05 : Revoke the user access immediately.


Pseudocode 

	FUNCTION HandleUnusualBehavior(UID):
    		Node = FindNodeInHeap(UID)
    
    		IF Node EXISTS THEN
       			HeapRemove(Node)
        		RevokeAccess(UID)
   		END IF
	END FUNCTION
