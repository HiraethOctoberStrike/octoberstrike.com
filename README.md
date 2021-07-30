# October Strike

## Get started

Clone the repository

```bash
git clone git@github.com:HiraethOctoberStrike/octoberstrike.com.git
```

Install the dependencies...

```bash
cd octoberstrike.com
npm install
```

...then start your dev server with  [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).

## Contribution Workflow

### Creating New Tasks

Tasks to be completed or issues that need fixing can be added from the [Issues](https://github.com/HiraethOctoberStrike/octoberstrike.com/issues) page. 

1. Click "New issue" to draft a new issue
2. Add a title and description
3. Select any appropriate **Labels** 
4. Select 'Dev Tasks' under **Projects**
5. "Submit new issue"

### Claiming a Task

Our [Dev Tasks](https://github.com/HiraethOctoberStrike/octoberstrike.com/projects/1) kanban board can be found on the [Projects](https://github.com/HiraethOctoberStrike/octoberstrike.com/projects) page.

1. Select a task from the "To do" column.
2. Assign yourself under **Assignees** and move the task to the "In progress" column
3. Create a new branch in your local environment to begin work `git checkout -b <your-descriptive-branch-name>`

### Finishing a Task

Once finished, present your changes for review and addition to the main branch from the [Pull Request](https://github.com/HiraethOctoberStrike/octoberstrike.com/pulls) page.

1. add and commit work to your local feature branch
2. push your branch to Github
3. Select "New Pull Request"
4. Select branches to compare: `base: main` <- `compare: <your-descriptive-branch-name>`
5. "Create Pull Request"
5. Link the original issue in the description: Add the text `closes #42` for example if the PR completes the requirements of issue #42
6. Select a few **Reviewers** and wait for review.
7. Make necessary revisions, add, commit, and push. You can either request a second review or if confident, merge the PR and delete your branch.

> That's it! If the issue was linked correctly both the Issue and PR tasks should be automatically moved to the "Done" column in the kanban board.


## New to Svelte?

Check out the [Svelte Tutorial](https://svelte.dev/tutorial/basics)

### Our Component Library

#### Button

|Prop Name |Type |Required |Default |Description |
--- | --- | --- | --- | ---
|text|string|yes|--|text displayed in button
|href|string|yes|--|url that button redirects to
|secondary|bool|no|false|if true, restyles with secondary colors
|tertiary|bool|no|false|if true, restyles with tertiary colors
|large|bool|no|false|if true, resizes to large dimensions
|smallText|bool|no|false|if true, restyles with small text

##### Button with default attributes
```html
  <Button text='STRIKE WITH US' url='/strike-with-us' />
```

##### Button with optional attributes
```html
  <Button text='STRIKE WITH US' url='/strike-with-us' secondary small />
```

## Deploying to the web (For future deployment decisions)

### With [Vercel](https://vercel.com)

Install `vercel` if you haven't already:

```bash
npm install -g vercel
```

Then, from within your project folder:

```bash
cd public
vercel deploy --name my-project
```

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
