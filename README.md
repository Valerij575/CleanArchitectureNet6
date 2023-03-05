# CleanArchitectureNet6

	In this project, we will create solution and projects based on the clean architecture, 
	and define the project dependencies. 
	Also, we will create authentication endpoints and models for register, login requests and responses. 
	Finally, we will create an autentication service that returns a mock response, and use the "REST client". 
	In addition, we will set up dependency injection for both the application and infrastructure layers.

## Create solution and project

1. Create solution
	dotnet new sln -o EattingApp

2. Presentation layers
	dotnet new webapi -o EattingApp.Api --framework net6.0
	
3. Infrastructure project
	is responsible for handling external dependencies such 
	as databases, email providers, and external API.
	
	dotnet new classlib -o EattingApp.Infrastructure --framework net6.0
	
4. Contracts

	dotnet new classlib -o EattingApp.Contracts --framework net6.0

	
5. Application

	dotnet new classlib -o EattingApp.Application --framework net6.0
	
	
6. Domain
	contains the core logic of the application and
	it defines the business rules and models the entities, 
	as well as the relationships between them

	dotnet new classlib -o EattingApp.Domain --framework net6.0
	
After created all projects, we need to add to the solution

dotnet sln add (ls -r **\*.csproj)
(or dotnet sln add src\EattingApp.Api for each projects)

dotnet build

### Create dependencies



