godot-package
=============

godot-package is a lightweight tool for managing and downloading dependencies in Godot projects

configure
---------

Copy `addons/godot-package/` into project and create `package.gd` file with required dependencies.

Example package.gd:

    extends "res://addons/godot-package/package.gd"

    func _requirements():
        dependency("nonameentername/godot-csound", {"tag": "v0.1.0-beta.9"})   

dependency should include github project and tag for a specific release.

install
--------

To download the dependencies run the following command on a terminal:

    godot --headless -s package.gd install
