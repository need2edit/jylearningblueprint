# Making an HBO Clone

A clone of the HBO app for iOS. For eductational purposes only. The HBO app is a fantasitic app with rich content, unique UI, and a lot of custom appearance work. I wanted to learn a lot, so I cloned it.

## Overview

Describing an App's structure and mechanics is a good way to scope out and understand what to build.

## App Behavior

What does the app do?

- Plays movies and TV episodes.
- Keeps track of what your are watching.
- Searches a library of content.
- Allows you to manually add content to your own list.
- Signs in and out of an account.
- Organizes content in various forms (featured, popular, trending)

## App Anatomy

The apps screens and components are described below.

### Overall Look and Feel

The app has a highly customized look and feel, themed with a custom color scheme. Buttons have a branded appearance, all screens have a custom background. Lots of rich imagery is loaded remotely on all screens.

### Tab Bar

The app has 3 tabs:

1. Home - The latest content, continue watching, for you, my list, just added, popular movies, popilar TV, and other trending content.
2. Search - Find what youre looking for with text search, explore collections, and popular searches.
3. Account - A place to switch profiles, see your list of content, and continue watching.

### The Side Bar

The HBO app has a sidebar that animates in from the left and is dismisses by tapping an X. It occupies around 90% of the screen width on an iPhone.

The content of the sidebar is a scrolling list of items, in multiple sections. 

1. The first section is various zones of the app featuring different kinds of content.
2. The second section is categories.
3. The third section is audio description content.
4. The fourth section is HBO channels (e.g. HBO, Cinemax, Adult Swim)

- App Zones
    - Series
    - Movies
    - Originals
    - Just Added
    - Last Chance
    - Coming Soon
    - Trending Now
    - Awards and Aclaim
- Categories
    - Action
    - Animation
    - Comedy
    - Crime
    - Documentaries
    - Drama
    - Fantasy & Sci-Fi
    - Horror
    - International
    - Kids & Family
    - Latino
- Audio Description
- Channels
    - HBO
    - Max Originals
    - DC
    - TCM

### TV Show - Details Screen

When tapping on a TV show additional details are shown:

- A thumbnail of the content bleeding under the navigation bar.
- A play button.
- Button to add to your list.
- Button to play a trailer.
- Button to download.
- Title and Description.
- A seasons area listing the episodes.
- Each episode has a thumbnnail title, duration, rating and download button.

### TV Show - Episode Screen

Similar to the TV Show Details Screen, this screen shows:

- A thumbnail of the content bleeding under the navigation bar.
- A play button.
- Button to add to your list.
- Button to play a trailer.
- An extras section with a horizontal carousel of additional content.
- Collapsable headers for Cast and Crew, Producers, Directors, Writers, Rating each with a 50-50 layout.

### Movie - Details Screen

When tapping on a Movie additional details are shown:

- A thumbnail of the content bleeding under the navigation bar.
- A play button.
- Button to add to your list.
- Button to play a trailer.
- Button to download.
- Title and Description.
- A "more like this" section with a horizontal carousel of other movies. Each movie shows a thumbnail without title or additional information. A small lable shows the channel (HBO, Cinemax).
- Collapsable headers for Cast and Crew, Producers, Directors, Writers, Rating each with a 50-50 layout.

### Home Screen

- Multiple horizontal carousels with different aspect ratios.
    - Movies have a 2/3 vertical rectangle.
    - Episodes may have a 4/3 horizontal rectangle.
- Some areas are a single large header with a button for more info.
- "Hubs" show extra large rectangular content and link to the channels areas in the sidebar above.

### Search Screen

- A search bar in the navigation area.
- A horizontal scrolling carousel of collections to explore.
- Popular searches: A 2x2 grid of movies and TV shows with 2/3 vertical rectangular thumbnails.

### Progress Bar

A small progress bar may appear on multiple elements showing the overall viewing status of a movie or TV show.

### Playback Screen

- A rewind 15s button.
- A fast forward 15s button.
- An airplay button.
- A captions button.
- A scrubber to navigate.
- A channel logo with a title.


## Planning the Build

How would we go about building this? Do we use UIKit? Do we use SwiftUI? Both?

### Use Cases for UIKit

This app has a lot of grids. Some scrolling horizontally, others vertically. It is a strong use case for UICollectionView and UICollectionViewCompositionalLayout.

### Use Cases for SwiftUI

This app has a lot of grids. It is a strong use case for using ScrollViews with LazyVGrids and LazyHGrids. There is also a lot of appearance customization that SwiftUI might be better at than UIKit.

### Data Storage

The app loads JSON from a server to show its content. Storing data locally could occur with a variety of technologies:

- User Defaults
- Core Data
- Realm or some other third party library.


