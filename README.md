# create-desktop-profile-package
Little script that takes an image and creates a profile and package to deploy.

    Usage: create_desktop_profile_package
        -w  --wallpaper location of the wallpaper you want to push out and create a profile for
        -v  --version   version of the wallpaper (must increment if you want to overright previous)
        -o  --output    directory to output packages to (defaults to current directory)
        -h  --help      show this help text

    create_desktop_profile_package packages an image to install into /Library/Desktop Pictures
    and creates a profile to assign that wallpaper.

## Design choice:
I'm not 100% sure on how to handle the scripting of the profile. There are two
options:
1) Have `uuidgen` insert the UUID's for the profile
2) Hard code the UUID's

If doing the former, you can't create a new version and overwrite the previous
version on a destination computer without altering the UUID back to the
original. With the later, any profile you create will be overwritten.
¯\\__(ツ)_/¯ It's a decision that you'd have to make. I set the default to option 1.