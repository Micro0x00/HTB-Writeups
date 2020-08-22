# Decode Me!!

## hello everyone i'm Mircro0x00 and i will help you in this challenge

***At first it appears to be something that is Base64 encoded as the lines end with the usual "=" but this is not the case... yet So first thing I did, like many others, is try to decode it like this, but it fails***
***Images initially look kind of base butAfter a bunch of Googling ***

![image](https://user-images.githubusercontent.com/67539414/90959340-bde1a680-e49a-11ea-94ef-583bdbf7d81a.png)

**we look into that we find the Fernet (symmetric encryption). This is a "symmetric encryption method which makes sure that the message encrypted cannot be manipulated/read without the key.** 

**And now we know who we are dealing with**
**Open your python console or make python file as you like

![Decodeme](https://user-images.githubusercontent.com/67539414/90961831-defec300-e4ab-11ea-8c7f-b14500557917.png)
## The code
    from cryptography.fernet import Fernet
    key = "993gmULBNujjrZCDev3W8kAVaLkXiyHhCL3500188bA="
    k = Fernet(key)
    final = k.decrypt(b"gAAAAABboRUb0FsuiYBk1tsXRDr6KAzU1xrNSUv7grB-G-dAEeyqj99kUebz466I2VcH5xDa5HEc5KkbgTklQ7tm9JCRPlJtRng1Ns3VEvbrk7B835OINfPnRbc-UIOnnCmW3CgMdMtf5wGLN299AZEzxIvuy71WC5d9xJDchyiORycuzCth95-4nTKphlNQQ2ko3DX72RxWeEjwt3mavnFXqcOCkGxUhJYmFltz_6ND56VGTrXZi_CK5xLODOX4sj1GNwN_CrU3sJ0obTdA2wF5OaDZLbA1GBPfK0PDlC9WxoUf85K0tFXKfqbt3c5YqtqfytNG5gTkbDFM2NjE7BveBf1DP9ca8g==")
    print(final)
