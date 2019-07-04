apple_resource(
    name = 'ShopcietyResources',
    dirs = [
        'Shopciety/Assets.xcassets'
    ],
    files = glob([
        'Shopciety/**/*.storyboard',
        'Shopciety/**/*.xib'
    ]),
)

apple_bundle(
  name = 'Shopciety',
  binary = ':ShopcietyBinary',
  deps = [':ShopcietyResources'],
  extension = 'app',
  info_plist = 'Shopciety/Info.plist',
  tests = [],
)

apple_binary(
    name = 'ShopcietyBinary',
    srcs = glob([
        "Shopciety/*.m"
    ]),
    headers = glob(['Shopciety/*.h']),
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework',
        '$SDKROOT/System/Library/Frameworks/UIKit.framework',
    ],
)
