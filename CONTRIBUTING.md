# Contributing 

## 🧩 New components 

The different components are showcased in the main page (`pages/index.vue`), in separate cards. To add a new card for a new library component, you need to:
- Create a branch from `main` with the name of the new component.
- Create the main content of the new card as a separate component in the `components` folder (let's call this the "content component"). You put there whatever you consider necessary to showcase the component.
- Import the "content component" in the `index.vue` file.
- Add the details of the new card in the `components` array in the `index.vue` file. The details are:
    - `title`: title of the card (usually the name of the component or a variation of it).
    - `component`: the "content component" you imported.
    - `documentationLink` (optional): link to the documentation of the component.
- Create a pull request to merge the new branch into `main`.

## ✏️ Any other modification 
- Create a branch from `main` with the name of the modification.
- Make the changes you consider necessary.
- Create a pull request to merge the new branch into `main`.

## 🚀 Deployment

Your changes will be add to the demo site automatically once the pull request is merged (may take a few minutes).

