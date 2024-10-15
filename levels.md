## What are executor levels and UNC?

**Levels:**\
Levels are an easy way to explain the capabilities of an executor. Here are their permissions, dumbed down:
```
0, None, None | Anonymous unused identity.
1, LocalGui, PluginSecurity LocalUserSecurity | Roblox studio UI.
2, GameScript, None (Keep in mind default capabilities...) | LocalScripts, Scripts, ModuleScripts, your every day scripts that you use in games.
3, ElevatedGameScript, PluginSecurity LocalUserSecurity RobloxScriptSecurity | CoreScripts **AND COREMODULES WHICH DIFFER FROM NORMAL MODULES** basically roblox's scripts found in CorePackages, ScriptContext and CoreGui.
4, CommandBar, PluginSecurity LocalUserSecurity | The command bar in roblox studio.
5, StudioPlugin, PluginSecurity | Roblox studio's plugins.
6, ElevatedStudioPlugin, PluginSecurity LocalUserSecurity RobloxScriptSecurity | Roblox's plugins.
7, COM, ALL | RCCService
8, WebService, ALL | Unknown
9, Replicator, WritePlayerSecurity RobloxScriptSecurity | Unknown
10, Assistant, UNKNOWN | UNKNOWN
```
^ This was made by Emper.\
You can see that some levels are actually better than others; a higher level does not mean a better executor. For example, level 7 is actually worse than level 6.
