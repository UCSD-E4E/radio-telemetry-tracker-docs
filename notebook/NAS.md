# E4E NAS
Our Network-Attached Storage is where we keep files which require multiple people to access. (We lost Google Drive space, <3 UCSD)

It is recommended to add the network to your machine so you don't have to log in through your browser every time you need to access the NAS.

## Setup

The steps to do this on **Windows** are as follows:
1. In File Explorer, go to "This PC" and right-click. Select "Add a network location".
2. Click "Next" twice, then enter "\\\\e4e-nas.ucsd.edu\\rct" in the text box for the network address.
3. Give a name to the network. You should include "rtt" and "e4e" in some way so you know what it is in the future.
4. You can now access RTT's directory on the NAS as a network location by returning to "This PC" on your file system.

And on **Mac**:
1. Go to Applications > Utilities > Disk Utility.
2. Click File > NFS Mounts > +.
3. Enter "//e4e-nas.ucsd.edu/rct" as the remote URL and enter a chosen location at which to mount it.

## (Some) Important Folders

The rct directory on the NAS has the following folders of which you should be aware:
- **CAD**: contains CAD files for physical pieces
- **From Google Drive**: contains data migrated from Drive in early 2023 (you shouldn't need to dive deep into this often)
- **Presentations**: contains past presentations, such as old dsp concepts and collaborator meeting presentations
- **Programmatics**: contains documentation and planning
- **test**: contains writeup of previous testing done to the system or its components
