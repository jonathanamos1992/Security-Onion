# Adding Rules

Rules are addeed via the Security Onion Manager CLI

PATH: /opt/so/rules/nids/suri/local.rules
<img width="1629" height="250" alt="image" src="https://github.com/user-attachments/assets/171cfaf0-d714-4332-a39f-b027fdb89a09" />

use 'sudo vi' to open local.rules
'sudo vi /opt/so/rules/nids/suri/local.rules'

<img width="938" height="53" alt="image" src="https://github.com/user-attachments/assets/495279f5-5cf1-4390-abfe-e66470d96be6" />
<img width="1637" height="1227" alt="image" src="https://github.com/user-attachments/assets/e24a2fc0-b84c-42a6-9be3-f405788886dc" />

Enter a rule (Make sure to delete the comment)
Rule should be in color to let you know.

For this example we made a quick Apache2 webserver on our Ubuntu machine to log traffic to port 80
<img width="1634" height="1223" alt="image" src="https://github.com/user-attachments/assets/b3937a4c-eacc-40a9-90dc-05073b504c33" />

'wq' to save and exit

confirm

'cat /opt/so/rules/nids/suri/local.rules'

<img width="1630" height="127" alt="image" src="https://github.com/user-attachments/assets/ef7aad8f-6992-4277-9563-40d64c37572f" />

### On the Manager Node:
'sudo so-rule-update'
(Should say rule added at bottom, this attempt is a redo)
<img width="1634" height="561" alt="image" src="https://github.com/user-attachments/assets/ebc9dfdf-cd31-49af-9869-44976e92f74f" />


### We write the rules on the Manager node and the Sensor nodes pull from the Manager node to update.
This is where suricata is actually running
<img width="1634" height="109" alt="image" src="https://github.com/user-attachments/assets/312da5a0-d7e0-4c2f-9a5d-df2c8877cb7c" />



### From the Sensor Node:

'sudo docker restart so-suricata'






























