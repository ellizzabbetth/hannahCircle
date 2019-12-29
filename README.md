

Running Application
dotnet run -p API
or 
cd API/
dotnet watch run


Solution Creation:

mkdir hannahCircle
cd .\hannahCircle\
dotnet new sln
dotnet new classlib -n Domain
dotnet new classlib -n Application
dotnet new classlib -n Persistence
dotnet new webapi -n API
dotnet sln add Domain/
dotnet sln add Application/
dotnet sln add Persistence/
dotnet sln add API/
cd Application/
    dotnet add reference ../Domain/
    dotnet add reference ../Persistence/
cd API/   
    dotnet add reference ../Application/
cd Persistence/
    dotnet add reference ..\Domain\