# Calendar Tools: setup

You'll host the files for free on GitHub Pages, then point Outlook at them. Plan on about 15 minutes.

## 1. Put the files online (GitHub Pages)

1. Sign in at github.com (or create a free account).
2. Click **New repository**. Name it exactly `outlook-calendar-tools` and set it to **Public**. Free GitHub Pages requires a public repo. Your people list is *not* stored in these files, so nothing personal is published.
3. On the new repo page, click **uploading an existing file**. Drag in `taskpane.html`, `index.html`, `README.md`, and the `assets` folder. Click **Commit changes**.
4. Go to **Settings → Pages**. Under "Branch," pick `main` and `/ (root)`, then **Save**.
5. Wait a minute, then open `https://YOUR-GITHUB-USERNAME.github.io/outlook-calendar-tools/taskpane.html` in a browser. A mostly blank page means it worked.

Don't upload `manifest.xml` to GitHub. It stays on your computer.

## 2. Edit the manifest

Open `manifest.xml` in Notepad. Use **Edit → Replace**, replace `YOUR-GITHUB-USERNAME` with your GitHub username, then click **Replace All** (9 replacements). Save.

## 3. Install it in Outlook

1. In new Outlook or Outlook on the web, go to **https://aka.ms/olksideload**, or use **Apps → Add apps**.
2. Choose **My add-ins**. At the bottom under **Custom Addins**, click **Add a custom add-in → Add from File**, and pick `manifest.xml`.
3. Accept the warning. It's your own add-in.

If "Add a custom add-in" is missing, your IT has turned off the *My Custom Apps* role. Ask them to enable it for your account.

## 4. Use it

1. In your calendar, click or drag the time slot to open a new event.
2. Click **Calendar Tools** in the event's toolbar. It may be under **Apps** or the **…** menu. Click the pin icon to keep the pane open.
3. The first time, open **Set up**. Enter your first name and add the people you do 1:1s with.

## Limits compared with your VBA

- Add-ins can't set **Show as** (Free / Away / Working elsewhere) or turn off the **reminder**. The pane tells you when to change these by hand. Doing them automatically needs Microsoft Graph, which is a later step.
- Events open as a form instead of saving silently. Review the form, then click **Save** or **Send**.
- The categories "Admin" and "Team" must already exist in your category list.
- The task-to-appointment macro and the two report macros aren't included. They need Graph.

## Updating

Edit `taskpane.html` on GitHub. Outlook picks up the change next time the pane opens, though it can take a few minutes for caching. You only re-install if `manifest.xml` changes.
