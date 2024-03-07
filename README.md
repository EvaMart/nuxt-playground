# OEB Visualizations Demo

Welcome to the official demonstration site for our Vue-based Web Components Library! This site serves as a showcase for our collection of high-quality, reusable web components designed to accelerate and enhance the web development of the [OpenEBnch](https://openebench.bsc.es) site. Each component is built with Vue, ensuring seamless integration and dynamic interactivity.
Features

Our library offers a wide range of features designed to meet modern web development needs:

- **Responsive Design**: Ensures your applications look great on any device.
- **Accessibility**: Components are built with accessibility in mind, promoting inclusivity.
- **Customization**: Easily themed and customized to fit your requirements.


## Installation and Usage

To run the demo site locally:

- Clone the repository: `git clone https://github.com/inab/oeb-visualizations-demo`  
- Install dependencies: `npm install`
- Serve the site locally: `npm run dev`
- Navigate to http://localhost:3000 to view the demo site.

## Development 

This site is built with [Nuxt.js](https://nuxtjs.org/), a Vue.js framework. The main page is located in `pages/index.vue`, and the different components are showcased in separate cards. The components are imported from the `oeb-visualizations` library, and the details of each card are defined in the `components` array in the `index.vue` file.

### Steps to Introduce New Cards for New Components

If you've crafted a new component within the `oeb-visualizations` library and wish to feature it on the site, adhere to the steps below:

- Start by generating the main content for the new card. Do this by creating a separate component within the `components` folder (referred to as the "content component"). This component should contain all necessary elements to effectively demonstrate the capabilities of the new library component.
- Next, ensure the "content component" is imported into the `index.vue` file.
- Proceed to incorporate the new card's details into the `components` array in the `index.vue` file. These details should include:
    - `title`: The name of the card, typically mirroring the component's name or a close variant.
    - `id`: A unique identifier for the card, generally the component's name in lowercase, without spaces.
    - `component`: Reference to the "content component" you've imported.
    - `documentationLink` (optional): A hyperlink directing users to the component's documentation. Usually of the form `https://inab.github.io/oeb-visualizations/#/component-name`.


Please, make sure to read the [CONTRIBUTION guidelines](./CONTRIBUTING.md) before adding new components.

## Deployment

The demo page is automatically deployed to GitHub Pages when changes are merged into the `main` branch. The deployment is handled by GitHub Actions, which runs the `deploy.yml` workflow to build and deploy the site.

## Components technical Documentation

Detailed technical documentation for each component is readily accessible from the demo site as links. Visit our [documentation section](https://inab.github.io/oeb-visualizations/) for more information (in-depth explanations, API details, and usage guidelines).

## Contributing

If you would like to add a new component or make any other modifications, please follow the guidelines in the [CONTRIBUTING.md](./CONTRIBUTING.md) file.

## Getting Feedback or Help 

If you need help or want to discuss something, you can open an [issue](https://github.com/inab/oeb-visualizations-demo/issues/new) in this repository.