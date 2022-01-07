# p4wnsolo-hackwebcams
How to hack webcams

This guide assumes that you have access to the WiFi network on which the webcam(s) is/are running.


## Step 1:  Scan the network

Use Angry IP scanner to scan the range of IP addresses the WiFi network uses

To do this, find out your IP address while connected to the WiFi.

Then remove the last octet (the numbers after the last `.`)

Open Angry IP scanner, Paste the IP address into the first part of the `IP Range` fields in Angry IP Scanner ("AIPS").
Put `1` after the last `.` in the IP address, so it's something like `192.168.1.1` (where `192.168.1` is most likely different from your actual IP address)
Then Paste your IP address into the second part of the `IP Range`, but replace the last octet with `255`.  It should look like `192.168.1.255`.


## Step 2:  Test the Results

Now, you should have a list of scanned IP addresses in AIPS.

Click the `Ports` column and select `Sort by Ports`.

This shows you the IP addresses which have Open ports, indicating that a device is currently using that IP address.

In my results, the IP addresses with Open ports were `192.168.1.1`, `.3`, `.4`, `.5`, and `.10`.

Now, copy the first IP address with an Open port and Paste it into your web browser, then hit Enter to browse to the IP address.

Most likely, the first IP address is the `router` in the Network.  In my case, `192.168.1.1` is the router's IP address.

Some networks have range extenders, which came immediately after the `router` IP address on the network I scanned.  These addresses were `192.168.1.3`, `.4`, and `.5`.

How do I know this?  They (all 3) had "ASUS" router login screens.

Last but not least, I put `192.168.1.10` in my browser, and voila - it's the webcam admin login splash screen.  Score!

## Step 3:  Try default credentials

Since many people never change default passwords, just google `(Webcam brand) default password`.

In my case, the result immediately popped up as a snippet in search results.

The default username was `admin` and password `12345`.

Give the credentials a try!

If it doesn't work, you can try brute-forcing.
