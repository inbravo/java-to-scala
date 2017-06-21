| Topic | Scala Dev Enviornment Setup |
| :--- | :--- |
| Git sample | [scala-src](https://github.com/inbravo/scala-src) |

---

##	**Setup of Scala Enviornment**
 * You can avoid any local setup and run example online with the help of [Scastie](https://scastie.scala-lang.org)
 * You can download [Scala distro](https://downloads.lightbend.com/scala/2.12.2/scala-2.12.2.zip) and run examples on [REPL](http://docs.scala-lang.org/overviews/repl/overview.html)
 * You can also do complete Scala Dev Enviornment setup using Eclipse IDE and SBT
	* **Scala build tool setup**
	  *	Best build tool for Scala is [sbt](http://www.scala-sbt.org)  
	  ![](/assets/m-1/keep-calm-and-install-sbt.png)
	  * Download setup in your desired compression format \(zip or tgz\)
	  * Decompress the downloaded file to local directory. Ex:`/download/path-to-sbt`
	  * Update **PATH** variable to include [sbt](http://www.scala-sbt.org) Ex:`[adixit@marcus ~]$ export PATH=$PATH:/download/path-to-sbt/bin`
	* **Eclipse setup**
	  * Download [Scala Eclipse](http://scala-ide.org)
	  * Inside your local scala-src project. Execute **sbt** command: `[adixit@marcus ~]$ sbt eclipse`
	  * Last step will download all required libraries and generate Eclipse configurations
	  * When last step is done, use Eclipse import project command and import your `scala-src` project
##	**Setup of Code Samples**
  * login if you have a [Github](/github.com) account or signup, if your don't have. If you do not want to create a Github account, just download the [scala-src](https://github.com/inbravo/scala-src) as zip, using tiny green button at right side
  * After login at Github, go to project [scala-src ](https://github.com/inbravo/scala-src)and [fork](https://help.github.com/articles/fork-a-repo/#fork-an-example-repository) the repository
  * A similar repository will be available in your code space. This is going to be your personal play area.
  * Setup Github on your local enviornment. Download [Github Desktop ](https://desktop.github.com) for Windows/Mac or use [Git Command Line](https://hub.github.com)
