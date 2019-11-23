This is the collect-all repository for the Fogget-About-It grow system, a management system and user console for a fleet of computerized fogponics growrooms, powered by commodity embedded systems. It is intended to be as user-friendly as possible for home users and non-technically inclined folk. It is currently in the form of Java projects - in the near future, we aim to turn these into a turn-key solution and build a user community.
 
Here are its constituent projects:

https://github.com/ColinGilbert/fogget-backend

```
The main part of the control system. Automatically configures new embedded systms that are aded to the network.
```

https://github.com/ColinGilbert/fogget-common
```
Java utilities that are used by all parts of the system - must be downloaded prior to building the project.
```

https://github.com/ColinGilbert/fogget-ui
```
A web interface that allows a new user to start managing their systems.
```

https://github.com/ColinGilbert/fogget-backend-ui-state-xfer
```
A small utility that decouples the UI from the backend. Must run on the same device as the backend itself prior to connecting the UI. It runs within a JSP/Servlets environment.
```

https://github.com/ColinGilbert/PlantSystemSimulator
```
A test program that allows you to simulate an embedded system prior to installing a real one.
```


Library dependencies
```
- Jackson 3. For JSON serialization/deserialization.
- Eclipse Paho MQTT client, Java.
```

Environment dependencies
```
- An MQTT broker running on the same device as the backend. We used Mosquitto.
- The embedded systems must each have a unique 64-bit integer programmed id (UID) into it prior to connection.
```

Future plans:
```
- Arduino code for embedded systems
- Program that creates a UID and a corresponding binary for loading onto a new embedded system
- A command-line app for pro users/Linux people
- A view-only GUI for monitoring purposes
- Further sweetening for the end-user
- Federated management
- Additional security measures
```
