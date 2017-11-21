# RedstoneLocker --- Powered by [LogoCat](https://mcuuid.net/?q=logocat) 
[![mcfallout](https://i.imgur.com/o6S7V07.png)](https://mcfallout.net)
Jar Download link: [Spigot Page](https://www.spigotmc.org/resources/falloutcraft.20984/)

This plugin is a minecraft server-side spigot plugin in order to enhance the experience of:
  - Detect the source of redstone flicker and stop it right away
  - With the minimal changes to the user's orginal design (No MORE ![](https://www.csie.ntu.edu.tw/~b98902055/items/323-0.png) that breaks user's masterpiece!)

###### Tested on 70 players with positive feedbacks from hardcore redstone players (mcfallout.net)c

---------
  ### Features : 
  - Redstone flickers / flasher smart detection ![](https://www.csie.ntu.edu.tw/~b98902055/items/76-0.png)  ![](https://www.csie.ntu.edu.tw/~b98902055/items/150-0.png)
    1. All of the redstone components for calculating as part of the flickers are configurable, including 
    ![](https://www.csie.ntu.edu.tw/~b98902055/items/55-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/149-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/151-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/157-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/158-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/131-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/72-0.png) ![](https://www.csie.ntu.edu.tw/~b98902055/items/71-0.png)... and so on.
  - Soft Removal ![](https://www.csie.ntu.edu.tw/~b98902055/items/285-0.png) 
    1. Intead of brutally place a sign ![](https://www.csie.ntu.edu.tw/~b98902055/items/323-0.png) that triggers the player. This plugin quickly find the source and ' gently turn in off '. To watch how the plugin did the job
    2. Heuristic functions are included to polish the removal and avoid the [notorious false positive].
  ### Media demo : 
  
  #A flicker without automatic re-triggering wire (Could be turned off by switching the comparator)
 ![](https://i.imgur.com/UrfjbDx.png)
#Detected! Temporarily remove the least amount of wire, put a BANNED effect on the location to notice the player. 
![](https://i.imgur.com/ffu70q4.png)
Also shown in console : 
[09:58:17 INFO]: [RedstoneLocker] : Location{world=CraftWorld{name=world},x=15.0,y=21.0,z=-27.0,pitch=0.0,yaw=0.0} 
is detected for redstone flickering.

#after a short amount of time (configurable). 
![](https://i.imgur.com/C3DYBL0.png)


#A flicker with automatic re-triggering wire
![](https://i.imgur.com/XQufdWC.png)

#Detected! Temporarily remove the least amount of wire
![](https://i.imgur.com/y46hWKN.png)

#Put back all the wire after a short amount of time (configurable). 
#ONLY the power source "redstone torch" is altered. 
![](https://i.imgur.com/Aeg2dWK.png)
  
  
  - [Youtube link](https://www.youtube.com/watch?v=DOGYUIlFsTQ&feature=youtu.be) 
   This video show how the plugin react to [normal redstone structures] and [evil redstone flickers], 
   while being smart as avoiding [false positive].
---------
### Environment 
This build is compiled and tested on these environments.
* [java] - JVM 1.8
* [spigot] - 1.12.x

### Hard-Dependency
This plugin needs to run with the following plugins with the latest version to work properly:
* none
----
### Installation
1. Drop the plugin jar file in your server folder /plugins/ and run once.
2. After the plugin folder and default config.yml is generated, stop the server.
3. Start to set your own config withing config.yml.

### Configuration setting
1. All kinds of redstone components are configurable. 
2. The plugin's default value is well-tuned on a 70 people server with positive feedbacks from hardcore redstone players.  (mcfallout.net) 
```sh
version: 1.0.0
# just ignore this.
Verbosity: 0
# for developers
ENABLED_WORLD: world,world_nether,world_the_end
# change into the world name you are interested in applying RedstoneLocker!
StructureDistance: 3
# the radius of a group of redstone structures. Just leave it 3. It is a tuned parameters. 
ReleasingTimeSecond: 10
# After a redstone structure has been detected containing flickers, how long would this area could fire redstone event without being ignore.
PeriodicalTicksMax: 25
# How much a ball space radius = 3(StructureDistance) could fire redstone event every second. (A circuit could fire multiple events based on how many components are considered. See the component config below.)

COUNTING_TORCH: true
# Should the redstone torches counted as a component?
COUNTING_HOPPER: false
# Should the hopper counted as a component?
COUNTING_REPEATER: true
COUNTING_COMPARATOR: true
COUNTING_WIRE: true
COUNTING_PISTON: false
COUNTING_STICKY_PISTON: false
COUNTING_BUTTON: false
COUNTING_PRESURE_PLATE: false
COUNTING_TRAPPED_CHEST: false
COUNTING_TRIWIRE: false
COUNTING_LEVER: false
COUNTING_OBSERVER: false
COUNTING_LIGHT_SENSOR: false
COUNTING_LAMP: false
COUNTING_NOTE_BLOCK: false
COUNTING_DISPENSER: false
COUNTING_DROPPER: false
COUNTING_DOOR: true
COUNTING_COMMAND_BLOCK: false
COUNTING_RAIL: false
# All of the above setting is well-tuned and ready to be used. 

```
----
### Permission nodes
none.

### Commands
| command |description| required permission |
| ------ | ------ |---|
| /redstonelocker reload | reload the config in config.yml | op |

----
### Todos
 - Any suggestions from my customers are welcomed !

----
### License

MIT licenses https://opensource.org/licenses/MIT
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [item]: <https://www.csie.ntu.edu.tw/~b98902055/items/>

   [vault]: <https://www.spigotmc.org/resources/vault.41918/>
   [multiverse-core]: <https://www.spigotmc.org/resources/multiverse-core.390/>
   [faction]: <https://www.spigotmc.org/resources/factions.1900/>
   [griefprevention]: <https://www.spigotmc.org/resources/griefprevention.1884/>
   [worldedit]: <https://dev.bukkit.org/projects/worldedit/files/2460562>
   [placeholderapi]: <https://www.spigotmc.org/resources/placeholderapi.6245/>
   [titlemanager]: <https://www.spigotmc.org/resources/titlemanager.1049/>
   [spigot]: <https://spigotmc.org>
   [java]: <https://java.com/zh_TW/>
   [license]: <https://opensource.org/licenses/MIT>

