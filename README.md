# create-desktop-profile-package
Little script that takes an image and creates a profile and package to deploy.

    Usage: create_desktop_profile_package
        -w  --wallpaper location of the wallpaper you want to push out and create a profile for
        -v  --version   version of the wallpaper (must increment if you want to overright previous)
        -o  --output    directory to output packages to (defaults to current directory)
        -h  --help      show this help text

    create_desktop_profile_package packages an image to install into /Library/Desktop Pictures
    and creates a profile to assign that wallpaper.
