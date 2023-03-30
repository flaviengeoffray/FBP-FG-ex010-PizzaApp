# FBP-FG-ex010-PizzaApp
Flavien Geoffray - 5999222008
<br/>
Framework Based Programming

## Session 1
This session is about building the main page of a pizza store. The app will allow users to order pizzas, customize them, and track order deliveries.<br/>
The home page component is implemented as a single component that currently displays a simple home page. The next step was to display the list of available pizza specials. A @code block with a list field is added to the Index.razor page to keep track of available specials. An HttpClient is injected into the Index component using the @inject directive to retrieve the list of pizza specials.<br/>
A markup has been then added to the Index component to list the pizza specials. The layout component for the pizza store app is defined in Shared/MainLayout.razor, which inherits from LayoutComponentBase. The MainLayout component is then updated to define a top bar with a branding logo and a nav link for the home page.<br/>

![1-001](https://user-images.githubusercontent.com/97790963/228799163-f2ac6b2b-20e4-4d38-9e87-07d72c17d666.png)

## Session 2
In this session, we are adding functionality to enable users to customize their pizza orders. We begin by adding an event handler to listen for clicks on pizza specials and show a pizza customization dialog. We also add some additional fields to the @code block to track the pizza being customized and whether the pizza customization dialog is visible.<br/>
Next, we create a new component called ConfigurePizzaDialog.razor that lets users specify the size and toppings for their pizza. We add a slider to the dialog to allow users to specify the pizza size and use data binding to update the pizza size stored in the configuringPizza object when the slider is moved.<br/>
Finally, we add buttons to the dialog to let users cancel or add the pizza to their order. We also update the Pages/Index.razor file to show the ConfigurePizzaDialog when a pizza special is selected, and add functionality to close the dialog when the user clicks the cancel button.<br/>


![2-001](https://user-images.githubusercontent.com/97790963/228799178-99ba2fe8-4fce-4b80-9a1b-91661ac91df5.png)
![2-002](https://user-images.githubusercontent.com/97790963/228799213-66ae8a6f-d528-4986-b1a8-7ed4bf586f62.png)
![2-003](https://user-images.githubusercontent.com/97790963/228799224-f4ea8e16-f70b-4d5d-9d34-248c4b8622ef.png)
![2-004](https://user-images.githubusercontent.com/97790963/228799246-c37b317c-9fb7-41d6-a6e7-4e36e534fe1a.png)

## Session 3
Session 3 was about updating orders: We created an Orders component to manage orders and orders status.
The Page "My Orders" displays the recap of the order. We also added a button to track the order.
All is done automatically.<br/>
 
https://user-images.githubusercontent.com/97790963/228808496-dab59d5e-4042-4917-b8eb-9b76774c4d56.mp4


## Session 4
Session 4 was about fixing a problem. We used the AppState pattern. This object can outlive the components and hold on to state even when the UI changes. The pattern leads to greater separation between presentation (components) and business logic.<br/>
The AppState pattern solves the problem of state management in Blazor applications by moving shared state outside of components and into the AppState. Components call methods on the AppState to trigger a state change. EventCallback takes care of dispatching change notifications to the appropriate components. This approach prevents state from being lost when a user navigates between pages in the application.<br/>


https://user-images.githubusercontent.com/97790963/228799324-6b28d48f-6007-4564-8812-bd92558b604a.mp4


## Session 5
In the session 5 we added a checkout page to a pizza ordering app in Blazor. The steps involve creating a new page component for the checkout, capturing the delivery address using a reusable AddressEditor component, and adding server-side and client-side validation to ensure a valid address is entered before an order can be submitted.

https://user-images.githubusercontent.com/97790963/228799326-7a586df6-bca0-4e63-89d5-b3d4036197f5.mp4


## Session 6
The Session 6 was similar as session 5, we created register and login page.

https://user-images.githubusercontent.com/97790963/228799351-31371058-28cd-45a2-86ea-d1b1ae30370c.mp4

## Session 7

In this session, we added a real-time map to the order status page for tracking pizza delivery. The Map component renders a div with a unique ID and then calls the deliveryMap.showOrUpdate function to display the map with specified markers passed to the Map component.<br/>

We also added a confirm prompt to verify if the user really wants to remove the pizza from the order when the Remove button is clicked. A RemovePizza method is also added that calls the Confirm method to prompt the user before removing the pizza from the order.<br/>


![7-001](https://user-images.githubusercontent.com/97790963/228800080-12112134-0eb1-4c09-b752-544217a4f83c.png)
![7-002](https://user-images.githubusercontent.com/97790963/228800097-de312ec9-772f-4e9a-9416-eff8c2e03b6d.png)

## Session 8
In this session we refactored some of the original components and make them more reusable. We also created a separate library project as a home for the new components.

## Session 9

This session add Progressive Web App (PWA) features to a Blazor web application. PWA features include installing the app into the OS taskbar or home screen, working offline, and receiving push notifications. To enable these features, a service worker is required, which is a small file that provides event handlers that the browser can invoke outside of the application's context.

https://user-images.githubusercontent.com/97790963/228799451-1f1f5360-c939-4551-a281-93e975d3d7f5.mp4


