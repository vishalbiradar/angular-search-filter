# Angular Search

Searching/filtering an object from the list of object using ng2-search-filter.

Steps:

1. Install the required packages
  ```sh
  npm install ng2-search-filter --save
  ```

2. Import Ng2SearchPipeModule from ng2-search-filter

  app.module.ts

  ```js

  // search module
  import { Ng2SearchPipeModule } from 'ng2-search-filter';

  @NgModule({
    ....
    ....

    imports: [
      Ng2SearchPipeModule
    ]
  })
  export class AppModule { }
  ```

3. Create a mock list in app.component.ts file

  ```js
  heroes = [
      { id: 11, name: 'Mr. Nice', country: 'India' },
      { id: 12, name: 'Narco' , country: 'USA'},
      ...
      ...
    ];
  ```
4. Let's create a search input field

  ```js
  <input type="text" [(ngModel)]="searchText">
  ```

5. Let's apply filter logic on the list

  ```
   filter: searchText
  ```
will do the magic of searching/filtering the object/element from the list.

So the actual iteration look like:

  ```js
   <div *ngFor="let hero of heroes | filter: searchText">
          <span>{{hero.id}}</span>
          <span>{{hero.name}}</span>
          <span>{{hero.country}}</span>
   </div>
  ```
  
  ## Demo
  
  https://stackblitz.com/edit/angular-search-demo


