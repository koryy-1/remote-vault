dotnet new sln --name "sln name"
dotnet new classlib -o <classlib name>
dotnet new console -o <console project name>
dotnet new webapi -o <webapi project name>
dotnet sln <name>.sln add <path to proj>
dotnet add app/app.csproj reference lib/lib.csproj