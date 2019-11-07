# Beat Saber Custom Avatars Plugin
[![Jenkins](https://img.shields.io/jenkins/build/https/ci.gnyra.com/job/CustomAvatarsPlugin/job/master?style=flat-square)](https://ci.gnyra.com/blue/organizations/jenkins/CustomAvatarsPlugin/)
[![GitHub](https://img.shields.io/github/license/nicoco007/CustomAvatarsPlugin?style=flat-square)](https://github.com/nicoco007/CustomAvatarsPlugin/blob/master/LICENSE)

## Contributing
Guidelines coming soon.

To automatically copy the compiled DLL to Beat Saber's installation directory, add a file called `CustomAvatar.csproj.user` next to `CustomAvatar\CustomAvatar.csproj` and paste in the following:

    <?xml version="1.0" encoding="utf-8"?>
    <Project ToolsVersion="Current" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
      <PropertyGroup>
        <PostBuildEvent>copy "$(TargetPath)" "D:\SteamLibrary\steamapps\common\Beat Saber\Plugins"
    copy "$(TargetDir)$(TargetName).pdb" "D:\SteamLibrary\steamapps\common\Beat Saber\Plugins"</PostBuildEvent>
      </PropertyGroup>
    </Project>