# Virtual ssh -X from old ati to new nvidia
We need to enable two Options for allowing indirect GLX
xorg.conf Should look like this:

    
    Section "SeverFlags"
        Option "AllowIndirectGLX" "on"
	    Option "IndirectGLX" "on"
    EndSection
    