subdir('ui')

# Resources
resources = gnome.compile_resources(
    'resources',
    configure_file(
        input: 'resources.gresource.xml.in',
        output: '@BASENAME@',
        configuration: {'appdata-file': appdata_file.full_path()},
    ),
    gresource_bundle: true,
    source_dir: meson.current_build_dir(),
    install: true,
    install_dir: pkgdatadir,
    dependencies: [blueprints, appdata_file],
)