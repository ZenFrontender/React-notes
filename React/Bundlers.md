
Bundlers like Parcel, its main job is to bundle our application, like in our application we have so many components or JS files, it bundles all those JS files and gives us a single JS file.

Well it does many other things but the main and most critical operation that bundler does is bundling the application.

So other things a bundler like Parcel does:

- it creates a Dev build

- it runs the dev build on a Local Server

- HMR = Hot module replacement

- It uses a file Watching algorithm which is written in C++ => it keeps watching all the files as soon as a change is made it automatically rebuilds the app

- Caching - Faster builds using caching and saving in parcel-cache folder

- Image Optimization

- for production build it does minification of files

- Bundling

- Compressing

- Consistent Hashing

- Code Splitting

- Diffrential Bundling - support older browsers

- Diagnostics

- Error Handling

- HTTPs

- Tree Shaking - removes unused code

- Different Dev and Production builds