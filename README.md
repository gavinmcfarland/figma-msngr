# Msngr

Messenger is a simple message handler for Figma.

> [!NOTE]
> This hasn't been packaged yet and is mainly a learning experience for me.

### Create an instance of Msngr

In both the UI and main code you'll need to create an instance of Msngr.

```ts
const msngr = new Msngr();
```

### Defining handlers

Define your event handlers.

```ts
const msngr = new Msngr({ handlers });

const handlers = {
  greet(value: any) {
    console.log(value);
  },
};
```

### Emitting a message

Calling emit invokes the event handler for the matching event name in either UI or main context.

```ts
msngr.emit("greet", "Hello world!");
```

### Awaiting a response

After emitting a message you can await a response

```ts
let res = await msngr.emit("greet");
```
