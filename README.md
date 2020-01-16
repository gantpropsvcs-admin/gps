# Gant Professional Services

This project is for a business site.  The project is React for development, and GatsbyJS which compiles MD files into a static site for speed and performance.  For the business user, there is a headless CMS (Netlify) that allows for WYSIWYG editing of MD files.

All pages are compiled and stored into Git itself.  Ultimately, the DNS for gantprofessionalservices.com will be pointed to Git as a host.

This project is in process and incomplete, but I'm happy to discuss any aspects to of it.

## GatsbyJS

Gatsby is a fantastic framework on top of React that creates very fast sites.  All dynamic data is gathered at build time, queries are processed and the data transformed into static files.  The query engine internally is GraphQL, which in Gatsby can accept any number of data sources, in this case, MD files.  Frontmatter is collected by the query engine at build time.  Gatsby includes a query interface that exposes all datasources in a convenient IDE for query development.  

## Netlify

Netlify is a headless CMS that provides content editing and creation only.  There is no front end for content delivery.  What makes Netlify interesting is that it embraces CICD principles.  Netlify monitors the Git repo and does a fetch and spawns a container that reconstitutes the build environment, performing all of the npm and Gatsby commands to build the site and then store the output back into Git.  This allows for both the developer changes that are committed and the business user edits in Netlify to always be published and live.  Images can be processed from 3rd party cloud hosts, since Git isn't great for image storage due to size.
