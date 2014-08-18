# The Two Sides of Spoonium

## Client

On the client, Spoon leverages: 

- The Spoon IDE and command line interface, for creating and managing containers locally
- The Spoon Plugin, for end-user deployment and container synchronization
- The Spoon VM, which underlies the Spoonium container framework and manages all containerized processes

#### Spoon IDE and Command Line Interface

The Spoon IDE, previously known as **Spoon Studio**, allows developers and systems administrators to build Spoon images through a friendly graphical user interface. The Spoon IDE is most commonly used for it's "snapshot" method of containerization. 

The Spoon command line interface (CLI) is a command line tool for creating containers and building images in real-time. The Spoon CLI also provides a suite of tools for managing containers and images. 

**Developers** can use the Spoon CLI to containerize their entire dev stack into their application -- ensuring that the same product a developer sees is the one encountered by end-users. 

**Sys admins** can use the Spoon CLI to more effectively manage their infrastructure. 

#### The Spoon Plugin

The Spoon Plugin is a small browser plugin that anyone can download from [Spoon](http://start.spoon.net/install). It comes packaged with the Spoon VM and the Spoon CLI, and will allow any Windows computer to run any containerized application. 

#### The Spoon VM

Underlying the Spoonium container framework is the Spoon VM. The Spoon VM is responsible for spawning and managing containers. 

## Server

Spoonium supports deployment to both public and private **hub** servers. 

#### Spoonium Hub

The [Spoonium Hub](http://spoonium.net/hub) is a public, SaaS platform for hosting and distributing Spoon images. 

**Repositories** on the hub host the images for a single project or product. For example, all of the trusted .NET images can be found under the spoonbrew/dotNet repository. 

Within a repository exists the entire version history of that project. Users can instantly pull or run the latest version of the project or rewind through the project's history and run a legacy version. 

Repositories may be public *or* private. All Spoonium accounts come with *unlimited* public repositories while private repositories require a paid account. 

**Why Use the Spoonium Hub?**

Because it will make your life much, much easier!

The hub can serve as an endpoint for end-user deployment as well as a hub for internal development. New application releases can be pushed to a public repository, where they can be run by your end-users with the click of a button. 

Internal and pre-release builds can, meanwhile, be held in private repositories where they can only be accessed by the members of your organization. When a build is ready for release, simply `spoon push` it to a public repository and deployment is done!

#### Spoon Server

If your organization would like to host their own internal Spoonium hub, Spoon provides a private hosting solution **Spoon Server**. Spoon Server can be hosted on any Windows machine and provides the same functionality as the Spoonium Hub, but hosted entirely on your organization's network. 

For more information, contact the Spoon sales team at [sales@spoon.net](mailto:sales@spoon.net). 