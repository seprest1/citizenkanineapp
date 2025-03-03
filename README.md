# Citizen Kanine
<div align="center">
<img src="https://user-images.githubusercontent.com/105940054/211120109-3efdd6b5-1deb-4b6f-81f3-4648a6e4516e.png" alt="dogs!" width="300" height="200"/>
<img src="https://i0.wp.com/thecitizenkanine.com/wp-content/uploads/2018/05/cropped-Logo_CitizenKanine_cropped.png?fit=953%2C499&ssl=1" alt="cklogo" width="300" height="200"/>
<img src="https://user-images.githubusercontent.com/105940054/211119141-bcce5ead-21e4-4f14-a9a3-a04b6951b08b.jpeg" alt="dogs!" width="300" height="200"/>
</div>



## Summary

[Citizen Kanine](https://thecitizenkanine.com/) is a dog walking business based in Minneapolis - where each morning 'Pack Leaders' embark on a route to pick up dogs from client homes for their daily walk. On a typical day, the business walks 36+ dogs in small groups around Lake Harriet rain or shine. 
 
Our goal was to provide a solution to Citizen Kanine that would streamline their workflow. Their current process involves manually scheduling both employees and clients (and their dogs), assigning dogs to specific routes for their dog-walkers or "Pack Leaders", and updating their books using various lists of client information each month.

Our design is a web-based application with two views, an admin dashboard and a mobile view for employees. The admin portal provides a centralized location for our client to manage employees, client information, client scheduling, as well as invoicing. This tool is estimated to save our client multiple hours a month on invoicing alone. 

The mobile view allows employees to keep track of their schedules, and manage the distribution of dogs on a daily basis, as well as efficiently checking in dogs walked each day. The daily data recorded by dog walkers (*whether dogs are checked in or no-shows*) is sent directly to a database table. This table is queried via the admin portal to create monthly invoices for each client. 

This project was a team effort -  built in its entirety over the course of two weeks as a part of [Prime Digital Academy](www.primeacademy.io).

### *My Contribution*

I, along with my classmate Blake Smith, spent the majority of my time working on the design and implementation of the front-end, as well as the mobile view. Our design philosophy was to create an application that was professional and playful, speaking to the nature of the business, while utilizing the company colors. I created the dashboard for load-balancing the routes of dogs, using ***React Beautiful DnD***. I also constructed the back-end for the map feature, which we were unable to complete within the timeframe, using ***Radar*** for geo-coding, ***Pigeon Maps*** and ***Map Tiler*** for the map iteslf. 

Visit our [demo version](https://citizenkanine.herokuapp.com/) using:  `username: admin | password: admin`.
The application has conditional rendering based on screen size, to visit the mobile view on a browser, use the developer tools to change the screen size. 

## Screenshots & Demo
<div align="center">
  <img width="600" alt="splash page" src="https://user-images.githubusercontent.com/105940054/211109777-47a0bd56-3eae-4479-995c-df500587b2c1.png">
  <img width="600" alt="client page" src="https://user-images.githubusercontent.com/105940054/211109766-2a32fa7b-ff84-41b2-8400-549a5c107b49.png">
  <img width="600" alt="client info" src="https://user-images.githubusercontent.com/105940054/211109795-0849c038-640c-4334-9b0d-d9b38356efb6.png">
  <img width="600" alt="invoice page" src="https://user-images.githubusercontent.com/105940054/211109775-dca4b656-8f22-4ce3-8a22-ac14ded9fcb0.png">
  <img width="600" alt="employee schedule" src="https://user-images.githubusercontent.com/105940054/211109816-34f3eab5-db8c-462b-801a-16bdfe86daa1.png">
  <div>
   <img width="300" alt="mobile routes" src="https://user-images.githubusercontent.com/105940054/211110054-61c7188a-dd57-4aaf-acba-73c048df59ad.png">
   <img width="300" alt="mobile routes checked in" src="https://user-images.githubusercontent.com/105940054/211111860-8d6e4941-cd60-4e32-bf82-d1cd60e2f592.png">
  </div>
<img src="https://media4.giphy.com/media/zTvyYZhNV8MzOxKvzt/giphy.gif">
 </div>




## Approach

_Duration: Two Week Sprint_

With this project being a much larger workload than previous projects in our experience, and the added layer of client involvement planning was integral to results. Before starting development we spent a week scoping the project, connecting with the client to clarify their needs,  and setting up a timeline. 

##### Wireframes
  
Through the sprint, our team met with the Client on multiple occasions to provide updates, and clarify questions. In order to remain on schedule, our group utilized a Kanban board to visualize tasks that were in-progress, completed, or blocked. This helped clarify which pieces of the puzzle still needed completion, and streamlined the team's workflow.

As a representation of the planning spent on this project - we have included the [scope document]((https://docs.google.com/document/d/1_sO_B9sY84xYKGdlWtzBYzdPIXpx9b63RNzQ3Ie6izc/)). This process involved spending time considering user flow, component structure, and design potential for the application. This experience also involved setting a timeline for certain features and was an interesting venture into estimating development time for a small team of developers.

## Getting Started

### Prerequisites

- React.js *(built on version 17.0.2)*
- API keys for [Cloudinary](https://www.maptiler.com) & [MapTiler](https://www.maptiler.com).

### Installation
Using your package manager - install the dependencies

```
$ ~ npm install
```
In your database manager - create a database named `citizen_kanine` use the provided database.sql file to create the necessary tables for this project. 
*(We have included optional dummy data for testing purposes)*

Populate dotEnv file with:

```
> SERVER_SESSION_SECRET= 'choose_a_secret_here'
> map_api_key= 'your_api_key'
> CLOUDINARY_NAME= 'your_api_name'
> CLOUDINARY_API_KEY= 'your_api_key'
> CLOUDINARY_API_SECRET= 'your_api_secret'
```
With your database set up - start the server.
```
$ ~ npm run server
```

With the server running - open another terminal window and start your client.

Navigate to http://localhost:3000 if the run client script doesn't automatically open the application.

```
$ ~ npm run client
```

Login: `username: admin | password: admin`.

### Built With:

*  [React.js](https://reactjs.org/docs/getting-started.html)
*  [Node.js](https://nodejs.org/en/docs/)
* [Material-UI](https://mui.com) - components and styling
* [React-beautiful-dnd](https://github.com/atlassian/react-beautiful-dnd) - Drag and Drop functionality for mobile view
* [Day.js](https://day.js.org) - Time Utility
* [SweetAlert](https://sweetalert.js.org) - Visual feedback for users
* [Passport](https://www.passportjs.org) - Secure Login & Account Management

*For a full list of dependencies - see the Package.json*

## Usage

  This application is meant to serve as a business management tool for Citizen Canine. It is meant to handle client, and employee scheduling - as well as client invoicing.  The next sections will walk you through the tools at your disposal in each view. 

### Desktop *(Admin Dashboard)*

 1. **Log In** - when logging in on a desktop using admin level credentials users will be brought to a desktop 'Splash Page'
 2. **Splash Page** - a Home Screen for the desktop experience, contains a notes section to help keep admin organized. Also includes a collapsible sidebar which allows for convenient site navigation.
 3. **Employee Management 'Pack Leaders'** - enter this view through the sidebar -  in this view admin is able to add/edit/delete employees, as well as modify and view their schedules.  Adding an employee will generate an account with their email as the username, and a temporary password.
 4. **Clients** -  enter this view through the sidebar - in this view admin can add/edit/delete clients as well as their dogs. There is also a search function to help access a specific client quickly. Also allows for schedule viewing and editing. 
 5. **Reports** -  enter this view through the sidebar - an invoicing tool for admins to select relevant data and export a CSV file to import into Quickbooks.
 6. **Account** - a form for admin to change their password.

### Mobile *(Employee View)*

 1. **Log In** - employees and admins can log in on a mobile device to access the mobile features. 
 2. **Splash Page** -  quick navigation page for relevant tools, as well as a bottom navigation bar to access these tools.

**Dogs in this section may contain 'flags' which tell the employee there may be a relevant note about the dog and its behavior.**

 3. **Routes / Route Select** - accessing routes through the provided navigation tools will lead users to a view showing the assigned dogs for a given day, and their default route distribution. **Admin** level users will have a button to access load balancing. Once routes are set for the day - users simply click their assigned route to view the details. 
 4. **Load Balancing** -  a tool for Admin level users to distribute dogs amongst their daily employees using a drag and drop interface. If a household has multiple dogs - they are grouped and have a matching background color. (Section contains flags)
 5. **Route Screen** -  once routes are set, and a user selects their assigned route on the route select page and is brought to a list view with tools for route management. Clicking on a line in the list of dogs will reveal the options available for a user. Here employees are able to mark a dog as 'checked in' or a 'no show', which will in turn update their list visually marking said dog off of the list. In this view, Admin level users are able to cancel a dog at no charge - in case they were accidentally still on the schedule for a given day. Clicking on a dog photo or avatar on the left side of the list will bring a user to Dog Details. (Section contains flags)
 6. **Dog Details** - this view shows relevant information for a specific dog and their client. Here is a centralized location for access protocols for client homes, notes on dog needs, emergency contact information, as well as photo upload for dog identification. (Section contains flags)
 7. **Account** - a form for users to change their password.

## Developer Notes

#### Quickbooks API/flexible invoice output

  Given the opportunity to revisit this project - we would be interested in exploring Quickbooks API integration especially for Client Data and Invoice Item sync so that any changes made app-side will reflect on Quickbooks.

  App does not allow customization of CSV output. Currently, dog walking history is formatted by server in invoice.router.js and sent to client. Invoice is itemized by invoice period (month), client, and service provided. Dog walking services are indexed in the "services" SQL table (database.SQL), and referenced by "id" in invoice.router.js.

  App currently determines service provided to customer based on number of days scheduled listed per client in "client_schedule" table AND number of dogs walked per day of service. Prices are currently fixed in the table. If Citizen Kanine needs to adjust their prices or services, a Quickbooks sync function could update the "service" table based on Quickbooks 'items' list. Depending on the type of changes, it would be important to preserve service "id" position in "services" table.

  Another possible solution is to add an updatable services menu, and to allow admin user to link customer directly to a 'base service' in on the 'client details' page. The advantage of these approaches would be A) allow admin user to interact with services list in the app and B) allow admin user to select 'friend and family' rate for a given customer.

  A third change to invoicing functionality would be to bypass CSV export and directly create invoices using Quickbooks API.

  The two hurdles with quickbooks integration are:
  1) setting up two-factor authentication with Citizen Kanine account.
  2) building a sandbox company with sample dataset and datastructure as close to the Citizen Kanine buisness account as possible

#### Mapping routes and dog location
  While we started exploring mapping for this project, it unfortunately did not fit into our timeline - this is a feature we think would be incredibly helpful for a visual of routes (for load balancing, and navigation). (Map API's / Providers listed below)

  some effort towards mapping routes has been made in the 'map' branch. In this branch:
  - "clients" table includes "lat" and "long" fields.
  - add new and update client routes automatically populates table with coorinate data based on address (MapTiler).
  - SQL queries in mobile.router need to updated to select "lat" and "long" for each client.
  
  Another area for exploration would be to attempt to develop step by step route directions for the employee - providing a streamlined pickup process for their morning. 

## Authors & Acknowledgement

Thanks to [Cloudinary](https://cloudinary.com) whose API supplied image upload capabilities for multiple parts of this application.

Thanks to the services that made the start of our Map display development possible: [Radar](https://radar.com), [MapTiler](https://www.maptiler.com) and [Pigeon Maps](https://pigeon-maps.js.org).

*Thanks to [Citizen Kanine](https://thecitizenkanine.com/) and Lisa Johnson for working with us and allowing us the opportunity to build something really cool.*

*Special thanks to [Prime Digital Academy](www.primeacademy.io) who equipped and helped us make this application a reality.*
  

  
