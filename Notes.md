Feb 5th - 14:05 - NextJs 14
https://github.com/mschwarzmueller/nextjs-complete-guide-course-resources

a fullstack react framework

- handles route setup & config
- handles req & res
- handles data fetching and submission

two approaches for building nextJs app : Pages router, app router

in react search engine crawlers don't see the page content when they first visit them

name of the component does not matter inside page.jsx file name does

- Routing, Pages & components
- Fetching & sending data
- Styling, Images & Metadat

  it's running on server can be validated by that console logs will be shown in terminals.

redirecting to diff page with anchor tag has a flow it refreshes the page
<a></a> - gets us out of single page application so,
use special component Link from next/link

inside app icon.png used as fat icon shown in tab header. also reserved keywork

[project-structure](https://nextjs.org/docs/app/getting-started/project-structure)
@ in next refers to Root project
we can place components folder out of app directory or add \_ as prefix to ignore for routing

Dynamic routes with squARE BRACKETS AND PASSING identifier in it.

named route/folder have precedense over dynamic names.
imported png as stored as onject so have to access it's src proprty which contains path, but next's Image does'nt require it

https://nextjs.org/docs/app/getting-started/css

in react we're using client components out of the box

in next by default they are react server component,

- Using client components Efficiently.
  usePathName hook gives currently active path.

add 'use client' far down to component tree as possible.
we can create a smaller component that uses client side rendering.

Images with unknown Dimentions
fill prop to fill th available space

setup basic DataBase:
npm install better-sqlite3
this package will allow us to work with sqlite database
which can be used locally without setting up any extra DB

initdb will create existing Db if exists otherwise creates new, and contains dummy data.
than run node initdb.js
and we gets sqlite db

Fetching data by Leveraging NextJS & Fullstack capabilities.

we don't need to use useEffect and fetch, we can directly reach out to database.
and write that in lib dir.

.run() is used to insert/change data
.all() is used to fetch data, all rows
and .get() for single row

because of async wrapped to func it will return promise, and we can also use async in react components as well now in next

next js performs aggressive cashing under the hood, to be presice it cashes any page that we visit including data of that page.
also, it cashes even more aggressively when running the website in production mode.

- Adding a loading page
- after clicking to meals only after 5sec i'm redirected to that page, so
- add loading.js file (it applies to all sibling + nested pages and layouts)
- loading.js is shown as fallback untill data is there.

Using Suspense & Streamed responses for granular Loading State mngmnt.

- using React's suspense to load certain data, and showing fallback

Handling Errors:
error.js file - must be a client component

for invalid path
not-found.js

The dangerouslySetInnerHTML property in a React application is the equivalent of the innerHTML attribute in the browser DOM. In vanilla JavasScript, innerHTML is a property of DOM elements that allows you to get or set the HTML content inside an element. It’s a part of the standard DOM API, not specific to React.

dangerouslySetInnerHTML is React’s replacement for using innerHTML. dangerouslySetInnerHTML is a property that you can use on HTML elements in a React application to programmatically set their content. Instead of using a selector to grab the HTML element and then setting its innerHTML, you can use this property directly on the element.

When dangerouslySetInnerHTML is used, React also knows that the contents of that specific element are dynamic, and, for the children of that node, it simply skips the comparison against the virtual DOM to gain some extra performance.

As the name of the property suggests, it can be dangerous to use dangerouslySetInnerHTML because it makes your code vulnerable to cross-site scripting (XSS) attacks. This can become an especially big issue if you are fetching data from a third-party source or rendering content submitted by users.

special func - notFound() - shows closest not-found/error page.
