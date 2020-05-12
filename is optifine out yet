# by Udon

import urllib.request


def is_optifine_update_out():
    """
    checks if optifine update for a version is out hell yeah
    :return: (str) if optifine is out
    """
    page = urllib.request.Request("https://optifine.net/downloads", headers={'User-Agent': 'Mozilla/5.0'})
    site = urllib.request.urlopen(page).read()
    data = site.decode('ISO-8859-1')  # Read the content as string decoded with ISO-8859-1

    version = input("enter minecraft version: ")
    words = [version]
    value = False

    for word in words:
        for line in data.splitlines():
            if word in line:
                if "pre" in line:
                    break
                else:
                    value = True

    if value:
        print("yessir")
    else:
        print("no sir")


is_optifine_update_out()
