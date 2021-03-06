**4.0.5** *(Apr 1 2020)*
- The frontend will now auto calculate the "24h Peak" label using your configured graphDuration in config.json

**4.0.3** *(Apr 1 2020)*
- Updated jquery dependency, 2.1.4->3.4.1
- Updated socket.io dependency, 1.3.7->2.3.0 (fixes several socket.io low risk vulns)
- Logs CF-Connecting-IP/X-Forwarded-For headers when present
- Added Minecraft version 1.15.1 support to config.json & minecraft.json

**4.0.2** *(Apr 1 2020)*
- Updated install.sh & start.sh scripts
- Committed package-lock.json
- Fixed outdated package.json version

**4.0.1** *(Apr 1 2020)*
- Fixed potential crash issue during startup when determining 24 hour graph peaks.
- Fixed a bug in the frontend that could result in "undefined" AM/PM time markers.
- Added protection to prevent artifically high player counts (>250k) degrading browser performance by abusing the graphs.
- Updated mime dependency, 1.3.4->2.4.4
- Updated request dependency, 2.74.0->2.88.2 (deprecated, should investigate removal)
- Updated sqlite3 dependency, 3.1.8->4.1.1 (fixes macOS install issue)
- winston & socket.io dependencies were not updated due to broken behavior. Will investigate as a follow up patch.

**4.0.0** *(Mar 30 2020)*
- Added dark mode
- Added 24hr peak feature
- Removed legacy category system
- Removed /status.json deprecation warning
- Removed Google Analytics tracker
- Changed default footer text
- Various bug fixes
- Removed gulp build tools

**3.1.0** *(Mar 14 2017)*
- Updated design. More flexible!
- Automatically builds indexes on database.
- Fixes issue with record query.

**3.0.0** *(Mar 11 2017)*
- Adds player count records.
- Adds "serverTypesVisible" to hide PC/PE badges.
- Moves Minecraft protocol versions out of site.js and into minecraft.json.
- Design tweaks to remove fluff.
- Fixes various bugs.

**2.2.2** *(Jul 5 2016)*
- Now builds against mcpe-ping-fixed (requires a ```npm install```)!

**2.2.1** *(Jun 20 2016)*
- Design tweaks (sticky bar at top, updated header/footer)
- New favicon 

**2.2.0** *(Mar 6 2016)*
- Added supported versions per network (courtesy of [@forairan](https://github.com/forairan))
- Updated dependency version of ```mc-ping-updated``` to 0.1.0

**2.1.0** *(Feb 23 2016)*
- You can now categorize servers. Add a "category tag" to their entry in ```servers.json```.
- Define the tags in ```config.json```, such as below:

```
"serverCategories": {
	"major": "Major Networks",
	"midsized": "Midsized Networks",
	"small": "Small Networks"
}
```
- If you have no categories, it will create a (hidden) category named "default".
- You can control whether or not categories are visible by default using the "categoriesVisible" tag in ```config.json```. 
  - If true and there's >1 category, the browser will have an option to hide/show the categories. Otherwise the controls are always hidden.
- New endpoint (```publicConfig.json```) allows the browser to know system details before the socket connection is established.
- New header design to make it less annoying.
- Various bug fixes.

**2.0.0** *(Feb 1 2016)*
- Servers are now referenced by their name on the graph controls instead of their IP.
- Servers now display their name on hover instead of their IP.
- Graph controls are now saved and loaded automatically.
- Moved server configuration into servers.json from config.json.
