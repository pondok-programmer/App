third_party_deps = [
    '//Libraries/ViewDSL:ViewDSL'
]

apple_resource(
    name = 'AppResources',
    dirs = [
      'App/Assets.xcassets'
    ],
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
    deps = [
        ':AppLibrary'
    ]
)

apple_library(
    name = 'AppLibrary',
    srcs = glob([
        "App/*.m",
        "App/*.swift"
    ]),
    deps = [
        '//Carthage/Checkouts:ViewDSL'
    ],
    headers = glob(['App/*.h']),
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
    ],
)