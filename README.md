In this project I have  build a **Nxt Trendz - Specific Product Details** by applying the concepts I have learned in react.

### Refer to the image below:

<br/>
<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-output-v0.gif" alt="product details output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>
<br/>

#### Design Files

<details>
<summary>Click to view the Design Files</summary>

- [Extra Small (Size < 576px) and Small (Size >= 576px) - Success](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-success-sm-output-v3.png)
- [Extra Small (Size < 576px) and Small (Size >= 576px) - Failure](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-error-sm-output.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Success](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-success-lg-output-v3.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Failure](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-error-lg-output.png)

</details>

### Project Set Up Instructions

<details>
<summary>Click to view the Set Up Instructions</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Project Completion functionalities

<details>
<summary>Click to view the Functionality added</summary>

#### Add Functionality

The app have the following functionalities

- When an _authenticated user_ clicks on a product in the Products Route, then the page will be navigated to **Product Item Details** route.
- When the **Product Item Details** route is opened,
  - An HTTP GET request will made to productDetailsApiUrl with `product id` as path parameter.
  - **_loader_** will be displayed while the HTTP request is fetching the data
  - After the HTTP request is successful, the response received will be displayed.
  - The quantity of the product will initially be 1.
  - The quantity of the product will be incremented by 1 when the plus icon is clicked.
  - The quantity of the product will be decremented by 1 when the minus icon is clicked.
  - The list of similar products will be displayed.
- When the **Product Item Details** route is opened, if the response received in the HTTP GET request returns the status as `404`, then the [Failure view](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-error-lg-output.png) will be displayed.
- When the **Continue Shopping** button in the [Failure view](https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-error-lg-output.png) is clicked, the page will be navigated to Products Route.
- When an _unauthenticated user_ tries to access the **Product Item Details** route, the page will be navigated to Login Route

</details>

<details>
<summary>Click to view the Example response</summary>

- The example response received from request to the **productDetailsApiUrl** will be

  ```example
    {
        "id":16,
        "image_url":"https://assets.ccbp.in/frontend/react-js/ecommerce/cloths-long-fork.png",
        "title":"Embroidered Net Gown","price":62990,"description":"An Embroidered Net Gown is the clothing worn by a bride during a wedding ceremony. It enhances your beauty wearing this vibrant, gorgeous, and beautiful Wedding Gown. Find your dream wedding dress today. It features foldable, one hoop steel, two layers of tulles, and is elastic in the waist part. ",
        "brand":"Manyavar",
        "total_reviews":879,
        "rating":3,
        "availability":"In Stock",
        "similar_products":[
            {
                "id":1,
                "image_url":"https://assets.ccbp.in/frontend/react-js/ecommerce/clothes-cap.png",
                "title":"Wide Bowknot Hat",
                "style":"Wide Bowknot Hat for Women and Girls (Multicolor)",
                "price":288,
                "description":"This Summer's perfect White Wide Brim Straw Beach hat is perfect for a hot day. It has the Floppy Style which gives you good coverage from the sun's hot rays and is sure to make the right style statement. It is made of high-quality & skin-friendly paper straw material and lightweight. ",
                "brand":"MAJIK",
                "total_reviews":245,
                "rating":3.6,
                "availability":"In Stock"
            },
            ...
        ]
    }
  ```

</details>





> #### Note
>
> <details open>
> <summary>Click to view Note Points</summary>
>
> **The following HTML attributes are required for the HTML for the tests to pass**
>
> - `Home` route will consist of "/" in URL path
> - `Login` route will consist of "/login" in URL path
> - `Products` route will consist of "/products" in URL path
> - `Product Item Details` route will consist of "/products/:id" in URL path
> - `Cart` route will consist of "/cart" in URL path
> - No need to use the `BrowserRouter` in `App.js` as I have already included in `index.js`
>
> - Prime User credentials
>
>   ```
>    username: rahul
>    password: rahul@2021
>   ```
>
> - Non-Prime User credentials
>
>   ```
>    username: raja
>    password: raja@2021
>   ```
>
> 
>
> 

### Resources

<details>
<summary>Data fetch URLs</summary>

#### Data Fetch URLs

- [https://apis.ccbp.in/products/:id](https://apis.ccbp.in/products/:id)

</details>

<details>
<summary>Image URLs</summary>

#### Images

- [https://assets.ccbp.in/frontend/react-js/star-img.png](https://assets.ccbp.in/frontend/react-js/star-img.png)
- [https://assets.ccbp.in/frontend/react-js/nxt-trendz-error-view-img.png](https://assets.ccbp.in/frontend/react-js/nxt-trendz-error-view-img.png) alt should be **error view**

</details>

<details>
<summary>Colors</summary>

#### Colors

<div style="background-color: #12022f; width: 150px; padding: 10px; color: white">Hex: #12022f</div>
<div style="background-color: #616e7c; width: 150px; padding: 10px; color: white">Hex: #616e7c</div>
<div style="background-color: #171f46; width: 150px; padding: 10px; color: white">Hex: #171f46</div>
<div style="background-color: #cbced2; width: 150px; padding: 10px; color: black">Hex: #cbced2</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #3b82f6; width: 150px; padding: 10px; color: white">Hex: #3b82f6</div>
<div style="background-color: #1e293b; width: 150px; padding: 10px; color: white">Hex: #1e293b</div>
<div style="background-color: #475569; width: 150px; padding: 10px; color: white">Hex: #475569</div>

<br/>
</details>

#### Font-families

- Roboto


