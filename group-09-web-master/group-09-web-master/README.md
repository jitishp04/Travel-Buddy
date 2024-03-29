## Teaser

![Teaser](./images/teaser.png)

## Entity-Relationship (ER) Diagram

![ER Diagram](./images/ERdiagram_TravelBuddy.jpg)

## Project Structure

| File                                                 | Purpose                           | What you do?                              |
| ---------------------------------------------------- | --------------------------------- | ----------------------------------------- |
| `server/`                                            | Backend server code               | All your server code                      |
| [server/README.md](server/README.md)                 | Everything about the server       | **READ ME** carefully!                    |
| `client/`                                            | Frontend client code              | All your client code                      |
| [client/README.md](client/README.md)                 | Everything about the client       | **READ ME** carefully!                    |
| [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md)             | Free online production deployment | Deploy your app online in production mode |
| [docs/LOCAL_DEPLOYMENT.md](docs/LOCAL_DEPLOYMENT.md) | Local production deployment       | Deploy your app local in production mode  |

## Requirements

The version numbers in brackets indicate the tested versions but feel free to use more recent versions.
You can also use alternative tools if you know how to configure them (e.g., Firefox instead of Chrome).

- [Git](https://git-scm.com/) (v2) => [installation instructions](https://www.atlassian.com/git/tutorials/install-git)
  - [Add your Git username and set your email](https://docs.gitlab.com/ce/gitlab-basics/start-using-git.html#add-your-git-username-and-set-your-email)
    - `git config --global user.name "YOUR_USERNAME"` => check `git config --global user.name`
    - `git config --global user.email "email@example.com"` => check `git config --global user.email`
  - > **Windows users**: We recommend to use the [Git Bash](https://www.atlassian.com/git/tutorials/git-bash) shell from your Git installation or the Bash shell from the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to run all shell commands for this project.
- [Chalmers GitLab](https://git.chalmers.se/) => Login with your **Chalmers CID** choosing "Sign in with" **Chalmers Login**. (contact [support@chalmers.se](mailto:support@chalmers.se) if you don't have one)
  - DIT342 course group: https://git.chalmers.se/courses/dit342
  - [Setup SSH key with Gitlab](https://docs.gitlab.com/ee/ssh/)
    - Create an SSH key pair `ssh-keygen -t ed25519 -C "email@example.com"` (skip if you already have one)
    - Add your public SSH key to your Gitlab profile under https://git.chalmers.se/profile/keys
    - Make sure the email you use to commit is registered under https://git.chalmers.se/profile/emails
  - Checkout the [Backend-Frontend](https://git.chalmers.se/courses/dit342/group-00-web) template `git clone git@git.chalmers.se:courses/dit342/2023/group-09-web.git`
- [Server Requirements](./server/README.md#Requirements)
- [Client Requirements](./client/README.md#Requirements)
- Google and unsplash API keys

## Getting started

```bash
# Clone repo then:
# Setup backend
cd server && npm install
npm run dev

# Setup frontend
cd client && npm install
npm run serve
```

> Check out the detailed instructions for [backend](./server/README.md) and [frontend](./client/README.md).

## Visual Studio Code (VSCode)

Open the `server` and `client` in separate VSCode workspaces or open the combined [backend-frontend.code-workspace](./backend-frontend.code-workspace). Otherwise, workspace-specific settings don't work properly.

## System Definition (MS0)

### Purpose

The travel companion is an app that helps you plan, track your travels, and create lifetime memories of each trip. The web based app creates an all in one package of important features to make your trip smooth sailing and unforgettable. You can list your visited destinations, create packing and bucket lists, and plan your trips and expenses.

### Features

- Destination map and planner (chaining to a path to plan roundtrip: "travel via")
- Journal/notes: 
  - Text-based
  - (Not implemented: *Images*)
- Checklists:
  - Packing lists
  - (Not implemented: *Bucket lists:*
    - *Destinations*
    - *Activities*)
  - (Not implemented: *Expenses lists:*
    - *Travel expenses, including calculation of sum and currency converter*)
- (Not implemented: *Reviews of destinations and activities*)

### Pages

- Main page containing a map for searching and/or saving possible destinations and activities. Clicking on the map brings up a menu containing options like “Save location” or "Create journal entry"
- Left Sidebar Menu containing entries for Journal, Locations, Activities, Checklists, preferences etc
- Right Sidebar Menu for additional details and options for list and note entries; pops up when entry is selected for creation/editing
- Pages for Journals, Checklists, Locations and an overview of all entries
