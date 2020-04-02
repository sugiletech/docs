- [Getting Started](#getting-started)
  - [Your First App](#your-first-app)
    - [Creating new project](#creating-new-project)
      - [Stackblitz](#stackblitz)
      - [Angular CLI](#angular-cli)
    - [Template Syntax](#template-syntax)
      - [Interpolation {{}}](#interpolation)
      - [*ngFor](#ngfor)
      - [Property Binding []](#property-binding)
      - [*ngIf](#ngif)
      - [Event Binding ()](#event-binding)
    - [Components](#components)
    - [Input](#input)
    - [Output](#output)
  - [Routing](#routing)

# Getting Started

## Your First App

### Creating new project

#### Stackblitz

#### Angular CLI

### Template Syntax

#### Interpolation {{}}

#### *ngFor

- Eg: `<div *ngFor="let item of items; let itemIndex=index">{{item}}</div>`

#### Property Binding []

-Eg: `<span [title]="expression"></span>`

#### *ngIf

#### Event Binding ()

- Eg: `<button (click)="handleClick()">Click Me!</button>`

### Components

- Class

  - `@Component` decorator
  - `selector`
  - `templateUrl`
  - `styleUrls`

- HTML Template
- Styles

### Input

  - Passing data from parent to child component
  - ```
    [data]="localData"

    @Input() data
    ```
### Output

  - Triggering event from child to parent component
  - ```js
        @Output() notify = new EventEmitter();
        notify.emit();

        (notify)="handleChildEvent()"
    ```

## Routing

