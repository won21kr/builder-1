## Builder.io custom design system example with React and storybook

> ✨ **Try it live [here](https://builder.io/fiddle/4b2e0a2e4b1a44a88a5e6f8c46cdfe7c)**!

In this example we show how to integrate react components with [Builder.io](https://builder.io). This is useful when you want to add the ability for your team to utilize custom components on the pages you build using the Builder editor, or even want to make it so people on your team can only build and edit your site's pages using your custom components.

The way it works is by utilizing Builder's [preview url feature](https://builder.io/c/docs/guides/preview-url). When you set the preview URL in the Builder editor to point to your site, Builder reads the custom components and settings you specify in your source code via the Builder React SDK and incorporates them into the Builder editor. 

The source code for the custom components used in this demo are [here](src/components), and you can see how they are registered with Builder by looking at the files that end in `*.builder.js` ([this is an example](https://github.com/BuilderIO/builder/blob/master/examples/react-design-system/src/components/ProductsList/ProductsList.builder.js)). The logic for adding components to the Builder editor menu can be found [here](https://github.com/BuilderIO/builder/blob/master/examples/react-design-system/src/builder-settings.js)


> 👉**Tip: want to limit page building to only your components? Try [components only mode](https://builder.io/c/docs/guides/components-only-mode)**


<img src="https://imgur.com/PJW3b4S.gif" alt="example" />

### Live Demo with Storybook

We also show how to intergrate Builder.io using [@builder.io/storybook](https://github.com/builderio/builder/tree/master/packages/storybook) within your storybook to give your users a playground where they can drag and drop your custom components and prototype something quick.

[Storybook Demo](https://builder-storybook.firebaseapp.com/)

<img src="https://user-images.githubusercontent.com/5093430/76154244-ebbe6480-608d-11ea-9dc9-08a59eda220e.gif" alt="storybook example" />


### To run the example Locally

- [Sign in or create an account](https://builder.io)
- Create a new page
- Clone and start the project:

```bash
git clone https://github.com/BuilderIO/builder.git
cd examples/react-design-system
npm install
```
To Run storybook
```
npm run storybook
```

To run the app
```
npm run start
```

- Now that you have the development server running on localhost, update the preview URL of the Builder.io entry you created to : `http://localhost:3000/home`

<img width="796" alt="Screen Shot 2020-02-18 at 9 48 51 AM" src="https://user-images.githubusercontent.com/5093430/74763082-f5457100-5233-11ea-870b-a1b17c7f99fe.png">

This will allow Builder to read in all your custom component logic and allow your team to edit and build using your components.

When you deploy this to a live or staging environment, you can change the preview URL for your model globally from [builder.io/models](https://builder.io/models) (see more about models [here](https://builder.io/c/docs/guides/getting-started-with-models) and preview urls [here](https://builder.io/c/docs/guides/preview-url))
