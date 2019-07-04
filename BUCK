apple_asset_catalog(
  name = 'MyAssetCatalog',
  dirs = glob([
    'App/**/*.xcassets',
  ]),
)

apple_resource(
    name = 'AppResources',
    dirs = [],
    files = glob([
        'App/**/*.storyboard',
        'App/**/*.xib'
    ]),
)

apple_bundle(
  name = 'App',
  binary = ':AppBinary',
  deps = [':AppResources'],
  extension = 'app',
  info_plist = 'App/Info.plist',
  tests = [],
)

apple_binary(
    name = 'AppBinary',
    srcs = glob([
        "App/*.m",
        "App/*.swift"
    ]),
    headers = glob(['App/*.h']),
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
    ],
)
