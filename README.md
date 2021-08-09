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
> if you get an error like: "command not found: npm", you might need to install [NodeJS](https://nodejs.org/en/download/)

...then start your dev server with  [Rollup](https://rollupjs.org):

```bash
npm run dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

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
5. Link the original issue in the description: Add the issue number after `closes #` e.g. `closes #42`
6. Select a `OppNHeimer as a **Reviewer**.
7. Make necessary revisions, add, commit, re-push, and request review again if changes are requested.

> That's it! If the issue was linked correctly both the Issue and PR tasks should be automatically moved to the "Done" column in the kanban board.

## Deploying to the web 

[Netlify](app.netlify.com) is our CI/CD service which allows us to automate deployments.

We have two deployed version of the site, `staging` and `production`.

### Staging

Staging is for internal review before new changes to the site are deployed to `production`.

URL: [labor-movement-x-staging.netlify.app](labor-movement-x-staging.netlify.app)

#### Deployment 

All PRs to the `main` branch will be automatically deployed to staging. **All changes to staging must be made via a pull request from `<your-feature-branch` to `main`.** 

The pull request can be merged **AFTER** review.

### Production

Production is our official external facing site which is viewed at [labormovementx.org](labormovementx.org).

#### Deployment

Changes to the `production` branch will be automatically deployed to the production site. **All changes to production must be made via a pull request from `main` to `production`.** 

The pull request can be merged **AFTER** approval by design and PR.

## New to Svelte?

Check out the [Svelte Tutorial](https://svelte.dev/tutorial/basics)

### Our Component Library

#### Button

Standard button with alternate styles for internal and external links

|Prop Name |Type |Required |Default |Description |
--- | --- | --- | --- | ---
|text|string|yes|--|text displayed in button
|href|string|yes|--|url that button redirects to
|secondary|bool|no|false|if true, restyles with secondary colors
|tertiary|bool|no|false|if true, restyles with tertiary colors
|large|bool|no|false|if true, resizes to large dimensions
|smallText|bool|no|false|if true, restyles with small text
|external|bool|no|false|if true, opens url in new tab

##### Button with default attributes
```html
  <Card text='STRIKE WITH US' url='/strike-with-us' />
```

##### Button with optional attributes
```html
  <Button text='STRIKE WITH US' url='/strike-with-us' secondary small />
```

#### Card

Card with a title on a color background and body

|Prop Name |Type |Required |Default |Description |
--- | --- | --- | --- | ---
|title|string|yes|--|card title text
|red|bool|no|false|if true, restyles with red title
|navy|bool|no|false|if true, restyles with navy title
|peach|bool|no|false|if true, restyles with peach title
|small|bool|no|false|if true, configures for narrow dimensions

##### Card with default attributes
```html
  <Card title='Write Your State Officials' >
    <!-- content of card goes inside -->
  </card>
```

##### Button with optional attributes
```html
  <Card title='Write Your State Officials' peach small>
    <!-- content of card goes inside -->
  </Card>
```

#### SocialLinks

Component with linked icons to social media pages

|Prop Name |Type |Required |Default |Description |
--- | --- | --- | --- | ---
|onDark|bool|no|false|if true, restyles for dark background

##### SocialLinks with default attributes
```html
  <SocialLinks />
```

##### SocialLinks with optional attributes
```html
  <SocialLinks onDark/>
```

#### PageTitle

Styling for h1 element at top of most pages with white background.

|Prop Name |Type |Required |Default |Description |
--- | --- | --- | --- | ---
|text|string|yes|--|content of the page title

##### PageTitle with default attributes
```html
  <PageTitle text='Labor Movement X' />
```

#### Section

Provides a set of standard margins for page sections

|Prop Name |Type |Required |Default |Description |
--- | --- | --- | --- | ---
|narrow|bool|no|false|if true, restyles with narrow margin
|narrower|bool|no|false|if true, restyles with a narrower margin
|narrowest|bool|no|false|if true, restyles with even narrower margins
|demands|bool|no|false|if true, restyles with a custom margins for demands section
|navy|bool|no|false|if true, restyles with navy background
|red|bool|no|false|if true, restyles with red background
|lightBlue|bool|no|false|if true, restyles with lightBlue background

##### Section with default attributes
```html
  <Section />
```

##### Section with optional attributes
```html
  <Section narrower red/>
```