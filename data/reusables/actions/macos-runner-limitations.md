* All actions provided by {% data variables.product.prodname_dotcom %} are compatible with arm64 {% data variables.product.prodname_dotcom %}-hosted runners. However, community actions may not be compatible with arm64 and need to be manually installed at runtime.
* Nested-virtualization and Metal Performance Shaders (MPS) are not supported due to the limitation of Apple's Virtualization Framework.
* Networking capabilities such as Azure private networking and assigning static IPs are not currently available for macOS larger runners.
* The arm64 macOS runners do not have a static UUID/UDID assigned to them because Apple does not support this feature. However, Intel MacOS runners are assigned a static UDID, specifically `4203018E-580F-C1B5-9525-B745CECA79EB`. If you are building and signing on the same host you plan to test the build on, you can sign with a [development provisioning profile](https://developer.apple.com/help/account/manage-profiles/create-a-development-provisioning-profile/). If you do require a static UDID, you can use Intel runners and add their UDID to your Apple Developer account.
{%- ifversion ghec %}
* {% data reusables.actions.macos-unavailable-ghecom %}
{%- endif %}
