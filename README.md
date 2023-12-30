# template

## Steps to initialize repos
* `git submodule update --init`
pulls down the content from each repo
* `git submodule foreach git checkout main`
recursively checks out all the repos to the develop branch
* All the projects should be initialized to their develop branch

### Folder Structure
```
├── app #the frontend
│   ├── dashboard #admin dashboard for managing the app
│   ├── lib #component libraries used in the frontend
│   │   └── lib-react-native (submodule) #react native component libraries
│   │       ├── doc #documentation for the component library
│   │       └── src #root source folder for the component library
│   │           ├── assets #assets directory for all media, font, and other assets 
│   │           ├── cloud #rest or sdk access to the backend
│   │           ├── components #various components to be used in the react native app
│   │           ├── constants
│   │           ├── contexts
│   │           ├── forms #forms
│   │           │   ├── FormBuilder #form builders built on top of react-native-forms
│   │           │   └── component #formes specific component library
│   │           ├── helpers
│   │           ├── hook
│   │           ├── mocks
│   │           ├── navigation #includes the navigation builder
│   │           ├── screens
│   │           │   └── Authentication #default authentication for apps
│   │           └── styles
│   └── mobile (submodule) #the react native mobile app directory
│           ├── __tests__
│           ├── android
│           ├── ios
│           └── node_modules
│           └── src #root source folder for the app
└── server  #the backend
    └── parse-b4a #backend items from back4app
        ├── cloud #cloud code for back4app. can be deployed using b4a cli
        └── public #webapps 
```