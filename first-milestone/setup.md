| **Topic** | **Setup** |
| :--- | :--- |
| Time required | 60 minutes |
| Benefits realized | Ability to run Scala examples locally |

---

This excersice involves three actions

* **Scala build tool setup**
  *	Best build tool for Scala is [sbt](http://www.scala-sbt.org)
  ![](/assets/m-1/sbt.png)
  * Download setup in your desired compression format \(zip or tgz\)
  * Decompress the downloaded file to local directory. Ex:`/download/path-to-sbt`
  * Update **PATH** variable to include [sbt](http://www.scala-sbt.org ). Ex:`[adixit@marcus ~]$ export PATH=$PATH:/download/path-to-sbt/bin`

* **Code setup**

  * login if you have a [Github](/github.com) account or signup, if your don't have
  * If you do not want to create a Github account, just download the [scala-src](https://github.com/inbravo/scala-src) as zip, using tiny green button at right side
  * After login at Github, go to project [scala-src ](https://github.com/inbravo/scala-src)and [fork](https://help.github.com/articles/fork-a-repo/#fork-an-example-repository) the repository
  * A similar repository will be available in your code space. This is going to be your personal play area.
  * Setup Github on your local enviornment. Download [Github Desktop ](https://desktop.github.com/)for Windows/Mac or use [Git Command Line](https://hub.github.com)

* **Eclipse setup**

  * Download [Scala Eclipse](http://scala-ide.org/)
  * Inside your local scala-src project. Execute **sbt** command: `[adixit@marcus ~]$ sbt eclipse`
  * Last step will download all required libraries and generate Eclipse configurations
  * When last step is done, use Eclipse import project command and import your `scala-src` project



