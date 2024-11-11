# UI and Data Structure

## DataStructure

This folder contains 5 subfolders, each focused on a different subject. In each folder, you'll find one or more designs.

**The goal is to create a data structure that represents the content shown in these designs.**

_For instance, in the SinglePost.png file in the DS_Example folder, we can identify the following elements:_

```
- category (or tag)
- title
- author
- date (publishingDate)
- coverImage
- content (which in this case is a mix of paragraphs, "h2", images, quotes,... )
```

_The data types are important as well. Here's an example data structure as a JavaScript object literal:_

```
const postStructure = {
id : string,
category : string,
title : string,
author : authorStructure | null,
date : date,
coverImage : string,
content (which in this case is a mix of paragraphs, "h2", images, quotes,... ) : contentStructure[],
}
```

_To complete this, we need two additional structures: authorStructure and contentStructure. This modular approach is a common practice, as we'll later explore in Mongoose._

```
const authorStructure = {
id : string,
firstName : string,
lastName : string,
portrait : string,
}
```

```
const contentStructure = {
contentType : "sectionTitle" | "paragraph" | "image" | "quote",
contentValue : string
}
```

Practice with the designs in the other folders. Consider questions like:

- What's the best data type for each key? Should it allow multiple values (like author: authorStructure | null) or be constrained (like contentType in contentStructure)?
- Should this be a single structure or split into multiple structures?
- What's the best way to relate two structures? For example, should postStructure have an author key, should authorStructure have a post key, or should both reference each other?

## UI

This folder contains 5 subfolders, each focused on a different subject.

In each folder, you'll find one or more designs and a data file (except in the UI4 folder, which contains instructions in markdown format). **Your task is to recreate the designs**.

All designs are in desktop view.

It's recommended, but not required, to make your work mobile-first. If you do, start developing with mobile in mind!

Remember: focus on **structure first, styling after**.

Ignore functionality for the most part, specially context, and routing — these exercises are specific to a local context.

You may use react-icons, but **no other libraries** (such as Bootstrap, Tailwind, any CSS frameworks, or component libraries like Material UI, Shadcn, Chakra UI, Swiper, etc.).
