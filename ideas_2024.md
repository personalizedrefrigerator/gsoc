# GSoC 2024 Ideas

This is another round for Joplin at Google Summer of Code. Detailed information on how to get involved and apply are given in the [general Summer of Code introduction](https://joplinapp.org/help/dev/gsoc/gsoc2023/)

**These are all proposals! We are open to new ideas you might have!!** Do you have an awesome idea you want to work on with Joplin but that is not among the ideas below? That's cool. We love that! But please do us a favour: Get in touch with a mentor early on and make sure your project is realistic and within the scope of Joplin. This year's themes are:

- **Plugins** - leverage the Joplin plugin API to add new functionalities
- **External apps** - leverage the Joplin public API to create external applications
- **Independent modules** - create self-contains modules within the core application
- And you are welcome to suggest your own ideas.

## Information for Contributors

These ideas were contributed by our developers and users. They are sometimes vague or incomplete. If you wish to submit a proposal based on these ideas, you are urged to contact the developers and find out more about the particular suggestion you're looking at.

Becoming accepted as a Google Summer of Code contributor is quite competitive. Accepted contributors typically have thoroughly researched the technologies of their proposed project and have been in frequent contact with potential mentors. **Simply copying and pasting an idea here will not work.** On the other hand, creating a completely new idea without first consulting potential mentors rarely works.

## List of ideas

### 1. Seamless desktop application updates

The desktop application currently supports automatic updates, however the process is not particularly smooth: the user is presented with a modal dialog, where they need to click "Download" and that opens the default browser to download the file. Then they need to run this file and go through the installer.

We would like to make this process smoother:

- The installer should be automatically downloaded in the background

- It should then install the app automatically when the next time the app is started

- And this should work at least on Windows and macOS (Linux may be special due to the different distribution methods)

Expected Outcome: The app shall inform the user that an update is available. If an update shall be applied, the installer runs the update process fully automatically in the background during the next startup. It shall be explored if a live update is feasible and how conflicts can be resolved as used files are to be replaced.

Difficulty Level: Medium

Skills Required: TypeScript, React. Some knowledge of Electron and electron-builder.

Potential Mentor(s): [Daeraxa](https://github.com/Daeraxa/), [StefanM](https://github.com/PackElend)

Expected size of project: 175 hours

### 2. PDF annotations

We would like to add annotation support to the beta PDF viewer on desktop. The annotation tools should be similar to what's in Apple Preview for instance - ability to draw over a PDF, to add text boxes, to draw lines and arrow, etc. These annotations must be saved to the file.

Expected Outcome: Add annotations to a PDF file

Difficulty Level: High

Skills Required: JavaScript

Potential Mentor(s): [CalebJohn](https://github.com/CalebJohn), [K. C. Tessarek](https://github.com/tessus/)

Expected size of project: 175 hours

### 3. Plugin inspector

Electron provides an API that allows inspecting any sub-process it creates. We can use that to monitor the performance of each plugin - how much CPU they use, how much memory, etc. We would also like to display an alert in the app if a plugin is using too much resources over a long period of time.

Expected Outcome: A module that interacts with the Electron API and gather information about the plugin processes. A window that displays the list of plugin along with CPU and memory information. An alert when a plugin uses too much resources.

Difficulty Level: High

Skills Required: JavaScript, Electron

Potential Mentor(s): [K. C. Tessarek](https://github.com/tessus/), [Roman](https://github.com/roman-r-m)

Expected size of project: 350 hours

### 4. Template insertion tool

Joplin can store general templates as notes that can be used in various contexts. For example, it could have email templates that could be inserted into a Thunderbird email. Or code snippets that could be inserted into a text editor. The workflow will be as follows

- User presses a global shortcut, for example, Ctrl+Alt+T, from any text editor (email client, code editor, etc.)
- A floating window is opened, from which the user can pick a note
- Once a note is selected, its content is inserted into the text editor

Expected Outcome: This can developed as an external application or possibly as part of the core application, but some changes will have to be made to allow this. It needs to work at least on Windows and macOS.

Difficulty Level: High

Skills Required: JavaScript, Windows/macOS programming

Expected size of project: 175 hours

Potential Mentor(s): [Daeraxa](https://github.com/Daeraxa/), [CalebJohn](https://github.com/CalebJohn)

### 5. AI-supported summary of notes and notebooks

When your quantity of notes grows you may want to summarize them or an _Abstract_. That action shall be leveraged by AI.

Expected Outcome: This can developed as an external application or possibly as part of the core application, but some changes will have to be made to allow this. It needs to work at least on Windows and macOS.

Difficulty Level: High

Skills Required: JavaScript, Windows/macOS programming, ML, AI

Potential Mentor(s): [Roman](https://github.com/roman-r-m), [K. C. Tessarek](https://github.com/tessus/)

Expected size of project: 350 hours

### 6. AI-supported categorizing, tagging 

When your quantity of notes grows you may want to review tags and rearrange notes and notebooks.  That action shall be leveraged by AI.

Expected Outcome: This can developed as an external application or possibly as part of the core application, but some changes will have to be made to allow this. It needs to work at least on Windows and macOS.

Difficulty Level: High

Skills Required: JavaScript, Windows/macOS programming, ML, AI

Potential Mentor(s): [Roman](https://github.com/roman-r-m), [Laurent](https://github.com/laurent22)

Expected size of project: 350 hours

## More info

- Make sure you read the [Joplin Google Summer of Code Introduction](https://github.com/joplin/gsoc/blob/main/readme.md)
- To build the application, please read [BUILD.md](https://github.com/laurent22/joplin/blob/dev/readme/dev/BUILD.md)
- And before creating a pull request, please read the [pull request guidelines](https://github.com/joplin/gsoc/blob/main/pull_request_guidelines.md)
