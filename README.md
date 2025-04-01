## Personal Setup for [Glance](https://github.com/glanceapp/glance)

To customise your own setup, please read Glance's configuration options.

### Setup
I use the binary for Windows to run a task in Windows Task Scheduler upon logon.
This setup will run Glance at `localhost:<PORT>`.

- Download the latest Glance binary for windows from the [releases page](https://github.com/glanceapp/glance/releases/latest) and save to a folder of your choice.
- Open Task Scheduler (using start menu search).
- *(Optional)* In the left side pabel, create a new folder in Task Scheduler Library with a name of your choice.
- Create a task inside that folder by right-clicking and selecting **Create Task...**.
- Add a name for your task *(example: Glance)*.
- In the **Triggers** tab, click the **New** button and select **At log on** from the list, then click OK.
- In the **Actions** tab, click the **New** button and select **Start a program** from the list (should be pre-selected), the choose the Glance binary file that you downloaded in the first step.
- In the **Start in (optional)** field, paste the path to the Glance folder that contains the binary file you downloaded in the first step, the click OK *(example: D:\Folder\Glance\\)*.
- Click OK to save the new task.

### Environment Variables
You will need a `.env` file to be able to run this config. The file needs to be in the same directory as the `glance.exe` binary.

```
PORT=<port number>
GITHUB_TOKEN=<your github access token here>
```
