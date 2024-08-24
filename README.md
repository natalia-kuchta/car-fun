# CarFun Project



CarFun is a dynamic web application built using the Nuxt.js framework and styled with Tailwind CSS. The primary goal of this project is to allow users
to browse car listings, filter them by city and brand, and display detailed information about each car.


## Key Features of the Project:

```
Dynamic Pages: The pages are dynamically generated based on URL data such as car name, ID, city, and brand.

Interactive Components: The application uses Vue.js components to render interactive elements like car cards, search forms, and more.

Reusable Layouts: The structure of the application is based on reusable layouts that ensure consistent appearance across different pages.

SEO: The application takes care of search engine optimization by dynamically generating meta tags and page titles.
```


## Project Structure and File Functions:


 ### Layouts (layouts/custom.vue)
```
What it does: Layouts define the general structure of the page, such as the header, footer, and other shared elements. The custom.vue layout in the

CarFun project ensures a consistent page appearance while allowing unique elements to be added to individual pages. Each page using this layout will

have a defined structure with appropriate components.

How it works: Nuxt.js automatically uses layouts to render pages. Pages can define which layout they want to use to ensure the correct structure.
```



### car.vue in the [city] directory
```
What it does: The car.vue file handles displaying cars in a specific city. It is a dynamic page that shows a list of available cars in the chosen city.

How it works: It uses dynamic URL parameters (e.g., city) and components like CarSideBar, which allows filtering cars. The main content is loaded

dynamically, depending on the selected city.
```


### [[make]].vue in the city/[city]/car directory
```
What it does: This page displays a list of cars of a specific brand in a given city. It is a more detailed subpage within a specific city.

How it works: The CarCard component renders individual car cards for the selected brand. The page uses dynamic URL parameters to filter cars by city and brand.
```


 ### [name]-[id].vue in the car directory
```
What it does: This is a detailed page for a specific car. It displays all the essential information about the selected model, such as specifications,description, and contact details.

How it works: It uses URL parameters such as car name and ID to retrieve and display the relevant data. The page utilizes components like

CarDetailHeros, CarDetailAttributes, and CarDetailDescrisption to present the car's details.
```


 ### index.vue in the city directory
```
What it does: This is the main page of the car section. It often contains a hero section and a search form.

How it works: It allows users to search for cars by city. The CarHero component displays a background with a header and a search bar.
```


 ### Path city/[city]/car
```
What it does: This is a dynamic URL path that generates subpages for cars in specific cities. For example, /city/Toronto/car will display a list of cars available in Toronto.

How it works: Nuxt.js dynamically generates these pages based on URL parameters. Inside this path, there are further dynamic subpages, such as /city/Toronto/car/Toyota, which filter cars by brand.
```

### How Does Nuxt.js Create Dynamic Pages?

Nuxt.js uses a file-based routing system to automatically create dynamic routes. Each file in the pages directory is automatically converted into a
route, simplifying the process of creating dynamic pages. As a result, the CarFun application can dynamically generate pages based on parameters such as city, car brand, or specific car ID.


### Tailwind CSS

In the CarFun project, styling is implemented using Tailwind CSS, allowing for the quick and easy implementation of responsive and modern user interfaces.

### Screenshots

![Screenshot from 2024-08-24 19-29-17](https://github.com/user-attachments/assets/d05717f6-32ca-4772-bcfa-08fafd5754ba)

![Page2](https://github.com/user-attachments/assets/22fa1441-fc09-44a0-9550-0b44790f639e)

![ContactPage](https://github.com/user-attachments/assets/6a76139e-be1b-45b3-a2ec-7cb97f959408)


