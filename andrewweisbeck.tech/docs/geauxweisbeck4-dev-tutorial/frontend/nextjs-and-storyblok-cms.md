---
sidebar_position: 2
---

# NextJS and Storyblok CMS Integration

NextJS and Storyblok CMS are the perfect choice for the second version of my professional website. There is a lot of advantages to content creation, as well as making APIs easier and creating awesome content that makes money.

My personal website is going to be a whole lot more impressive then the first time around. I am a much better developer and will actually implement a full stack solution. Refer to the [introduction section](/docs/geauxweisbeck4-dev-tutorial/geauxweisbeck4-dev-introduction) to get an overview of all the technology used.

Now, let's go ahead and get started on integrating Storyblok and Next JS!

## Setup Projects

To get started, we will first create a brand new Next.js application and then we will add Storyblok CMS:

```
$ npx create-next-app basic-nextjs

$ cd basic-nextjs

$ npm install @storyblok/react axios
```

To see what your app we created looks like run `npm run dev` and go to localhost:3000.

## Connect to Storyblok



## Fetching Data

## Setting Preview URL

## Adding new stories and dynamically rendering pages

To create a new story, go to the `Content` section in your space and click on the `Create New` button in the top right corner. Click on the `Story` option and a popup will appear. For the first story on my site, I created the About page, so I put in `About` under `Name` and `about` under `Slug`. Finally click on `Create` to add a new story and we will get a 404 error initially - that is because we are only fetching the published links and generating their pages. Choosing `Publish` will display a page with our layout.

Continue to do the same with the `Blog` and `Services` pages. They get loaded with the `[...slug].js file, which catches routes.

The right hand side of our stories contain an empty body with a plus button that allow us to add existing components to the page

### Adding Components

Add the `Teaser` component and fill in the `Name` field for it. When we fill in content, we will see changes in the visual editor. Once we hover over the right side, we'll see a similar plus button below the `Teaser`. Add a `Grid` component with three `Features as columns, similar to our `home` story. You can also add another `grid`.

## Create Dynamic Menus

We must start by creating a new content type component where our menu items can be stored. Start by going to Block Library and select + New Block

### Links and Resources

[Storyblok Next.js Ultimate Tutorial](https://www.storyblok.com/tp/nextjs-headless-cms-ultimate-tutorial)

[Stackblitz Demo](https://stackblitz.com/edit/nextjs-5-minutes)

[Next.js Technology Hub](https://storyblok.com/tc/nextjs)

[Storyblok React SDK](https://github.com/storyblok/storyblok-react)

[Next.js Documentation](https://nextjs.org/docs/)
