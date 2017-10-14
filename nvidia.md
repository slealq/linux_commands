# Virtual ssh -X from old ati to new nvidia
We need to enable two Options for allowing indirect GLX so we need that **xorg.conf** looks like this:

    
    Section "SeverFlags"
        Option "AllowIndirectGLX" "on"
	    Option "IndirectGLX" "on"
    EndSection
    